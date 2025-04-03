# regresion-lineal-CA_mama
Este codigo se realizo con la intension de tener un conocimiento sobre que factores afectan la desicion de las mujeres participantes
en la encuesta, para decidir hacerse el estudio de deteccion de cancer de mama, haciendo una regresion logisitica multivariable. 
Resumen de resultados:

Evaluación General del Modelo

Pseudo R-cuadrado: 0.2831
Este valor indica que el 28.31% de la variabilidad en la realización de la mastografía es explicada por las variables independientes. Aunque no es un valor alto, en modelos de salud y comportamiento no es raro obtener valores relativamente bajos.

Log-Likelihood (-140.07) vs. LL-Null (-195.39)
El modelo con predictores tiene un log-likelihood más alto, lo que sugiere que mejora significativamente con respecto a un modelo sin variables explicativas. Además, el LLR p-value (4.488e-18) confirma que el modelo en su conjunto es estadísticamente significativo.

Interpretación de los Coeficientes
Cada coeficiente refleja el efecto de una variable en la probabilidad de realizarse la mastografía, manteniendo las demás constantes.

Edad (+0.1176, p=0.000): Este coeficiente es significativo y positivo. Indica que a mayor edad, mayor es la probabilidad de realizarse la mastografía.

Estado civil (-0.1746, p=0.174): No significativo. No parece influir de manera fuerte en la decisión de realizarse la mastografía.

Escolaridad (+0.2119, p=0.180): No significativo. La educación podría influir, pero no de manera estadísticamente fuerte.

Religión (+0.4748, p=0.068): Casi significativo. Puede haber una leve relación entre la religión y la mastografía.

Tiene hijos (-6.1225, p=0.005): Significativo y negativo. Indica que las mujeres con hijos tienen una probabilidad mucho menor de hacerse una mastografía.

Número de hijos (-0.0543, p=0.750): No significativo. No parece haber relación entre la cantidad de hijos y la realización de la mastografía.

Familiar con cáncer de mama (-0.0742, p=0.865): No significativo. No parece influir en la decisión.

Labora (trabajo) (+0.1561, p=0.588): No significativo. No hay evidencia clara de que el hecho de trabajar influya en la decisión de hacerse una mastografía.

Informada sobre el cáncer de mama (-0.9493, p=0.002): Significativo y negativo. Sorprendentemente, estar informada reduce la probabilidad de hacerse una mastografía.

Cree que la autoexploración es suficiente (+0.8640, p=0.008): Significativo y positivo. Las mujeres que creen que la autoexploración es suficiente tienen una mayor probabilidad de hacerse la mastografía, lo cual es contradictorio con la idea de que si consideran suficiente la autoexploración, podrían no realizar estudios adicionales.

Cree importante hacerse estudios (-0.4925, p=0.713): No significativo. La creencia sobre la importancia de realizar estudios no parece influir en la decisión.

Tiene dependientes (+0.0237, p=0.946): No significativo. No parece afectar la decisión de realizarse la mastografía.

Responsable económico (+0.2006, p=0.323): No significativo. No parece haber una relación clara.

Variables más significativas:

Edad (positiva)

Tiene hijos (negativa)

Estar informada sobre el cáncer de mama (negativa)

Creer que la autoexploración es suficiente (positiva)

Matriz de Confusión y Métricas del Modelo

Matriz de confusión:
[ 80  41 ]
[ 25 141 ]

Interpretación:

80: Mujeres predichas correctamente como que no se hicieron la mastografía.

41: Mujeres que se hicieron la mastografía, pero el modelo predijo que no (Falsos Negativos).

25: Mujeres que no se hicieron la mastografía, pero el modelo predijo que sí (Falsos Positivos).

141: Mujeres predichas correctamente como que sí se hicieron la mastografía.

Métricas de rendimiento del modelo:

Precisión (Accuracy) = 77.00%
El 77% de las predicciones fueron correctas.

Precisión de clase 0 (No se hizo la mastografía) = 76%

Precisión de clase 1 (Sí se hizo la mastografía) = 77%

Sensibilidad (Recall) de "Sí se hizo la mastografía" = 85%
El modelo identifica bien a las mujeres que sí se hicieron la mastografía.

F1-score = 0.81 para "Sí se hizo la mastografía", lo que indica un buen balance entre precisión y recall.

