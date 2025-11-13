# - Data Engineer

Solución completa de prueba técnica con SQL y PySpark

---

## Sección 1: SQL

### Ejercicio 1: Tabla Resumen Qatar 2022

**Objetivo:** Calcular puntos y diferencia de goles por equipo por cada grupo

**Resultado:**

('ALEMANIA', 'GRUPO E', 6, 0)
('ARABIA SAUDI', 'GRUPO C', 4, -3)
('ARGENTINA', 'GRUPO C', 9, 9)
('COREA DEL SUR', 'GRUPO F', 6, 3)
('COSTA RICA-NUEVA ZELANDA', 'GRUPO E', 4, 1)
('DINAMARCA', 'GRUPO D', 5, 3)
('ECUADOR', 'GRUPO A', 7, 2)
('ESPANA', 'GRUPO E', 3, 0)
('ESTADOS UNIDOS', 'GRUPO B', 1, -7)
('FRANCIA', 'GRUPO D', 2, -4)
('GHANA', 'GRUPO F', 0, -4)
('HOLANDA', 'GRUPO A', 5, 3)
('INGLATERRA', 'GRUPO B', 9, 8)
('IRAN', 'GRUPO B', 2, -4)
('JAPON', 'GRUPO E', 4, -1)
('MEXICO', 'GRUPO C', 1, -7)
('PERU-AUSTRALIA-EAU', 'GRUPO D', 5, 5)
('POLONIA', 'GRUPO C', 3, 1)
('PORTUGAL', 'GRUPO F', 7, 2)
('QATAR', 'GRUPO A', 1, -6)
('SENEGAL', 'GRUPO A', 3, 1)
('TUNEZ', 'GRUPO D', 3, -4)
('UCRANIA-ESCOCIA-GALES', 'GRUPO B', 4, 3)
('URUGUAY', 'GRUPO F', 4, -1)


---

### Ejercicio 2: Clasificados con Información de Partidos

**Objetivo:** Identificar 1º y 2º de cada grupo con fecha, hora y sede de octavos

**Resultado:**

('GRUPO A', '1º', 'ECUADOR', '03/12/2022', '06:00:00 PM', 'Estadio Khalifa, Rayán')
('GRUPO A', '2º', 'HOLANDA', '04/12/2022', '10:00:00 PM', 'Estadio Al Bayt, Jor')
('GRUPO B', '1º', 'INGLATERRA', '04/12/2022', '10:00:00 PM', 'Estadio Al Bayt, Jor')
('GRUPO B', '2º', 'UCRANIA-ESCOCIA-GALES', '03/12/2022', '06:00:00 PM', 'Estadio Khalifa, Rayán')
('GRUPO C', '1º', 'ARGENTINA', '03/12/2022', '10:00:00 PM', 'Estadio Ahmed bin Ali, Rayán')
('GRUPO C', '2º', 'ARABIA SAUDI', '04/12/2022', '06:00:00 PM', 'Estadio Al Thumama, Doha')
('GRUPO D', '1º', 'PERU-AUSTRALIA-EAU', '04/12/2022', '06:00:00 PM', 'Estadio Al Thumama, Doha')
('GRUPO D', '2º', 'DINAMARCA', '03/12/2022', '10:00:00 PM', 'Estadio Ahmed bin Ali, Rayán')
('GRUPO E', '1º', 'ALEMANIA', '05/12/2022', '06:00:00 PM', 'Estadio Al Janoub, Al Wakrah')
('GRUPO E', '2º', 'COSTA RICA-NUEVA ZELANDA', '06/12/2022', '06:00:00 PM', 'Estadio Qatar Foundation, Rayán')
('GRUPO F', '1º', 'PORTUGAL', '06/12/2022', '06:00:00 PM', 'Estadio Qatar Foundation, Rayán')
('GRUPO F', '2º', 'COREA DEL SUR', '05/12/2022', '06:00:00 PM', 'Estadio Al Janoub, Al Wakrah')


---

### Ejercicio 3: Equipos Élite (Quintil Superior)

**Objetivo:** Identificar eequipos elite

**Resultado:**

('ARGENTINA', 'GRUPO C', 9, 9)
('INGLATERRA', 'GRUPO B', 9, 8)
('ECUADOR', 'GRUPO A', 7, 2)
('PORTUGAL', 'GRUPO F', 7, 2)
('ALEMANIA', 'GRUPO E', 6, 0)



---

## Sección 2: PySpark

### Ejercicio 4: Análisis de Jugadores de Fútbol

**Objetivo:** Crear ranking por país y nuevo ranking por eficiencia (goles/partido)

**Resultado:**


================================================================================
Respuesta 2.1: DataFrame jugador
================================================================================
+-------+------------------+-----------+------------+-----------------------+
|ranking|            nombre|codigo_pais|numero_goles|numero_partidos_jugados|
+-------+------------------+-----------+------------+-----------------------+
|      1| Cristiano Ronaldo|         32|         115|                    184|
|      2|          Ali Daei|         24|         109|                    148|
|      3|    Mokhtar Dahari|         28|          89|                    142|
|      4|     Ferenc Puskás|         20|          84|                     89|
|      5|      Lionel Messi|          5|          81|                    158|
|      6|     Sunil Chhetri|         21|          80|                    125|
|      7|      Ali Mabkhout|         13|          79|                    104|
|      8|   Godfrey Chitalu|         39|          79|                    111|
|      9|     Hussein Saeed|         23|          78|                    137|
|     10|              Pelé|          8|          77|                     92|
|     11|     Sándor Kocsis|         19|          75|                     68|
|     12|Kunishige Kamamoto|         26|          75|                     76|
|     13|   Bashar Abdullah|         27|          75|                    134|
|     14|Robert Lewandowski|         31|          74|                    128|
|     15|    Majed Abdullah|          4|          72|                    117|
|     16|      Kinnah Phiri|         29|          71|                    117|
|     17|Kiatisuk Senamuang|         36|          71|                    134|
|     18|    Miroslav Klose|          1|          71|                    137|
|     19|   Piyapong Pue-on|         36|          70|                    100|
|     20|       Abdul Kadir|         22|          70|                    111|
+-------+------------------+-----------+------------+-----------------------+
only showing top 20 rows

================================================================================
Respuesta 2.2: Mejor jugador por país
================================================================================
+---------------------+---------------------------+-------+----------------+
|nombre               |nombre_pais                |ranking|es_mejor_jugador|
+---------------------+---------------------------+-------+----------------+
|Miroslav Klose       | Alemania                  |18     |true            |
|Cha Bum-Kun          | Corea del Sur             |38     |true            |
|Didier Drogba        | Costa de Marfil           |29     |true            |
|Hossam Hassan        | Egipto                    |27     |true            |
|Ali Mabkhout         | Emiratos Arabes Unidos    |7      |true            |
|David Villa          | España                    |37     |true            |
|Clint Dempsey        | Estados Unidos            |41     |true            |
|Landon Donovan       | Estados Unidos            |43     |false           |
|Abdul Ghani Minhat   | Federación Malaya/ Malasia|34     |true            |
|Carlos Ruiz Gutiérrez| Guatemala                 |25     |true            |
+---------------------+---------------------------+-------+----------------+
only showing top 10 rows


================================================================================
Respuesta 2.3: Comparación de rankings (por eficiencia)
================================================================================
+---------------------+---------------------------+-----------------+----------------+------------------+
|nombre               |nombre_pais                |goles_por_partido|num_ranking_pais|nuevo_ranking_pais|
+---------------------+---------------------------+-----------------+----------------+------------------+
|Miroslav Klose       | Alemania                  |0.518            |1               |1                 |
|Cha Bum-Kun          | Corea del Sur             |0.43             |1               |1                 |
|Didier Drogba        | Costa de Marfil           |0.619            |1               |1                 |
|Hossam Hassan        | Egipto                    |0.386            |1               |1                 |
|Ali Mabkhout         | Emiratos Arabes Unidos    |0.76             |1               |1                 |
|David Villa          | España                    |0.602            |1               |1                 |
|Clint Dempsey        | Estados Unidos            |0.404            |1               |1                 |
|Landon Donovan       | Estados Unidos            |0.363            |2               |2                 |
|Abdul Ghani Minhat   | Federación Malaya/ Malasia|0.859            |1               |1                 |
|Carlos Ruiz Gutiérrez| Guatemala                 |0.511            |1               |1                 |
|Carlos Pavón         | Honduras                  |0.564            |1               |1                 |
|Sándor Kocsis        | Hungría                   |1.103            |1               |1                 |
|Imre Schlosser       | Hungría                   |0.868            |2               |2                 |
|Gerd Müller          | Alemania Federal          |1.097            |1               |1                 |
|Ferenc Puskás        | Hungría/ España           |0.944            |1               |1                 |
+---------------------+---------------------------+-----------------+----------------+------------------+
only showing top 15 rows


 Sí, el resultado cambió: 6 jugadores cambiaron de posición.

Jugadores que cambiaron de posición:
+------------------+-----------+----------------+------------------+-----------------+
|nombre            |nombre_pais|num_ranking_pais|nuevo_ranking_pais|goles_por_partido|
+------------------+-----------+----------------+------------------+-----------------+
|Romário           | Brasil    |4               |2                 |0.786            |
|Neymar            | Brasil    |2               |4                 |0.603            |
|Jasem Al-Huwaidi  | Kuwait    |2               |1                 |0.759            |
|Bashar Abdullah   | Kuwait    |1               |2                 |0.56             |
|Piyapong Pue-on   | Tailandia |2               |1                 |0.7              |
|Kiatisuk Senamuang| Tailandia |1               |2                 |0.53             |
+------------------+-----------+----------------+------------------+-----------------+


================================================================================
Estructura JSON por país (todos los jugadores):
================================================================================
+-----------+-----------------------+------------------------+
|CODIGO_PAIS|NOMBRE_PAIS            |JUGADORES_ESTRELLA      |
+-----------+-----------------------+------------------------+
|1          | Alemania              |[{Miroslav Klose, 1, 1}]|
|10         | Corea del Sur         |[{Cha Bum-Kun, 1, 1}]   |
|11         | Costa de Marfil       |[{Didier Drogba, 1, 1}] |
|12         | Egipto                |[{Hossam Hassan, 1, 1}] |
|13         | Emiratos Arabes Unidos|[{Ali Mabkhout, 1, 1}]  |
+-----------+-----------------------+------------------------+
only showing top 5 rows


✓ JSON exportado a: /tmp/jugadores_resultado_final.json


---

### Ejercicio 5: Centros Educativos - UDF y Distancia Euclidiana

**Objetivo:** Analisis centros educativos Madrid

**Resultado:**
+-------------+------------------+------------------+--------------------------+----------------------------------------------------+-------------------+------------------+-------------------------------------------+------------+------------------+------------------+------------------+------------------+------------------------------------------------------+----------+-----------+-----------------------+----------------+----------------+----------------+---------------------+------------------+---------------+---------------+----------------+-----------------+
|centro_codigo|centro_nombre     |centro_tipo_codigo|centro_tipo_desc_abreviada|centro_tipo_descripcion                             |centro_titular     |centro_titularidad|contacto_email1                            |contacto_fax|contacto_telefono1|contacto_telefono2|contacto_telefono3|contacto_telefono4|contacto_web                                          |dat_codigo|dat_nombre |direccion_codigo_postal|direccion_coor_x|direccion_coor_y|direccion_numero|direccion_via_nombre |direccion_via_tipo|distrito_codigo|distrito_nombre|municipio_codigo|municipio_nombre |
+-------------+------------------+------------------+--------------------------+----------------------------------------------------+-------------------+------------------+-------------------------------------------+------------+------------------+------------------+------------------+------------------+------------------------------------------------------+----------+-----------+-----------------------+----------------+----------------+----------------+---------------------+------------------+---------------+---------------+----------------+-----------------+
|28000029     |SAN BLAS          |070               |CP INF-PRI-SEC            |COLEGIO DE EDUCACIÓN INFANTIL, PRIMARIA Y SECUNDARIA|COMUNIDAD DE MADRID|PÚBLICO           |cp.sanblas.ajalvir@educa.madrid.org        |918844211   |918844589         |                  |                  |                  |http://www.educa.madrid.org/cp.sanblas.ajalvir        |3         |Madrid-Este|28864                  |458832          |4487797         |s/n             |Víctor Hurtado       |CALLE             |               |               |002             |Ajalvir          |
|28000042     |EL ALAMO          |014               |CP INF-PRI                |COLEGIO DE EDUCACIÓN INFANTIL Y PRIMARIA            |COMUNIDAD DE MADRID|PÚBLICO           |cp.elalamo.elalamo@educa.madrid.org        |918122834   |918120652         |                  |                  |                  |http://www.educa.madrid.org/cp.elalamo.elalamo        |2         |Madrid-Sur |28607                  |415961          |4453703         |1               |del Río Alagón       |CALLE             |               |               |004             |Álamo, El        |
|28000054     |ANTONIO DE NEBRIJA|014               |CP INF-PRI                |COLEGIO DE EDUCACIÓN INFANTIL Y PRIMARIA            |COMUNIDAD DE MADRID|PÚBLICO           |cp.antoniodenebrija.alcala@educa.madrid.org|918882368   |918882368         |                  |                  |                  |http://www.educa.madrid.org/cp.antoniodenebrija.alcala|3         |Madrid-Este|28806                  |468386          |4482313         |13              |San Ignacio de Loyola|CALLE             |               |               |005             |Alcalá de Henares|
|28000066     |CARDENAL CISNEROS |014               |CP INF-PRI                |COLEGIO DE EDUCACIÓN INFANTIL Y PRIMARIA            |COMUNIDAD DE MADRID|PÚBLICO           |cp.cardenalcisnero.alcala@educa.madrid.org |918837578   |918880447         |615303251         |                  |                  |http://www.educa.madrid.org/cp.cardenalcisnero.alcala |3         |Madrid-Este|28801                  |468658          |4481259         |2               |San Juan             |CALLE             |               |               |005             |Alcalá de Henares|
|28000078     |CERVANTES         |014               |CP INF-PRI                |COLEGIO DE EDUCACIÓN INFANTIL Y PRIMARIA            |COMUNIDAD DE MADRID|PÚBLICO           |cp.cervantes.alcala@educa.madrid.org       |918816276   |918889973         |                  |                  |                  |http://www.educa.madrid.org/cp.cervantes.alcala       |3         |Madrid-Este|28800                  |469547          |4481511         |5               |Giner de los Ríos    |CALLE             |               |               |005             |Alcalá de Henares|
+-------------+------------------+------------------+--------------------------+----------------------------------------------------+-------------------+------------------+-------------------------------------------+------------+------------------+------------------+------------------+------------------+------------------------------------------------------+----------+-----------+-----------------------+----------------+----------------+----------------+---------------------+------------------+---------------+---------------+----------------+-----------------+
only showing top 5 rows


================================================================================
5.2.1: Promedio de coordenadas por titularidad
================================================================================
+--------------------+-----------------+-----------------+
|  centro_titularidad|       promedio_x|       promedio_y|
+--------------------+-----------------+-----------------+
|             PÚBLICO|440157.3842874543|4474481.943970768|
|             PRIVADO|439602.9362934363|4476838.754826255|
|  PRIVADO CONCERTADO|440264.7489361702|4474293.580851064|
|PÚBLICO-TITULARID...|         438924.0|        4479147.0|
+--------------------+-----------------+-----------------+


================================================================================
5.2.2: UDF para distancia euclidiana
================================================================================
Centros con distancia al centroide de su grupo:
+-----------------------------+------------------+----------------+----------------+-----------------+-----------------+----------------------+
|centro_nombre                |centro_titularidad|direccion_coor_x|direccion_coor_y|promedio_x       |promedio_y       |distancia_al_centroide|
+-----------------------------+------------------+----------------+----------------+-----------------+-----------------+----------------------+
|SAN BLAS                     |PÚBLICO           |458832          |4487797         |440157.3842874543|4474481.943970768|22935.39              |
|EL ALAMO                     |PÚBLICO           |415961          |4453703         |440157.3842874543|4474481.943970768|31894.04              |
|ANTONIO DE NEBRIJA           |PÚBLICO           |468386          |4482313         |440157.3842874543|4474481.943970768|29294.71              |
|CARDENAL CISNEROS            |PÚBLICO           |468658          |4481259         |440157.3842874543|4474481.943970768|29295.28              |
|CERVANTES                    |PÚBLICO           |469547          |4481511         |440157.3842874543|4474481.943970768|30218.49              |
|DAOIZ Y VELARDE              |PÚBLICO           |468826          |4481956         |440157.3842874543|4474481.943970768|29626.86              |
|SAGRADO CORAZON DE JESUS     |PRIVADO CONCERTADO|468895          |4481221         |440264.7489361702|4474293.580851064|29456.42              |
|SAN FELIPE NERI              |PRIVADO CONCERTADO|468721          |4481288         |440264.7489361702|4474293.580851064|29303.24              |
|ESCUELAS PIAS                |PRIVADO CONCERTADO|470018          |4481495         |440264.7489361702|4474293.580851064|30612.36              |
|EMPERADOR FERNANDO           |PÚBLICO           |468369          |4480180         |440157.3842874543|4474481.943970768|28781.3               |
|SANTA MARIA DE LA PROVIDENCIA|PRIVADO CONCERTADO|469022          |4482033         |440264.7489361702|4474293.580851064|29780.5               |
|COMPLUTENSE                  |PÚBLICO           |470510          |4481599         |440157.3842874543|4474481.943970768|31175.85              |
|NUESTRA SEÑORA DEL VAL       |PÚBLICO           |470873          |4481791         |440157.3842874543|4474481.943970768|31573.27              |
|DOCTORA DE ALCALA            |PÚBLICO           |469522          |4482291         |440157.3842874543|4474481.943970768|30385.23              |
|SAN GABRIEL                  |PRIVADO CONCERTADO|467137          |4483263         |440264.7489361702|4474293.580851064|28329.64              |
|SAN IGNACIO DE LOYOLA        |PRIVADO CONCERTADO|469041          |4482916         |440264.7489361702|4474293.580851064|30040.29              |
|MINERVA                      |PRIVADO CONCERTADO|469753          |4481732         |440264.7489361702|4474293.580851064|30411.96              |
|ALONSO DE AVELLANEDA         |PÚBLICO           |471046          |4482286         |440157.3842874543|4474481.943970768|31859.22              |
|CALASANZ                     |PRIVADO CONCERTADO|468941          |4481493         |440264.7489361702|4474293.580851064|29566.18              |
|LOPE DE VEGA                 |PRIVADO CONCERTADO|469744          |4482228         |440264.7489361702|4474293.580851064|30528.37              |
+-----------------------------+------------------+----------------+----------------+-----------------+-----------------+----------------------+
only showing top 20 rows


================================================================================
5.2.3: Centro más céntrico por titularidad
================================================================================
Centro elegido como punto de reunión por cada titularidad:
+---------------------------+--------------------------------------------------------------------+----------------------+----------------+----------------+
|centro_titularidad         |centro_nombre                                                       |distancia_al_centroide|direccion_coor_x|direccion_coor_y|
+---------------------------+--------------------------------------------------------------------+----------------------+----------------+----------------+
|PRIVADO                    |INSTITUTO VOX                                                       |121.2                 |439513          |4476920         |
|PRIVADO CONCERTADO         |TEIDE II                                                            |448.71                |439841          |4474146         |
|PÚBLICO                    |SANTA TERESA DE JESUS                                               |444.01                |439759          |4474678         |
|PÚBLICO-TITULARIDAD PRIVADA|ESCUELA DE FORMACION ESPEC. IMAGEN DIAG. HOSPITAL CLINICO SAN CARLOS|2318.46               |438970          |4476829         |
+---------------------------+--------------------------------------------------------------------+----------------------+----------------+----------------+



---

### Ejercicio 6: Exportación Multi-formato y Justificación

**Objetivo:** Exportar datos en 3 formatos y justificar el mejor para big data

**Archivos Generados:**

```
/tmp/
├── centros_educativos.parquet  
├── centros_educativos.json     
└── centros_educativos.csv      
```



**Recomendación para Databricks: PARQUET**

**Ventajas:**
-  Almacenamiento columnar 
-  Compresión eficiente 
-  Formato nativo de Spark
-  Preserva tipos de datos y metadatos

**Por qué NO CSV:**
- ❌ Almacenamiento por filas (ineficiente)
- ❌ Sin compresión
- ❌ 5-10x más grande que Parquet
- ❌ Lee todos los datos siempre

**Por qué NO JSON:**
- ❌ 3-5x más grande que Parquet
- ❌ Parseo costoso
- ❌ Sin optimizaciones Spark


---

## Autor

**Harold**
- Data Engineer 
