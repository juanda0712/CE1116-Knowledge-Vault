# **Ventana de Contexto del modelo**

La ventana de contexto de un modelo de lenguaje es el límite de tokens que el Transformer Core procesa directamente en una sola pasada, funcionando como memoria de trabajo finita y no como memoria a largo plazo. Los tokens suelen ser subunidades de palabras o caracteres definidas por la tokenización, y su longitud máxima define la cantidad de información que el modelo puede considerar simultáneamente.
El tamaño de la ventana es un cuello de botella computacional, ya que la atención tiene complejidad O(n²·d), impactando directamente los costos operativos y la latencia durante la inferencia. Esto motiva la investigación en mecanismos de atención escalables, como la atención restringida, que permiten procesar secuencias más largas sin comprometer eficiencia.
En la práctica, se emplea Session History Stitching, donde el contenido relevante de interacciones anteriores se selecciona, reescribe y compacta antes de enviarse al modelo, optimizando la continuidad de la conversación o la generación de texto. La efectividad de los tokens puede variar según su posición: los del inicio o final suelen influir más que los del medio (“Lost in the Middle”), y la dilución del contexto puede afectar la coherencia de las respuestas.
El tamaño de la ventana es también un hiperparámetro crítico, definido por los diseñadores del modelo, que impacta directamente en su capacidad para manejar información y la calidad de sus predicciones.

## 📚 Idea/Concepto

Número máximo de tokens que un modelo puede procesar de manera simultánea para generar una respuesta coherente. Determina la cantidad de información que se puede mantener activa en memoria durante la predicción.

## 📌 Puntos Claves (Opcional)

- GPT-3: ~2,048 tokens; GPT-4: hasta 128k.
- Limita la extensión de documentos procesados.
- Impacta el costo computacional.

## 🔗 Connections

- [[Large Language Models (LLMs)]]
- [[Mecanismo de atención utilizado en la arquitectura de Transformers]]
- [[Tokenización]]
