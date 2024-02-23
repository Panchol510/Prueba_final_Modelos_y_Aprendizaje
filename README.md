## <span style="font-size:larger;">Prueba Final - Modelos y Aprendizaje</span>


**Objetivo**: En el notebook probar al menos con 3 modelos, evaluarlos y decidir cuál es el mejor, justificando la respuesta en base a las matrices de confusión que aparecen al evaluar el error en training y en test.

**Carga de datos**
El primer paso es la carga de del data set a través del comando “pd.read_csv” y así su exploración

**Procesamiento de la información**
Se procede con la verificación de la información del dataset para analizar si hay duplicados, nulos, blancos y el tipo de variable. 

**Categorización de variable**
Se procede categorizar la variable “M” con el valor “1” y “B” con el valor “0” con el fin de agrupan datos similares en distintas categorías o clases, lo que facilita su análisis y comprensión.

**Análisis del desbalanceo de los datos**
Para el valor 0, que parece corresponder a un diagnóstico negativo, hay 357 casos en el conjunto de datos. Para el valor 1, que parece corresponder a un diagnóstico positivo, hay 212 casos en el conjunto de datos.
Hay un desequilibrio en la distribución de clases en el conjunto de datos, ya que hay más casos con diagnósticos negativos (357) que positivos (212). Este desequilibrio puede afectar el rendimiento de ciertos modelos de aprendizaje automático y debe ser tenido en cuenta durante el proceso de modelado y evaluación

**Balanceo de datos**
El objetivo del balanceo de datos es corregir desequilibrios en la distribución de clases dentro de un conjunto de datos. En muchos problemas de clasificación, puede ocurrir que una clase esté sobrerrepresentada en comparación con otras, lo que puede llevar a un sesgo en el modelo de aprendizaje automático hacia la clase mayoritaria y a un rendimiento deficiente en la clasificación de las clases minoritarias. Se utilizó la técnica de submuestreo aleatorio (Random Under-Sampling) para equilibrar las clases en un conjunto de datos desequilibrado y así se obtuvo  "0" = 212 & "1" =212

**Escalamiento de los datos**
Esta técnica es utilizada en el preprocesamiento de datos que tiene como objetivo estandarizar las características de un conjunto de datos, es decir, ajustarlas a una escala común. Esto se hace para que todas las características contribuyan por igual al análisis o al modelo de aprendizaje automático, evitando así que una característica con una escala mucho mayor domine sobre otras características durante el análisis.

**Por el tipo de información que contiene el dataset se estimó que los modelos más apropiados son: Modelo Logistic Regression, Modelo árbol de decisión y Modelo Radom forest**

**Ventaja y desventaja de cada modelo**

<span style="text-decoration: underline;">Modelo Logistic Regression:</span>

Ventajas:
   Buen desempeño en términos de precisión, recall y accuracy.
  Interpretabilidad: Es fácil de entender y explicar cómo funciona el modelo.
  
  Desventajas:
   Limitado a problemas lineales: La regresión logística asume una relación lineal entre las variables de entrada y la variable de salida, lo que puede limitar su capacidad para 
   modelar relaciones complejas.

Modelo árbol de decisión:

    
   Ventajas:
    Fácil de entender e interpretar: Los árboles de decisión pueden visualizarse fácilmente, lo que facilita su explicación a personas no técnicas.
    Capacidad para manejar datos no lineales: Los árboles de decisión pueden manejar relaciones no lineales entre las variables de entrada y la variable de salida.
    
   Desventajas:
    Propensos al sobreajuste: Los árboles de decisión tienden a sobreajustarse a los datos de entrenamiento, lo que puede resultar en un rendimiento deficiente en datos no vistos.

Modelo Radom forest:
  
  Ventajas:
  Reducción del sobreajuste: Random Forests mitigar el sobreajuste mediante el promedio de múltiples árboles de decisión entrenados en subconjuntos aleatorios del conjunto de datos.
  Buen rendimiento: Suelen tener un rendimiento sólido en una variedad de conjuntos de datos y son menos propensos al sobreajuste que los árboles de decisión individuales.
  
  Desventajas:
  Menos interpretables que los árboles de decisión individuales: Debido a que Random Forests están compuestos por múltiples árboles de decisión, pueden ser más difíciles de       
  interpretar y visualizar que un solo árbol de decisión.


**Modelo Logistic Regression**

Resultados:

Recall Score 
Test: El modelo tiene una tasa de recuperación del 90% en el conjunto de datos de prueba. Esto significa que de todos los casos positivos en el conjunto de datos, el 90% fueron identificados correctamente por el modelo como positivos.
Train: En el conjunto de datos de entrenamiento, la tasa de recuperación es del 91.28%. Esto indica que, durante el entrenamiento, el modelo identificó correctamente el 91.28% de todos los casos positivos.

Accuracy Score
Test: La exactitud del modelo en el conjunto de datos de prueba es del 96.49%. Esto significa que el 96.49% de las predicciones hechas por el modelo en el conjunto de datos de prueba fueron correctas.
Train: En el conjunto de datos de entrenamiento, la exactitud es del 96.48%. Esta métrica indica que el 96.48% de las predicciones hechas por el modelo durante el entrenamiento fueron correctas.

Precision Score
Test: La precisión del modelo en el conjunto de datos de prueba es del 100%. Esto significa que, de todas las instancias clasificadas como positivas por el modelo, el 100% fueron realmente positivas.
Train: En el conjunto de datos de entrenamiento, la precisión es del 99.37%. Esto indica que el 99.37% de todas las instancias clasificadas como positivas por el modelo durante el entrenamiento fueron realmente positivas.

**Modelo árbol de decisión**

Resultados:

Recall Score
Test: El modelo tiene una tasa de recuperación del 87.5% en el conjunto de datos de prueba. Esto significa que de todos los casos positivos en el conjunto de datos, el 87.5% fueron identificados correctamente por el modelo como positivos.
Train: En el conjunto de datos de entrenamiento, la tasa de recuperación es del 100%. Esto indica que durante el entrenamiento, el modelo identificó correctamente el 100% de todos los casos positivos.

Accuracy Score 
Test: La exactitud del modelo en el conjunto de datos de prueba es del 92.98%. Esto significa que el 92.98% de las predicciones hechas por el modelo en el conjunto de datos de prueba fueron correctas.
Train: En el conjunto de datos de entrenamiento, la exactitud es del 100%. Esta métrica indica que el 100% de las predicciones hechas por el modelo durante el entrenamiento fueron correctas.

Precision Score 
Test: La precisión del modelo en el conjunto de datos de prueba es del 92.11%. Esto significa que de todas las instancias clasificadas como positivas por el modelo, el 92.11% fueron realmente positivas.
Train: En el conjunto de datos de entrenamiento, la precisión es del 100%. Esto indica que el 100% de todas las instancias clasificadas como positivas por el modelo durante el entrenamiento fueron realmente positivas.

**Modelo Radom forest**

Resultados:

Recall Score 
Test: El modelo tiene una tasa de recuperación del 95% en el conjunto de datos de prueba. Esto significa que de todos los casos positivos en el conjunto de datos, el 95% fueron identificados correctamente por el modelo como positivos.
Train: En el conjunto de datos de entrenamiento, la tasa de recuperación es del 100%. Esto indica que durante el entrenamiento, el modelo identificó correctamente el 100% de todos los casos positivos.

Accuracy Score 
Test: La exactitud del modelo en el conjunto de datos de prueba es del 98.25%. Esto significa que el 98.25% de las predicciones hechas por el modelo en el conjunto de datos de prueba fueron correctas.
Train: En el conjunto de datos de entrenamiento, la exactitud es del 100%. Esta métrica indica que el 100% de las predicciones hechas por el modelo durante el entrenamiento fueron correctas.

Precision Score
Test: La precisión del modelo en el conjunto de datos de prueba es del 100%. Esto significa que de todas las instancias clasificadas como positivas por el modelo, el 100% fueron realmente positivas.
Train: En el conjunto de datos de entrenamiento, la precisión es del 100%. Esto indica que el 100% de todas las instancias clasificadas como positivas por el modelo durante el entrenamiento fueron realmente positivas.

**Conclusión**

Basándonos únicamente en los resultados proporcionados, la mejor opción entre Regresión Logística, Árbol de Decisión y Random Forest sería el modelo de Random Forest. 

Rendimiento en el conjunto de prueba
El Random Forest muestra un alto rendimiento en términos de precisión, recall y accuracy tanto en el conjunto de prueba como en el conjunto de entrenamiento.
Tiene una precisión del 100% en ambos conjuntos de datos para predecir ambas clases (benigno y maligno).

Generalización y mitigación del sobreajuste:
Random Forest tiende a generalizar bien a datos no vistos y a mitigar el sobreajuste gracias a su naturaleza de promediar múltiples árboles de decisión entrenados en subconjuntos aleatorios del conjunto de datos.

Capacidad para manejar relaciones no lineales:
Random Forest puede manejar relaciones no lineales entre las variables de entrada y la variable de salida, lo que lo hace adecuado para problemas con características complejas.
