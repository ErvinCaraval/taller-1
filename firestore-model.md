## Justificación del modelo propuesto

El modelo de datos propuesto para Firebase Firestore está diseñado para cubrir todas las funcionalidades descritas en el README.md del proyecto "Juego de Preguntas Multijugador". Se utilizan colecciones separadas para usuarios, partidas, preguntas, historial y ranking, lo que permite escalabilidad, consultas eficientes y flexibilidad para futuras ampliaciones. La estructura facilita:

- **Escalabilidad:** Cada colección puede crecer de forma independiente y soportar grandes volúmenes de datos.
- **Flexibilidad:** Permite agregar campos o subcolecciones según nuevas necesidades (por ejemplo, chat en partidas, historial por usuario).
- **Consultas eficientes:** El acceso a datos por usuario, partida o historial es directo y optimizado para Firestore.
- **Separación de responsabilidades:** Cada entidad (usuario, partida, pregunta, etc.) tiene su propia colección, simplificando la lógica de backend y frontend.
- **Compatibilidad con Firebase:** El modelo aprovecha las ventajas de Firestore, como la sincronización en tiempo real y la gestión de permisos por documento.

Este diseño está alineado con las mejores prácticas para aplicaciones multijugador y educativas, y puede adaptarse fácilmente a nuevas funcionalidades o requisitos del negocio.

// Firestore data model for Juego de Preguntas Multijugador
// This file describes the collections and example documents for Firebase Firestore

/*
Collection: users
----------------
{
  id: string (Firestore auto-ID),
  email: string,
  passwordHash: string,
  displayName: string,
  stats: {
    gamesPlayed: number,
    gamesWon: number,
    correctAnswers: number,
    incorrectAnswers: number,
    totalScore: number
  },
  createdAt: timestamp,
  friends: [userId],
  resetToken: string (optional),
  resetTokenExpires: timestamp (optional)
}

Collection: games
-----------------
{
  id: string (Firestore auto-ID),
  type: "public" | "private",
  status: "waiting" | "in_progress" | "finished",
  players: [userId],
  invited: [userId],
  questions: [questionId],
  currentQuestion: number,
  scores: {
    [userId]: number
  },
  answers: {
    [userId]: [
      { questionId: string, selectedOption: number, isCorrect: boolean, answeredAt: timestamp }
    ]
  },
  createdBy: userId,
  createdAt: timestamp,
  finishedAt: timestamp (optional)
}

Collection: questions
---------------------
{
  id: string (Firestore auto-ID),
  text: string,
  options: [string],
  correctOption: number,
  category: string,
  explanation: string,
  createdBy: userId,
  createdAt: timestamp,
  isActive: boolean,
  lastUpdated: timestamp
}

Collection: history
-------------------
{
  id: string (Firestore auto-ID),
  userId: string,
  gameId: string,
  answers: [
    { questionId: string, selectedOption: number, isCorrect: boolean, answeredAt: timestamp }
  ],
  score: number,
  playedAt: timestamp
}

Collection: ranking
-------------------
{
  id: string (Firestore auto-ID),
  userId: string,
  totalScore: number,
  gamesPlayed: number,
  gamesWon: number,
  correctAnswers: number,
  position: number,
  updatedAt: timestamp
}

// Subcollections (optional, for scalability):
// users/{userId}/games: historial de partidas del usuario
// games/{gameId}/chat: mensajes de chat en la partida
// games/{gameId}/events: eventos de la partida (inicio, fin, respuestas, etc.)

// Example Firestore security rules and indexes should be defined for production use.
