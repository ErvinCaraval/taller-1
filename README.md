# Juego de Preguntas Multijugador 

## Descripción General
Este proyecto consiste en un MVP de un juego multijugador en el que los participantes compiten respondiendo preguntas en tiempo real. El sistema cuenta con un encargado de crear y gestionar las preguntas, incluyendo sus opciones de respuesta y la solución correcta. Para el almacenamiento de usuarios, partidas y preguntas se utilizará una base de datos no relacional, lo que garantiza escalabilidad, flexibilidad y un manejo eficiente de la información en entornos dinámicos.

## Propósito
- Gamificar el aprendizaje y el entretenimiento.
- Demostrar el uso de IA en el desarrollo ágil con Scrum.
- Aplicar bases de datos no relacionales para escalabilidad.

## Audiencia Objetivo
- Público general

## Funcionalidades Principales
- Registro y autenticación de usuarios.
- Creación y unión a partidas multijugador.
- Generación dinámica de preguntas.
- Almacenamiento de datos en una base no relacional (Firebase).
- Sistema de puntuación y ranking.
- Retroalimentación.
- Panel de administración para agregar/modificar preguntas.
- Historial de partidas y estadísticas personales.

## Historias de Usuario (Formato Connextra)
1. Como usuario nuevo, quiero registrarme para poder participar en partidas.
2. Como jugador, quiero unirme a partidas multijugador para competir con otros.
3. Como jugador, quiero responder preguntas para probar mis conocimientos.
4. Como sistema, quiero almacenar preguntas y partidas en una base de datos no relacional para escalabilidad.
5. Como usuario, quiero ver mi historial y estadísticas para medir mi progreso.
6. Como administrador, quiero agregar/modificar preguntas para mantener el juego actualizado.
7. Como jugador, quiero ver el ranking en tiempo real para saber mi posición.
8. Como usuario, quiero recibir retroalimentación después de las respuestas.
9. Como jugador, quiero invitar amigos a partidas privadas.
10. Como usuario, quiero recuperar mi contraseña si la olvido.
11. Como jugador, quiero filtrar preguntas por categorías.
12. Como jugador, quiero ver el tiempo restante para responder cada pregunta.
13. Como jugador, quiero ver el resumen de la partida al finalizar.

## Product Backlog y Release Plan

## Product Backlog Inteligente

### Leyenda
- 🧠 = Historia implementada con IA
- 📝 = Historia implementada sin IA


### Historias de Usuario Detalladas

| ID | Historia | Descripción | Prioridad | Estimación | Dependencias | Criterios de aceptación | Pruebas sugeridas | IA |
|----|----------|-------------|-----------|------------|--------------|------------------------|-------------------|----|
| 1 | Como usuario nuevo, quiero registrarme para poder participar en partidas. | Permitir que nuevos usuarios creen una cuenta. | Alta | 2 pts | Ninguna | - El usuario puede registrarse con email y contraseña.<br>- El email no está repetido.<br>- Se envía confirmación de registro.<br>- El registro es seguro y cumple RGPD. | - Intentar registrar con email existente (debe fallar).<br>- Registrar usuario nuevo (debe funcionar). | 📝 |
| 2 | Como jugador, quiero iniciar sesión para acceder a mis partidas. | Permitir que los usuarios inicien sesión. | Alta | 2 pts | 1 | - El usuario puede iniciar sesión con email y contraseña.<br>- Se valida credenciales.<br>- Sesión segura y persistente. | - Iniciar sesión con credenciales incorrectas (debe fallar).<br>- Iniciar sesión con credenciales correctas (debe funcionar). | 📝 |
| 3 | Como jugador, quiero crear y unirme a partidas multijugador para competir con otros. | Permitir que los usuarios creen partidas y se unan otros jugadores. | Alta | 3 pts | 2 | - El usuario puede crear una partida.<br>- Otros usuarios pueden unirse.<br>- Se gestiona el estado de la partida. | - Crear partida y verificar que otros pueden unirse.<br>- Simular flujo de partida. | 📝 |
| 4 | Como jugador, quiero responder preguntas para probar mis conocimientos. | Consumir preguntas almacenadas en la base de datos que fueron creadas por el administrador. | Alta | 5 pts | 3 | - El jugador recibe preguntas con sus opciones de respuesta. <br>- Se valida la respuesta seleccionada y se informa si es correcta o incorrecta. <br>- Las preguntas provienen del banco gestionado por el administrador. | - El sistema muestre una pregunta con sus opciones al iniciar la partida..<br>-Confirmar que, al responder, el sistema indique si fue correcta o incorrectad. | 🧠 |
| 5 | Como sistema, quiero almacenar usuarios, partidas y preguntas en Firebase para escalabilidad. | Guardar usuarios, partidas y preguntas en Firebase. | Alta | 3 pts | 1,3,4 | - Los datos se guardan y recuperan correctamente.<br>- Integridad y consistencia de datos.<br>- Escalabilidad comprobada. | - Crear, leer, actualizar y borrar datos.<br>- Pruebas de carga. | 📝 |
| 6 | Como jugador, quiero ver mi historial y estadísticas para medir mi progreso. | Mostrar a los usuarios su historial y estadísticas. | Media | 2 pts | 2,5 | - El usuario puede ver partidas jugadas y estadísticas.<br>- Datos actualizados en tiempo real.<br>- Visualización clara. | - Jugar partidas y verificar historial.<br>- Validar estadísticas. | 📝 |
| 7 | Como administrador, quiero agregar/modificar preguntas para mantener el juego actualizado. | Permitir a administradores agregar/modificar preguntas manualmente. | Media | 2 pts | 5 | - El administrador puede crear, editar y borrar preguntas.<br>- Validación de contenido.<br>- Cambios reflejados en el juego. | - Agregar y modificar preguntas desde el panel.<br>- Verificar actualización en partidas. | 📝 |
| 8 | Como jugador, quiero ver el ranking en tiempo real para saber mi posición. | Calcular y mostrar puntajes y posiciones de los jugadores. | Media | 2 pts | 3,5 | - El sistema actualiza puntajes en tiempo real.<br>- El ranking se muestra correctamente.<br>- Actualización automática. | - Simular partidas y verificar ranking.<br>- Validar actualización. | 📝 |
| 9 | Como usuario, quiero recibir retroalimentación después de las respuestas. | Dar feedback inmediato sobre respuestas correctas/incorrectas. | Media | 3 pts | 4 | - El sistema explica por qué una respuesta es correcta o incorrecta.<br>- Feedback relevante y claro.<br>- Las explicaciones se guardan en la base de datos al crear la pregunta. | - Responder preguntas y verificar feedback.<br>- Validar explicaciones. | 🧠 |
| 10 | Como jugador, quiero invitar amigos a partidas privadas. | Permitir invitar amigos a partidas privadas. | Baja | 2 pts | 3 | - El usuario puede invitar amigos.<br>- Invitación por enlace o email.<br>- Acceso seguro. | - Invitar y verificar acceso.<br>- Validar privacidad. | 📝 |
| 11 | Como usuario, quiero recuperar mi contraseña si la olvido. | Permitir a los usuarios recuperar su contraseña. | Baja | 1 pt | 1 | - El usuario puede solicitar recuperación.<br>- Recibe instrucciones por email.<br>- Seguridad en el proceso. | - Solicitar recuperación y verificar email recibido.<br>- Intentar recuperación con email no registrado. | 📝 |
| 12 | Como jugador, quiero filtrar preguntas por categorías. | Filtrar preguntas según intereses del usuario. | Baja | 2 pts | 4 | - El sistema sugiere categorías relevantes.<br>- Filtrado eficiente.<br>- Personalización por usuario. | - Seleccionar intereses y verificar sugerencias.<br>- Validar filtrado. | 🧠 |
| 13 | Como jugador, quiero ver el tiempo restante para responder cada pregunta. | Mostrar tiempo restante para cada pregunta. | Baja | 1 pt | 3 | - El usuario ve un temporizador en cada pregunta.<br>- Temporizador preciso.<br>- Notificación al finalizar tiempo. | - Verificar temporizador en la interfaz.<br>- Simular expiración de tiempo. | 📝 |
| 14 | Como jugador, quiero ver el resumen de la partida al finalizar. | Mostrar resumen de resultados al terminar la partida. | Baja | 1 pt | 3,8 | - El usuario ve puntajes, respuestas y ranking final.<br>- Resumen claro y completo.<br>- Acceso al historial. | - Finalizar partida y verificar resumen.<br>- Validar acceso al historial. | 📝 |

---

## Release Plan Detallado


### Día 0: 16 de septiembre de 2025 (Inicio del equipo)

**Sprint 1 (16-18 sept):**
- Registro y autenticación de usuarios (ID 1,2)
- Almacenamiento en base de datos no relacional (ID 5)

**Sprint 2 (19-22 sept):**
- Creación y unión a partidas multijugador (ID 3)
- Generación dinámica de preguntas usando IA (ID 4)

**Sprint 3 (23-25 sept):**
- Panel de administración para preguntas (ID 7)
- Sistema de puntuación y ranking (ID 8)
- Historial de partidas y estadísticas personales (ID 6)

**Sprint 4 (26-28 sept):**
- Retroalimentación automática sobre respuestas (IA) (ID 9)
- Filtrado inteligente de preguntas por categorías (IA) (ID 12)
- Revisión de reportes de preguntas inapropiadas (ID 13)

**Sprint 5 (29-30 sept):**
- Invitar amigos a partidas privadas (ID 10)
- Recuperación de contraseña (ID 11)
- Tiempo límite para responder preguntas (ID 14)
- Resumen de partida al finalizar (ID 15)
- Resumen de partida al finalizar (ID 15)
- Pruebas finales, integración, mejoras y documentación

**Entrega final:** 30 de septiembre de 2025
---

## Uso de IA en el Proceso
- Generación y refinamiento de historias de usuario.
- Sugerencia de tareas técnicas y prompts para desarrollo.
- Documentación de cada interacción con IA (prompts, respuestas, tiempo, valor añadido).

## Documentación y Evaluación
- Registrar todos los prompts y respuestas de IA.
- Documentar el diseño, decisiones técnicas y lecciones aprendidas.
- Entregar el MVP funcional y la documentación en el repositorio.

## Ejemplo de Prompt para IA
> Actúa como Product Owner experto en juegos educativos. Genera un Product Backlog para un juego de preguntas multijugador, usando base de datos no relacional y funcionalidades de IA. Prioriza las historias y estima el esfuerzo en puntos de historia.

## Tecnologías Sugeridas
- Backend: Node.js, Python o similar
- Base de datos: MongoDB, Firebase
- Frontend: React, Vue, Angular
- IA: OpenAI API, Gemini, Copilot

## Estructura Recomendada del Proyecto
- `src/` — código fuente (backend, frontend)
- `tests/` — pruebas automatizadas
- `docs/` — documentación, prompts, artefactos de planificación

## Referencias
- Ver `deepseek_markdown_20250913_cef725.md` para guía Scrum, ingeniería de prompts y requisitos.

---
Última actualización: 2025-09-13
