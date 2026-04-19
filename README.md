# Desempe-o
Logitrans Eventos

Descripcion General del Proyecto: 
"LogiTrans es un sistema de gestión logística diseñado para registrar envíos, asignar rutas óptimas, verificar disponibilidad de conductores y vehículos, y analizar estadísticas de tiempos, costos e incidencias. El proyecto busca optimizar la operación de transporte y brindar información clara para la toma de decisiones."

Instrucciones de uso:
1. Ejecutar el script en MySQL para crear las tablas, vistas y procedimientos, es importante esta nueva creacion dado que se 
añadieron campos para poder ejecutar de una manera mas completa los eventos.
2. Insertar los seeders.
3. Activar el programador global de eventos (SET GLOBAL event_scheduler = ON;)
4. Copia y ejecuta cada script:
- EVT_ActualizarEstimacionesEntrega
- EVT_VerificarDocumentacionFlota
- EVT_OptimizarRutasDiarias
- EVT_GenerarReporteFuelConsumption,
- EVT_MonitorearDesviacionesRuta).
Cada evento queda registrado en la base de datos y se ejecutará automáticamente segun la programacion definida.
5. abajo de cada script esta el select indicado para revisar si el procedimiento se esta ejecutando debidamente, tambien 
se puede ejecutar mediante 'SELECT * FROM auditoria_eventos ORDER BY fecha_ejecucion DESC;' que fue una tabla creada exclusivamente
para revisar la ejecucion de los eventos en el tiempo programado.
