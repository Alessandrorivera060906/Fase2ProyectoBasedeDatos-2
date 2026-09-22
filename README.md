# EduGT — Fase 2

Proyecto de Bases de Datos II · Sección 02 · Universidad Rafael Landívar  
Catedrática: Ing. Diana Gutiérrez · Guatemala, 22 de septiembre de 2026

| Integrante | Carné |
| --- | --- |
| Axel Guillermo Alvarado Taracena | 1284724 |
| Diego Andrés Diaz Estupiñan | 1214024 |
| María Ínes Leiva Casiano | 1089524 |
| Javier Alessandro Rivera Lemus | 1241224 |
| Jennifer Fernanda Turcios Estrada | 1088724 |

## Antes de empezar

- Antes de ejecutar los scripts, seleccione la base de datos EduGT en la lista desplegable de SSMS.
- Ejecute cada script completo, con Ctrl + A y luego F5.

## Orden de ejecución

| # | Archivo | Qué hace |
| --- | --- | --- |
| 1 | 01_CreacionBD.sql | Crea las tablas, llaves, restricciones e índices del modelo |
| 2 | 02_Fase2Procedimientos.sql | Crea los 16 procedimientos almacenados y la vista vw_CatalogoCursos |
| 3 | 03_EduGT_Datos_Prueba.sql | Carga los datos de prueba |
| 4 | 04_Casos_de_Prueba.sql | Ejecuta las pruebas de cada procedimiento |

Tome en cuenta que el paso 3 borra toda la información de las tablas y reinicia los contadores IDENTITY antes de insertar, para que los identificadores sean idénticos en cualquier equipo.

## Datos que deja cargados el paso 3

| Rol | ID |
| --- | --- |
| Instructores | 1, 2, 3 |
| Revisores | 4, 5 |
| Administrador | 6 |
| Estudiantes | 7 al 12 |

| Curso | Estado |
| --- | --- |
| 1 y 2 | DISPONIBLE |
| 3 | PENDIENTE |
| 4 | RECHAZADO |
| 5 | ENREVISION |
| 6 | INACTIVO |
| 7 | PENDIENTE, incompleto a propósito |

## Notas

- Los casos de éxito muestran la fila modificada en la pestaña Resultados.
- Los casos de error aparecen en rojo en la pestaña Mensajes. Ese es el resultado esperado.
- Las pruebas se ejecutan en orden, porque varias dependen del estado que dejó la anterior. Para repetirlas desde cero, vuelva a ejecutar el paso 3.
