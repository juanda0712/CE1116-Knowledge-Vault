# **Embeddings**

Los embeddings son representaciones numéricas densas y aprendibles de tokens o unidades de información en un espacio vectorial de varias dimensiones, diseñadas para capturar similitudes semánticas y relaciones contextuales. Cada embedding es un vector de parámetros aprendibles, ajustado durante el entrenamiento mediante minimización de una función de coste y retropropagación.
En los Transformers, los embeddings iniciales funcionan como una tabla de consulta (lookup table) y se refinan progresivamente mediante los bloques de atención, generando embeddings contextuales, donde la representación de un token depende de su contexto en la frase (por ejemplo, “banco” de río vs. “banco” financiero). La dimensionalidad de los embeddings (p. ej., 512, 768, 12288) es un hiperparámetro crítico que determina la riqueza de la representación.
Los embeddings incluyen información posicional (Positional Encoding) para que el modelo comprenda el orden de los tokens, dado que los Transformadores carecen de recurrencia. Los vectores de Query, Key y Value se derivan mediante proyecciones lineales de los embeddings (multiplicados por matrices WQ, WK, WV) antes de calcular la atención.
Además, los embeddings pueden ser multimodales, integrando texto, imágenes y audio en un mismo espacio vectorial, permitiendo un procesamiento integral y contextualizado. Por ejemplo, un modelo puede analizar una imagen de comida y generar consejos nutricionales relevantes combinando información visual y textual.
Esta definición se centra en embeddings densos y aprendibles, que son la base de los modelos modernos de lenguaje, sin profundizar en representaciones dispersas anteriores (como one-hot encoding), manteniendo claridad y relevancia técnica.

## 📚 Idea/Concepto

Representaciones vectoriales densas de tokens, palabras o unidades de entrada en un espacio continuo de alta dimensión, donde la cercanía entre vectores refleja similitud semántica o sintáctica.

## 📌 Puntos Claves (Opcional)

- Generados inicialmente por lookup tables y refinados contextualmente.
- Dimensionalidad configurable (ej. 512, 768, 12288).
- Incluyen codificación posicional para mantener el orden.

## 🔗 Connections

- [[Tokenizacion]]
- [[Mecanismo de atención utilizado en la arquitectura de Transformers]]
- [[Redes Neuronales]]
