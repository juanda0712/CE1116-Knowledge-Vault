# **Large Language Models (LLMs)**

Un Large Language Model (LLM) es un modelo de Deep Learning entrenado con enormes volúmenes de texto y miles de millones de parámetros, diseñado para predecir la siguiente palabra en una secuencia, lo que le permite capturar patrones complejos y conocimiento del mundo.
Se basan en la arquitectura Transformer, cuyo núcleo es el mecanismo de autoatención, que identifica qué partes del texto son relevantes en cada paso. Cada bloque incluye Feed-Forward Networks (FFN) para abstraer patrones de alto nivel, así como conexiones residuales y Layer Normalization que estabilizan el entrenamiento. Las palabras se representan mediante embeddings y se aplica codificación posicional para preservar el orden de la secuencia. La generación de texto utiliza Softmax y puede ajustarse con la temperatura para controlar la diversidad de las predicciones. En decodificadores como GPT, se emplea atención causal para evitar que tokens futuros influyan en los presentes.
El entrenamiento se realiza en dos fases: pre-entrenamiento (aprendizaje general) y fine-tuning (adaptación específica). Durante el entrenamiento, se ajustan los parámetros; durante la inferencia, se genera texto a partir del modelo ya entrenado. Los Transformers permiten paralelización masiva, aunque la ventana de contexto finita limita la memoria en interacciones largas. A escalas masivas, los LLMs desarrollan habilidades emergentes, como razonamiento complejo, que van más allá de su objetivo de predicción de palabras.

## 📚 Idea/Concepto

Modelos de aprendizaje profundo con miles de millones de parámetros, entrenados en grandes cantidades de texto, que aprenden patrones estadísticos y contextuales del lenguaje para generar, resumir o razonar sobre texto.

## 📌 Puntos Claves (Opcional)

- Escalan en parámetros (ej. GPT-3 con 175B).
- Usan arquitecturas Transformer.
- Se adaptan a tareas con pocas instrucciones (few-shot).

## 🔗 Connections

- [[Redes Neuronales]]
- [[Mecanismo de atención utilizado en la arquitectura de Transformers]]
- [[Ventana de Contexto del modelo]]
