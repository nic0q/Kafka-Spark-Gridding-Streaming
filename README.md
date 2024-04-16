# Kafka - Spark Streaming
Nota: 6.5 🤑
Todo lo necesario para runnear el programa se encuentra en el mismo notebook, con sus respectivas versiones.

### Contexto
Las antenas del observatorio ALMA se ubican en el llano de Chajnantor a 4800 metros sobre el nivel
del mar, en el Desierto de Atacama. Estas antenas miden señales de radio frecuencia en longitudes
de onda milimétricas y submilimétricas. La señal capturada por las antenas, entonces, no es la luz
visible emitida por el objeto, sino la radiación que esa luz produce al interactuar con el gas y polvo
que se encuentra alrededor del objeto. Luego, es necesario transformar esta se˜nal de RF a una se˜nal
de intensidad. Este proceso se llama síntesis de imágenes.
Para ser más específicos, la señal capturada por las antenas corresponde a mediciones en el plano de
Fourier. La Figura 1 muestra una típica distribución de posiciones de muestreo en el plano uv (plano
Fourier) de una cierto objeto. Cada punto representa una medición, llamada visibilidad. Aunque no
es relevante para este lab, diremos que cada par de antenas produce una visibilidad, y a medida que
pasa el tiempo y gira la tierra, el punto se mueve en el plano uv.
(Créditos al docente que redactó el documento).

### Procedimiento
- Se utiliza Kafka para crear 1 productor con X tópicos donde cada visibilidad (En este caso son 3 millones aprox.) dependiente de su tópico le corresponderá un tópico en particular.
- Mediante sentencias SQL el consumidor realiza el gridding y operaciones correspondientes que guardará en un .csv para finalmente graficar

### Resultado con 3 millones de visibilidades
![image](https://github.com/nic0q/Kafka-Spark-Gridding-Streaming/assets/91075814/880051e0-b375-47b6-a985-77f5adc42ffe)
