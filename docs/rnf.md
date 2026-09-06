# Requerimientos no funcionales

| # | Atributo | Metrica | Umbral | Condicion de carga | Verificacion | Consecuencia si no se cumple |
|---|---|---|---|---|---|---|
| 1 | Rendimiento | p95 de latencia | menor a 400 ms | 200 usuarios concurrentes | Prueba de carga | El usuario abandona la reserva |
| 2 | Disponibilidad | Uptime mensual | 99.9% | Operación normal 24/7 | Monitoreo sintético | Pérdida de agendamiento de citas urgentes |
| 3 | Seguridad | Cifrado de datos | TLS 1.3 / AES-256 | Transmisión y reposo | Auditoría de seguridad | Exposición de historial de datos médicos sensibles |

## Escenarios completos

### Escenario 1
-Fuente: Paciente en la aplicación móvil
-Estimulo: Solicita consultar disponibilidad de citas para una especialidad
-Artefacto: Módulo de Agendamiento / API Gateway
-Entorno: Hora pico (200 usuarios concurrentes)
-Respuesta: Retorna el listado de horas disponibles
-Medida: Tiempo de respuesta en el p95 menor a 400 ms