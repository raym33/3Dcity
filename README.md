# 🏙️ C1 English Metropolis MEGA

> Juego educativo inmersivo en 3D para aprender inglés nivel C1 mediante exploración urbana interactiva.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Three.js](https://img.shields.io/badge/Three.js-000000?style=flat&logo=three.js&logoColor=white)

## 📖 Descripción

**C1 English Metropolis MEGA** es un juego de exploración en primera persona que combina el aprendizaje del inglés avanzado (nivel C1) con mecánicas de mundo abierto. Los jugadores exploran una ciudad 3D generada proceduralmente, interactúan con NPCs, recolectan materiales educativos y completan misiones mientras practican estructuras gramaticales complejas.

## ✨ Características Principales

### 🎮 Jugabilidad
- **Exploración en primera persona** con controles fluidos WASD
- **Ciudad procedural** con más de 25 rascacielos, parques y edificios
- **100+ NPCs interactivos** con diálogos educativos
- **40+ papeles/revistas** coleccionables con contenido gramatical
- **Sistema de misiones** con waypoints y seguimiento de progreso
- **Transporte público** con sistema de autobús (11 paradas)
- **Interiores detallados** para cada tipo de establecimiento

### 📚 Contenido Educativo
- Enfoque en gramática C1: condicionales de tercer tipo, inversión negativa, subjuntivo
- Vocabulario contextualizado por ubicación
- Síntesis de voz para pronunciación
- Sistema de feedback inmediato en diálogos

### 🎯 Mini-juegos
- **Pac-Man** jugable en máquinas arcade dentro del juego

## 🕹️ Controles

| Tecla | Acción |
|-------|--------|
| `W` | Avanzar |
| `S` | Retroceder |
| `A` | Desplazar izquierda |
| `D` | Desplazar derecha |
| `←` `→` | Rotar cámara |
| `E` | Interactuar |
| `M` | Mostrar/ocultar minimapa |
| `ESC` | Menú de pausa |

## 🏢 Ubicaciones

El juego incluye diversos establecimientos, cada uno con contenido educativo especializado:

| Ubicación | Temática Educativa |
|-----------|-------------------|
| 👔 Tienda de Ropa | Moda, tendencias, descripciones |
| 💊 Farmacia | Innovaciones farmacéuticas, salud |
| 🍽️ Restaurante | Gastronomía, técnicas culinarias |
| 🏦 Banco | Finanzas, estrategias de inversión |
| 💃 Discoteca | Entretenimiento, vida social |
| ⛪ Catedral | Arquitectura, historia, cultura |
| 🏟️ Estadio | Deportes, eventos, competiciones |

## 🏗️ Arquitectura Técnica

### Tecnologías
- **Three.js** - Motor de renderizado 3D
- **Web Speech API** - Síntesis de voz
- **HTML5/CSS3** - Interfaz de usuario
- **JavaScript ES6+** - Lógica del juego

### Sistemas del Juego

```
┌─────────────────────────────────────────────────────────┐
│                    GAME ENGINE                          │
├─────────────────────────────────────────────────────────┤
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐     │
│  │  Renderer   │  │   Physics   │  │  Collision  │     │
│  │  (Three.js) │  │   System    │  │   System    │     │
│  └─────────────┘  └─────────────┘  └─────────────┘     │
│                                                         │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐     │
│  │    NPC      │  │   Mission   │  │   Audio     │     │
│  │   Manager   │  │   Tracker   │  │   System    │     │
│  └─────────────┘  └─────────────┘  └─────────────┘     │
│                                                         │
│  ┌─────────────┐  ┌─────────────┐  ┌─────────────┐     │
│  │  Transport  │  │  Interior   │  │    UI       │     │
│  │   System    │  │  Generator  │  │   Manager   │     │
│  └─────────────┘  └─────────────┘  └─────────────┘     │
└─────────────────────────────────────────────────────────┘
```

### Estructura de Datos

```javascript
// Sistema de Misiones (~20 NPCs)
missions = {
  npcId: {
    location: { x, y, z },
    dialogues: [...],
    vocabulary: [...],
    rewards: { points, items }
  }
}

// Papeles Educativos (~32 documentos)
papers = {
  locationId: {
    title: "...",
    content: "...",
    grammarFocus: "...",
    exercises: [...]
  }
}

// Paradas de Autobús (11 destinos)
busStops = [
  { name: "Downtown", position: {...} },
  { name: "Business District", position: {...} },
  // ...
]
```

## 🖥️ Interfaz de Usuario

```
┌──────────────────────────────────────────────────────────┐
│  ⭐ Score: 1250    📋 Missions: 3/20    📄 Papers: 15/40 │
├──────────────────────────────────────────────────────────┤
│                                                          │
│                                                    ┌───┐ │
│                   VISTA 3D                         │MAP│ │
│                                                    └───┘ │
│                                                          │
│                      [E] Talk to Sarah                   │
├──────────────────────────────────────────────────────────┤
│  📍 Business District  |  Press E to interact           │
└──────────────────────────────────────────────────────────┘
```

## 🎓 Contenido Gramatical C1

El juego cubre estructuras gramaticales avanzadas:

- **Condicionales Mixtos**: "If I had studied harder, I would be fluent now"
- **Inversión Negativa**: "Never have I seen such a thing"
- **Subjuntivo**: "I suggest that he be present"
- **Cleft Sentences**: "What I need is more practice"
- **Participios Compuestos**: "Having finished the task, she left"
- **Reported Speech Avanzado**: Cambios de tiempo y perspectiva

## 🚀 Cómo Jugar

1. **Descarga** el archivo `C1-English-Metropolis-MEGA.html`
2. **Abre** el archivo en un navegador moderno (Chrome, Firefox, Edge)
3. **Explora** la ciudad usando los controles WASD
4. **Interactúa** con NPCs presionando E cuando aparezca el indicador
5. **Recolecta** papeles para aprender gramática y vocabulario
6. **Completa** misiones para ganar puntos y desbloquear contenido
7. **Usa** el sistema de autobús para moverte rápidamente

## 📊 Sistema de Puntuación

| Acción | Puntos |
|--------|--------|
| Recolectar papel | +50 |
| Completar diálogo | +30 |
| Viaje en autobús | +20 |
| Completar misión | +100 |
| Respuesta correcta | +25 |

## 🔧 Requisitos del Sistema

- **Navegador**: Chrome 80+, Firefox 75+, Edge 80+, Safari 13+
- **WebGL**: Soporte requerido
- **RAM**: 4GB mínimo recomendado
- **Conexión**: No requiere internet después de cargar

## 📁 Estructura del Proyecto

```
3Dcity/
└── C1-English-Metropolis-MEGA.html    # Archivo único con todo el juego
    ├── HTML Structure                  # Estructura del documento
    ├── CSS Styles                      # Estilos de interfaz
    ├── Three.js Scene                  # Escena 3D y renderizado
    ├── Game Logic                      # Mecánicas del juego
    ├── Educational Content             # Diálogos y papeles
    └── Audio System                    # Síntesis de voz
```

## 🤝 Contribuir

Las contribuciones son bienvenidas. Algunas áreas donde se puede mejorar:

- [ ] Añadir más NPCs y diálogos
- [ ] Expandir el contenido gramatical
- [ ] Mejorar los gráficos 3D
- [ ] Añadir más mini-juegos
- [ ] Implementar sistema de guardado
- [ ] Añadir modo multijugador
- [ ] Traducir interfaz a otros idiomas

## 📄 Licencia

Este proyecto es de código abierto. Consulta el archivo LICENSE para más detalles.

## 👤 Autor

Creado por [@raym33](https://github.com/raym33)

---

<p align="center">
  <b>¡Aprende inglés C1 mientras exploras una ciudad virtual!</b>
  <br>
  <a href="https://github.com/raym33/3Dcity">⭐ Dale una estrella si te gusta el proyecto</a>
</p>
