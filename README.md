# TinyGPT

En clase el profe dijo que íbamos a tener **dos TPs, los dos individuales**, más un trabajito
en clase. Los dos van juntos: primero armo un GPT chiquito y lo entreno (TP1), y después
agarro ese mismo modelo y le hago fine-tuning (TP2).

## Los dos TPs

### TP1 — armar y entrenar el TinyGPT → `01_pretraining/`
- Preentrenar un GPT chiquito (un decoder tipo GPT) a nivel de caracteres.
- Jugar con las estrategias de decodificación (greedy, temperatura, top-k, top-p).
- Sumar el KV-cache y ver si realmente acelera.
- Cambiar el bloque feed-forward por un **Mixture of Experts** (como DeepSeek/Mixtral) y
  comparar contra el modelo denso.
- Al final, entrenar una versión con el tokenizer de **GPT-2**. Ese es el modelo que después
  uso en el TP2.
- Se entrega **antes de la clase 7**.

### TP2 — fine-tuning → `02_finetuning/`
- Agarrar el modelo que entrené en el TP1 y hacerle **fine-tuning**.
- El profe dijo que un GPT preentrenado NO es un chatbot: solo completa texto. Con el
  fine-tuning lo convierto en algo útil (un clasificador o un asistente tipo chat).
- Se entrega **antes de la clase 8**.

## Data importante
- Los dos TPs son **individuales**.
- El TP2 **depende del modelo del TP1**, así que ese checkpoint lo tengo que guardar.
- Se corre tranqui en **Google Colab**, no hace falta hardware grande.
- Se entrega mandando el link del repo de GitHub por mail al profe.
