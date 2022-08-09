# Trabajo Práctico - Gestión de Datos - 2022 - 1C

Trabajo práctico grupal realizado para la materia gestión de datos en la UTN. Consistía de varias etapas en las que debíamos organizar datos que se nos fueron entregados todos juntos en una tabla Maestra. Trataba sobre telemetría en carreras de fòrmula 1. Se contaba con datos de los autos, mediciones de sus autopartes, pilotos, escuderias, carreras, circuitos, incidentes, etc.

## Modelo de Datos y Primera Migración
Comenzamos ejecutando un script que organizaba todos los datos en una tabla maestra desnormalizada y sin aparente relacion. Nuestro primer objetivo erac rear el modelo de datos, creando las tablas necesarias y sus relaciones correspondientes para que los datos cumplan las formas normales. Teniendo en cuenta el modelo de negocio, el enunciado y las diferentes entradas de la tabla maestra, organizamos los datos en 23 tablas, con sus respectivos atributos.

Luego se llevó a cabo la primera migración desde la tabla maestra hacia nuestras nuevas tablas. Todo esto mediante el **script_creacion_inicial** que crea las tablas y realiza la migración.

## Modelo BI y Segunda Migración
Se creó un nuevo modelo relacional. En este caso para aplicar en menor medida un modelo de inteligencia de negocios. Creamos 8 tablas de dimensiones que contaban con los datos necesarios para realizar los cálculos de las consultas pedidas por enunciado. Además a eso hicimos 3 tablas de hechos, ya con datos precalculados para hacer la creación final de las vistas usando estas tablas para las consultas, agrupados por dimensión según conveniencia e informacion en común. En este caso teniamos una tabla para el registro de telemetría, otra para las paradas y una última para los incidentes. La creación de tablas, sus respectivos cálculos y relaciones se realizaba mediante la ejecución de **script_creacion_BI**

## Creación de Vistas
Para finalizar en el mismo script mencionado en el punto anterior, se creaban vistas con la informacion requerida por enunciado.
