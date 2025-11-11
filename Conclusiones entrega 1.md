# Data-Science-II-Entrega-Garcia-Bossio

Hipotesis a plantear para este proyecto:
1) Las ventas se mantuvieron durante todo el año
2) La categoria más vendida fue Elementos de oficina
3) El producto más vendido fue Tecnologia
4) Entre más premium el cliente, más compra

<img width="1588" height="890" alt="image" src="https://github.com/user-attachments/assets/8be17ea4-af49-4463-b449-300dca50d3f2" />
<img width="425" height="413" alt="image" src="https://github.com/user-attachments/assets/7e16cf16-25e9-4dfc-9335-2d1cacc7b260" />
<img width="1589" height="890" alt="image" src="https://github.com/user-attachments/assets/0ab9c14a-9439-4f70-99ca-f748026d1644" />



Resultados

Segun los datos obtenidos concluimos que:
1) Las ventas alcanzaron su pico máximo en feb, mar y jun
2) La mayor categoria vendida fue Office Supplies con un 63,4%
3) El producto más vendido no se relaciona con la tecnologia, de hecho fue la categoria menos vendida con un 15,8%
4) El tener una mejor categoría de cliente no hace comprar más (de hecho produjeron más cantidad de venta los clientes básicos)

Elegí un método de feature selection para reducir la dimensionalidad del dataset, seleccioné modelo Random Forest para evaluar la importancia de cada característica.
Realicé un análisis para identificar qué factores son los más importantes para impulsar las ventas totales. 
Primero, organicé y limpié los datos de ventas, incluyendo información como nombres de productos, categorías, fechas de venta y datos de los clientes. Luego, el modelo identificó automáticamente cuáles de estos
factores tienen el mayor impacto en el total de ventas.

¿Qué se encontró con esto?

Identifiqué los productos, categorías y clientes que más influyen en el total de ventas.
Descubrí patrones y relaciones clave que podrían no ser evidentes a simple vista.

¿Qué se podría hacer con esta información?

1) Optimizar estrategias de marketing: Enfocarse en los productos y categorías más influyentes para maximizar el retorno de inversión en marketing.
2) Mejorar la gestión de clientes: Identificar y fidelizar a los clientes más valiosos.
3) Tomar decisiones más informadas: Utilizar estos datos para predecir tendencias de ventas y ajustar el inventario y la producción en consecuencia.

En resumen, este análisis nos proporciona una visión clara y basada en datos sobre los factores que realmente impulsan las ventas. 
Esto permitirá tomar decisiones más estratégicas y optimizar los esfuerzos de la empresa para lograr un mayor crecimiento y rentabilidad.

Luego pasé a elegir un algoritmo de regresión o clasificación para entrenar con los datos elegidos. 
Elegí el modelo Random Forest Regressor porque es robusto y suele dar buenos resultados al predecir valores continuos como el total de ventas.
-Mi modelo explica el 88.5% de la variabilidad en las ventas totales (R2 = 0.885). Esto es bueno, indica que capturo gran parte de los factores que influyen en las ventas.

-En promedio, mis predicciones se desvían en aproximadamente 53.72 unidades monetarias del valor real de las ventas (MAE = 53.72). Esto da una idea de mi precisión típica.

-Sin embargo, hay margen para mejorar mi precisión. Los errores son relativamente altos, así que puedo ser afinado para reducirlos.

En pocas palabras:
Usé Random Forest porque es potente para predecir ventas, y aunque explico una buena parte de la variabilidad, puedo ser aún más preciso afinándome.

Para profundizar el análsisis de esta Base de Datos, primero sumé a la misma la "Categoría de cliente", que no se enconrtaba en la original.
Esto arrojó el siguiente resultado: que el tipo de cliente estandar consumia más que el super primium y el primium.

Luego realicé un análisis univariado y uno bivariado de lo que obtuve las siguientes conclusiones:
1) El análisis de las ventas muestra que la venta promedio por transacción es de aproximadamente 273 pesos, aunque la mediana de 42 pesos indica que la mayoría de las ventas son de menor monto. La moda en 2 pesos revela que la mayoría de las transacciones corresponden a compras de bajo valor, lo cual sugiere que los clientes realizan principalmente compras pequeñas, con algunas ventas de mayor volumen que influyen en el promedio.

2) El análisis de la cantidad de productos vendidos revela que, generalmente, los clientes compran alrededor de 3 productos por transacción. La mediana confirma que la mayoría de las compras oscilan en torno a esta cantidad, mientras que la moda indica que la compra más frecuente también es de 3 productos. Esto sugiere que el patrón habitual de compra es moderado, con la mayoría de los clientes realizando compras de tamaño similar, centradas en torno a los 3 productos.

3) El análisis de la distribución de ventas por categoría revela que en todas las categorías predominan las transacciones de bajo monto, evidenciado por la mediana cercana a cero. Sin embargo, existen outliers en cada categoría que representan transacciones excepcionalmente altas, especialmente en las categorías de Office Supplies y Technology. Esto indica que, aunque la mayoría de las ventas son moderadas o pequeñas, hay algunas operaciones de gran volumen que impactan significativamente en las cifras totales.

4) El análisis de la relación entre el tipo de cliente y la cantidad vendida por cliente muestra un coeficiente de Pearson de aproximadamente 0.0097. Este valor indica una correlación muy débil y prácticamente nula entre ambas variables, lo que sugiere que el tipo de cliente no tiene un efecto lineal significativo en la cantidad de productos que compran. Por lo tanto, otros factores probablemente influyen más en el volumen de ventas por cliente y deben considerarse para entender mejor los patrones de compra
El análisis muestra que la categoría de producto tiene una relación fuerte y positiva con el total de ventas, con un coeficiente de Pearson de aproximadamente 0.886. Este valor indica que, en general, las categorías que generan mayores ventas tienden a estar asociadas, sugiriendo que ciertas categorías son más rentables o populares. Este hallazgo puede orientar estrategias enfocadas en fortalecer esas categorías que, a su vez, impactan significativamente en los resultados globales de ventas.

5) Análisis del gráfico de dispersión entre categoría de producto y total de ventas
El gráfico muestra cómo se distribuyen las ventas totales en las diferentes categorías de productos: Technology, Office Supplies y Furniture. Se observa que:
•	La categoría Technology destaca con un punto en el extremo superior, indicando que algunas transacciones en esta categoría alcanzan niveles muy altos de ventas, significativamente por encima del resto.
•	La categoría Office Supplies presenta varios puntos en niveles bajos, sugiriendo que la mayoría de sus ventas son moderadas o pequeñas, aunque con algunos picos que elevan el valor total.
•	La categoría Furniture muestra una dispersión similar, con la mayoría de las ventas concentradas en niveles medios y algunos picos aislados en valores muy altos.
El análisis visual indica que, aunque la mayoría de las ventas en cada categoría se concentran en niveles moderados, existen algunas transacciones puntuales de gran volumen especialmente en tecnología y mobiliario, que pueden estar influyendo en los resultados totales.

6) Análisis de regresión multivariado
El análisis de regresión multivariada revela cómo distintas variables influyen en las ventas totales. Los resultados muestran que:
- La cantidad de productos vendidos tiene un impacto positivo y fuerte, con un coeficiente de aproximadamente 123.28. Esto indica que, en promedio, cada unidad adicional en la cantidad vendida incrementa las ventas totales en ese valor, manteniendo constantes las demás variables.
- En cuanto a la categoría de producto, se evidencia que:
  - La categoría Office Supplies tiene un efecto negativo en las ventas, con un coeficiente de aproximadamente -251.76, sugiriendo que, en comparación con la categoría base (posiblemente Furniture), las ventas en Office Supplies son en promedio menores.
  - La categoría Technology tiene un impacto positivo, con un coeficiente de aproximadamente 255.07, indicando que esta categoría genera ventas significativamente mayores en comparación con la categoría de referencia.
En conclusión,estos resultados sugieren que la cantidad de productos vendidos y la categoría de producto son factores clave que afectan las ventas totales. Potenciar la venta en categorías como Tecnología y gestionar estratégicamente las categorías con menor impacto, como Office Supplies, puede ser una estrategia efectiva para incrementar los ingresos.

Para profundizar el análisis de ventas totales de la empresa, utilicé dos modelos de ML aplicados a la predicción de la variable total_venta. Se utilizaron los modelos Regresión Lineal y Árbol de Decisión, evaluados mediante validación cruzada de 3 folds.
Estos fueron los resultados: 
<img width="473" height="237" alt="image" src="https://github.com/user-attachments/assets/d352a1c6-d9f7-4c85-95ce-2e34f4ccd584" />


El modelo de regresión lineal obtuvo un R² de 0,93, lo que indica que explica el 93% de la variabilidad de las ventas. Los errores medios (RMSE=214,5; MAE=116,5)
son consistentes y de baja dispersión, lo que sugiere que el modelo es estable y generaliza bien.
Eñ modelo de Árbol de Decisión, aunque muestra un MAE más bajo (64,3), su RMSE más alto (344,2) y la mayor variabilidad entre folds reflejan menor estabilidad. El R²=0,81 sugiere un desempeño correcto, pero inferior al modelo lineal. 
En Conclusión: La Regresión Lineal es el modelo más adecuado para este conjunto de datos, al ofrecer mayor capacidad explicativa, estabilidad y coherencia en las predicciones. El Árbol de Decisión podría explorarse más adelante si se incorporan variables no lineales o interacciones complejas

Tras aplicar la técnica de búsqueda aleatoria de hiperparámetros (RandomizedSearchCV) al modelo de Árbol de Decisión, se logró una mejora significativa en su desempeño. El modelo ajustado alcanzó un R² de 0,87, frente al 0,81 inicial, lo que indica una mayor capacidad para explicar las variaciones en las ventas totales. Esta optimización permitió encontrar la estructura del árbol más equilibrada —con una profundidad moderada y reglas más generales— reduciendo errores y evitando que el modelo se sobreadapte a casos puntuales.

En términos prácticos, esto significa que el modelo optimizado predice las ventas con mayor estabilidad y precisión, brindando una herramienta confiable para la toma de decisiones comerciales. Gracias al ajuste fino de sus parámetros, el modelo aprende mejor los patrones reales de compra y venta, lo que puede ayudar a proyectar ingresos, anticipar demandas y planificar estrategias de precios o promociones con mayor respaldo analítico.



