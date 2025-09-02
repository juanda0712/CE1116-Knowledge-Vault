# **Mecanismo de atención utilizado en la arquitectura de Transformers**

El mecanismo de atención permite que un modelo enfoque su procesamiento en las partes más relevantes de la información. Cada token del input se proyecta en tres vectores: query (Q), key (K) y value (V), generados mediante matrices de pesos aprendibles (WQ, WK, WV) aplicadas a los embeddings de entrada. Los pesos de atención se calculan mediante el producto punto de Q y K, escalado por √dk para estabilidad numérica, y normalizados con Softmax, luego aplicados a V para obtener la representación final de cada token.
En Transformers, se usa self-attention, donde cada token atiende a todos los demás para capturar dependencias largas. El mecanismo se implementa como multi-head attention, donde cada cabeza aprende diferentes relaciones (sintácticas, semánticas, contextuales); las salidas se concatenan y se proyectan linealmente mediante WO. Para decodificadores autorregresivos, se aplica enmascaramiento causal para garantizar generación secuencial correcta.
El mecanismo forma parte de los bloques Transformer, que incluyen Feed-Forward Networks (FFN) para abstracción de alto nivel, así como conexiones residuales y Layer Normalization para estabilidad del entrenamiento. Aunque es altamente paralelizable, su complejidad es O(n²·d) respecto a la longitud de la secuencia, limitando la ventana de contexto de los LLMs.

## 📚 Idea/Concepto

Proceso mediante el cual un modelo asigna diferentes pesos a cada parte de una secuencia al procesar un token, permitiéndole enfocarse en las partes más relevantes para la tarea.

## 📌 Puntos Claves (Opcional)

- Se basa en el cálculo de similitud entre vectores Query, Key y Value.
- Atención escalada por el producto punto (Scaled Dot-Product Attention).
- Permite paralelismo y sustituye recurrencia.

## 🔗 Connections

- [[Large Language Models (LLMs)]]
- [[Embeddings]]
- [[Ventana de Contexto del modelo]]
