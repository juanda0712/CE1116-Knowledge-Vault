# **Tokenización**

La tokenización es el proceso fundamental de preprocesamiento en modelos de lenguaje y arquitecturas multimodales. Consiste en segmentar la entrada (texto, audio, imagen o video) en unidades mínimas llamadas tokens, que representan la base operativa del modelo. En el caso del texto, cada token se convierte en un ID numérico único dentro de un vocabulario y, posteriormente, se proyecta en un vector denso mediante la matriz de embeddings (W_E), la cual funciona como una tabla de consulta y cuyos valores se aprenden y ajustan durante el entrenamiento para capturar relaciones semánticas.
Los métodos modernos de tokenización, como BPE y WordPiece, permiten dividir palabras en subunidades, lo que reduce el tamaño del vocabulario, mejora la representación de palabras raras y ofrece una solución eficiente al problema de las palabras fuera de vocabulario (OOV). Esta estrategia asegura un equilibrio entre la compacidad del vocabulario y la fidelidad semántica.
En arquitecturas actuales, el concepto de token trasciende el texto y se extiende a segmentos de otras modalidades (píxeles de imágenes, espectrogramas de audio, fragmentos de video), lo que permite integrar diferentes tipos de datos bajo un marco unificado. De esta manera, la tokenización no solo facilita la entrada al modelo, sino que también define la granularidad de la información y constituye el puente entre datos crudos y representaciones vectoriales que impulsan el aprendizaje profundo.

## 📚 Idea/Concepto

Proceso de dividir un texto en unidades más pequeñas llamadas tokens, que pueden ser caracteres, subpalabras o palabras completas, y que sirven como entrada a los modelos de lenguaje.

## 📌 Puntos Claves (Opcional)

- Métodos comunes: BPE, WordPiece, SentencePiece.
- Define cuántos tokens ocupa una oración.
- Afecta directamente la eficiencia y precisión del modelo.

## 🔗 Connections

- [[Embeddings]]
- [[Ventana de Contexto del modelo]]
- [[Large Language Models (LLMs)]]
