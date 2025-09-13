# Proyecto Integrador II
**Mauricio Gaona**  
mauricio.gaona@correounivalle.edu.co  
Profesor  
Facultad de Ingeniería  
Escuela de Ingeniería de Sistemas y Computación  
2025-II

---

## Scrum con ingeniería de software aumentada con IA

El propósito de incluir inteligencia artificial en cada etapa del proceso de la metodología Scrum es potenciar la productividad, la calidad y la toma de decisiones del equipo, actuando como un apoyo constante en todo el ciclo de desarrollo ágil.

---

### Artículo corto:

**Potenciando Scrum: IA para Scrum Masters y Product Owners**  
Por Vanessa Amaya & ChatGPT  
https://scrum.mx/informate/2024/2/26/potenciando-scrum-ia-para-scrum-masters-y-product-owners

---

**INTELIGENCIA ARTIFICIAL PARA SCRUM MASTERS**
- Automatizar procesos y tareas repetitivas
- Resolución de conflictos
- Diseño de Retrospectivas
- Reforzar apoyo a Product Owners
- Modelado de escenarios y predicciones sobre Scrum en su equipo
- Identificar oportunidades de mejora

---

## La ingeniería del prompt (Prompt Engineering)

También conocida como "Promptgramming", es una práctica emergente en el campo de la inteligencia artificial (IA) que se enfoca en la creación y optimización de instrucciones para guiar a los LLMs para producir resultados útiles.

### Objetivos de Promptgramming

1. **Precisión y Relevancia**: Desarrollar prompts que conduzcan a respuestas precisas y relevantes.
2. **Eficiencia**: Minimizar la cantidad de iteraciones necesarias para obtener resultados satisfactorios.
3. **Adaptabilidad**: Crear prompts que sean versátiles y puedan ajustarse a diversos contextos y necesidades.

---

## Elementos clave para escribir Prompts de manera efectiva

| Elemento | Descripción | Prioridad |
|----------|-------------|-----------|
| Tarea y Objetivo | Definición clara de la tarea y el objetivo deseado. | Obligatorio |
| Contexto | Información de fondo relevante para la solicitud. | Opcional pero es muy importante |
| Ejemplos | Ilustraciones de salidas esperadas. | Importante |
| Experto | Personalidad o rol que el sistema debe adoptar. | Opcional, pero altamente recomendado |
| Formato y Longitud | Especificación de la estructura y extensión de la respuesta. | Opcional |
| Tono de Voz | Estilo de comunicación deseado (formal, informal, etc.). | Opcional |
| Audiencia | Público objetivo al que se dirige la respuesta. | Opcional |

Los elementos clave para escribir prompts se estructuran como una plantilla.

---

## Ejemplos

### Ejemplo 1:
**Prompt:**  
Actúa con la personalidad de un experto en redacción académica y normas APA.  
Redactar un resumen crítico de un artículo científico sobre Inteligencia Artificial aplicada en educación, con un máximo de 300 palabras.

El estilo de escritura es formal y técnico, dirigido a estudiantes universitarios en ingeniería de sistemas.

Debes tener en cuenta el siguiente contexto: “El artículo analiza cómo la IA se está utilizando en procesos de tutoría inteligente y personalización del aprendizaje en universidades latinoamericanas.”

Sigue el siguiente ejemplo de contenido: “El texto debe contener título, introducción, análisis crítico y conclusiones, con referencias APA al final.”

### Ejemplo 2:
**Prompt:**  
Actúa con la personalidad de un Product Owner experto en plataformas educativas digitales.  
Genera un Product Backlog inicial para una plataforma de e-learning con al menos 10 historias de usuario en formato Connextra.

El estilo de escritura debe ser claro, técnico y orientado a la usabilidad, dirigido a un equipo de desarrollo de software y diseñadores UX/UI.

Debes tener en cuenta el siguiente contexto: “La plataforma debe permitir a estudiantes registrarse, acceder a cursos en video, realizar evaluaciones en línea, recibir retroalimentación automática y obtener certificados digitales. Los instructores deben poder subir contenidos, crear cuestionarios y hacer seguimiento al progreso de los estudiantes.”

Sigue el siguiente ejemplo de contenido: “Cada historia de usuario debe incluir el actor, la tarea y el propósito; además, deben estar priorizadas según la siguiente escala (Alta, Media, Baja) y contar con al menos un cinco criterios de aceptación por historia.”

---

## Ejemplo práctico: App de venta de flores en línea

**Necesidad del cliente:**  
“Quiero que los usuarios puedan registrarse, ver el catálogo de flores y comprar con tarjeta de crédito o débito”.

**Historia de Usuario generada por IA:**  
- Como usuario registrado deseo ver el catálogo de flores y pagar con tarjeta de crédito o débito para comprar de manera rápida y segura desde la app.

**Lo que pasó aquí:** La IA generativa tomó la frase del cliente y la convirtió en una HU lista para Product Backlog.

Para un resultado más completo, se requiere participación del Cliente, Product Owner y el equipo de desarrollo. Se podría proponer que haga un proceso más completo como:
- Dividir la necesidad en varias HU más detalladas
- Realizar una priorización de las HU generadas
- Detectar ambigüedades o cosas que faltan
- Estimación de esfuerzo (puntos historia)
- etc

No queremos que la IA sea solo un copiloto, sino también un pensador estratégico (copilot y co-thinker).

---

## Prompt avanzado para análisis de requisitos

Se le solicita a la IA que cree un prompt que incluya estos conceptos usando la plantilla provista.

### Experto
Actúa con la personalidad de un Product Owner experto en metodologías ágiles y en ventas por internet.

### Tarea y Objetivo:
Generar un análisis avanzado de requisitos en formato ágil a partir de una solicitud en lenguaje natural, descomponiéndola en Historias de Usuario, priorizándolas, detectando ambigüedades y estimando esfuerzo en puntos de historia.

### Contexto:
El cliente ha solicitado: "Quiero que los usuarios puedan registrarse, ver el catálogo de flores y comprar con tarjeta de crédito o débito."
Se requiere aplicar un enfoque que apoye la fase de requisitos.

### Ejemplos:
Salida esperada organizada con:  
ID  
Historia de Usuario (Usando el formato de Connextra)  
Prioridad (Alta/Media/Baja)  
Ambigüedades detectadas  
Estimación (puntos historia)

Además, se debe incluir un resumen de dependencias y recomendaciones para planificación.

### Formato y Longitud:
Respuesta estructurada como un **resumen narrativo** (2 a 4 párrafos para cada item).  

Items:  
1. Realizar un análisis semántico y dividir el requisito en varias Historias de Usuario (HU).  
2. Indicar la priorización automática de las HU, explicando la lógica de la priorización.  
3. Detectar ambigüedades en los requisitos y formular las preguntas que deberían hacerse al cliente.  
4. Estimar el esfuerzo en puntos de historia (Scrum) para cada HU.  

### Tono de Voz:
Formal, técnico, orientado a equipos de desarrollo ágil.  

### Audiencia:
Equipo de desarrollo de software Product Owner, Scrum Team y Stakeholders.

---

## Análisis completo del ejemplo de la app de flores

### Análisis Semántico
He procesado la frase "Quiero que los usuarios puedan registrarse, ver el catálogo de flores y comprar con tarjeta de crédito o débito" para descomponerla en las siguientes **Historias de Usuario (HU)**:

- **HU 1: Registro de Usuario**
  - Como usuario nuevo, **quiero** poder crear una cuenta, **para así** acceder a las funcionalidades de compra.
- **HU 2: Navegación del Catálogo**
  - Como usuario, **quiero** poder ver y explorar un catálogo de flores con sus detalles, **para así** elegir las que deseo comprar.
- **HU 3: Compra con Tarjeta**
  - Como usuario registrado, **quiero** poder pagar mi pedido utilizando una tarjeta de crédito o débito, **para así** completar mi compra de manera segura.

### Priorización Automática
Se ha aplicado un modelo de priorización automático basado en una la escala (Alta, Media y Baja) y la dependencia funcional entre las historias:

- **HU 1: Registro de Usuario: Prioridad alta.** El registro es un **habilitador** para las otras funcionalidades.
- **HU 2: Navegación del Catálogo: Prioridad alta.** Ver el catálogo es una **funcionalidad crítica de valor**.
- **HU 3: Compra con Tarjeta: Prioridad alta.** Es el **objetivo de negocio final**, que genera ingresos.

La lógica de priorización es que las tres historias son **críticas para la App**.

### Detección de Ambigüedades
Se ha identificado varias ambigüedades y vacíos en los requisitos iniciales:

- **Sobre el registro de usuario:**
  - ¿Qué información de usuario se necesita para el registro?
  - ¿Se requiere verificación de correo electrónico?
  - ¿Cómo manejamos la recuperación de contraseña?

- **Sobre el catálogo de flores:**
  - ¿Qué detalles de las flores deben mostrarse?
  - ¿Los usuarios pueden filtrar o buscar flores por criterios específicos?
  - ¿El inventario debe ser dinámico y reflejar la disponibilidad real?

- **Sobre la compra con tarjeta:**
  - ¿Qué pasarela de pagos se utilizará?
  - ¿Se necesita guardar la información de la tarjeta para futuras compras?
  - ¿Cómo se maneja el envío o la entrega?

### Estimación de Esfuerzo
Utilizando un modelo de estimación ágil (Story Points):

- **HU 1: Registro de Usuario: 3 Puntos de Historia.**
- **HU 2: Navegación del Catálogo: 5 Puntos de Historia.**
- **HU 3: Compra con Tarjeta: 8 Puntos de Historia.**

Estas estimaciones son un punto de partida y deberán ser revisadas por el equipo de desarrollo.

---

## Taller 1: Desarrollo de un MVP Usando Ingeniería de Software Aumentada con IA en el Marco de la metodología ágil Scrum

### Objetivo del Taller:
Desarrollar de un Producto Mínimo Viable (MVP) aplicando la metodología ágil Scrum, potenciando cada fase del proyecto con herramientas de Inteligencia Artificial (IA) como ChatGPT, Gemini, Cloude, Copilot, Jira, entre otras.

### Duración:
(3 semanas) Fecha de entrega Septiembre 30 de 2025.

### Requisitos Previos:
- Conocimientos básicos de metodologías ágiles (Scrum).
- Experiencia previa en programación y desarrollo de software.
- Cuenta activa en herramientas de IA.

### Conceptualización y Planificación del Proyecto

#### 1. Idea:
- Proponer una idea para el desarrollo de un MVP usando IA en cada etapa del proceso.

#### 2. Presentación de Propuestas de Proyecto (para la próxima clase, 10 minutos):
- Cada equipo presentará su propuesta de aplicación, destacando:
  - El problema que resuelve o propósito del MVP.
  - La audiencia objetivo.
  - Las funcionalidades principales.
  - Crear de 8 a 15 historias de usuario (HU) siguiendo el formato de Connextra
  - Product Backlog y Release plan.

#### 3. Uso de IA para Mejorar la Planificación y análisis:
- Generar prompts para:
  - Generar el Product Backlog
  - Refinar las historias de usuario.
  - Sugerir tareas técnicas necesarias.
  - Documentar los prompts utilizados y el tiempo empleado en cada interacción con la IA.

#### 4. Desarrollo del MVP:
- Implementación de las HU planeadas para cada Sprint.
- Uso de herramientas de IA para:
  - Diseño
  - Generación de código
  - Pruebas
  - Despliegue
  - Documentar los prompts utilizados y el tiempo empleado en cada interacción con la IA.

#### 5. Documentación del Proceso:
- Registrar cada interacción con la IA:
  - Prompt utilizado.
  - Respuesta de la IA.
  - Tiempo empleado.
  - Valor añadido (¿Aceleró el proceso? ¿Generó nuevas ideas?).
  - Manuales

#### 6. Revisión de los Sprints:
- Presentación del avance del MVP
- Recibir retroalimentación y ajustar el producto backlog si es necesario.

#### 7. Evaluación:
- Se evaluará:
  - Creatividad e innovación del proyecto (MVP).
  - Uso efectivo de la IA en marco de la metodología Scrum.
  - Documentación detallada y organizada.

**Material Entregable:**
- MVP funcional y referencia al repositorio (GitHub)
- **Documentación del proyecto**: Incluyendo todos los prompts utilizados, tiempos de respuesta de la IA y lecciones aprendidas.

---

**Próxima Clase**: Traer elaborados los puntos 1,2 y 3 de la propuesta del MVP

---

## Proceso de desarrollo ágil con Scrum para aplicaciones inteligentes

**Smar BPM**  
**Argillactura**

**Sprint Cero**  
**Spint Smar Product Backlog**  
**Equipo de desarrollo**

**Scrum Master**  
**Equipo de desarrollo**

**Sprint Funcionalidades tradicionales**  
**Funcionalidades inteligentes**

**Reunión diaria**  
**Sprint Review**  
**Sprint Retrospective**

### Herramientas de IA
(ChatGPT, Gemini, Galileo AI, Github Copilot, etc)

---

**Reunirse en equipos e iniciar la lluvia de ideas de posibles proyectos**

- **DESIGN**
  - AECH
  - DESIGN

---

## ¿Preguntas?

- [ ]  
- [ ]  
- [ ]  

---

### Gracias