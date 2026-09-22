# 1. Comprender el problema.
**¿Quién utilizará estos datos?**

Los datos serán utilizados por el ayuntamiento.

**¿Qué decisiones se pueden tomar con ellos?**

Determinar si la calidad del aire es la correcta o no, si esta no es correcta se pueden generar alertas y planificar las medidas de movilidad.

**¿Qué diferencia hay entre una alerta inmediata y un informe histórico?**

Una alerta te avisa en el momento en el que hay un error para poder solucionarlo y un informe histórico te permite ver donde ha habido fallos durante un tiempo para poder ver así en qué lugar se generan más fallos y prevenirlos para que no vuelvan a ocurrir.

# 2. Analizar cobertura y calidad

- 1.Identifica dos problemas de calidad y explica sus consecuencias.

Lecturas congeladas, estas pueden provocar que durante las dos horas que no se han medido correctamente ya que se han repetido los datos, haya podido haber una temperatura o humidad inapropiada lo cual puede afectar a la salud de las personas.

Sensor no catalogado, esto puede provocar que se utilicen sus lecturas cuando no es un sensor correcto o que no se utilicen siendo este un sensor correcto.

- 2.Indica qué distrito necesita mayor atención y justifica tu respuesta.

El D4 ya que aún siendo el que más población tiene y teniendo mucho tráfico y actividad industrial es el segundo que menos sensores tiene por cada 100.000 habitantes.

- 3.Elige una anomalía y explica si la corregirías, la marcarías como dudosa o la excluirías.

Datos ausentes, la corregiría ya que 186 registros es un número demasiado grande de registros.

# 3.Comparar arquitecturas
| Criterio | Batch | Streaming |
| ------ | ---- | ------ |
| Rapidez para generar alertas   | Lento | Rápido |
| Coste y complejidad  | Barato  | Caro |
| Informes históricos  |    Muy adecuado | Adecuado, con más complejidad | 
| Picos de datos  |  Más picos debido a que procesa por lotes | Menos picos | 
# 4.Elaborar una recomendación

El riesgo más urgente es la ausencia de datos ya que si los análisis no estan teniendo en cuenta el pm2.5 y este está presente puede suponer un grave problema para la salud de las personas. Por lo que yo propongo el cambio a la arquitectura Batch ya que esta es más barata y genera unos informes muy adecuados. Pero esto no quita que problemas como el mantenimiento seguiría pendiente.

También tendriamos que tener en cuenta la privacidad ya que al recibir cordendas exactas de la ubicación de la gente se podrían obtener sus rutinas lo cual es muy peligroso y por ello se debería cifrar sus cordenadas antes de almacenarlas.