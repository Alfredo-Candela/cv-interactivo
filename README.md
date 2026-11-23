# 🚀 CV Web Interactivo con Vídeos (Google Vids) e IA (Gemini + Antigravity)

**Autor:** Alfredo Candela Estellés  
**Titulación:** Grado en Administración y Dirección de Empresas (ADE) & Data Science — ESIC University  
**Cargo actual:** Audit Intern en Ernst & Young (EY)  
**Contacto profesional:** [LinkedIn](https://www.linkedin.com/in/alfredo-candela-estell%C3%A9s-bba163355) · [GitHub](https://github.com/Alfredo-Candela) · [Email](mailto:ce.alfredo2004@gmail.com)  

---

## 🎯 Objetivo del Proyecto

Este proyecto consiste en el desarrollo y despliegue en **GitHub Pages** de un **currículum vitae interactivo de nueva generación**, integrando:
1. **Perfil profesional estructurado y verificado** en `perfil_cv.json` y `perfil_cv.txt`.
2. **Tres píldoras audiovisuales de 30 segundos** generadas con **Google Vids** (`videos/pitch.mp4`, `videos/proyecto.mp4` y `videos/habilidades.mp4`).
3. **Agente conversacional IA (Gemelo Digital)** impulsado por la API REST de **Gemini** (`gemini-2.5-flash`), con arquitectura de **RAG ligero (Retrieval-Augmented Generation)** fundamentado en la base de conocimiento de Alfredo.
4. **Diseño web responsivo, moderno y accesible**, integrado en un único archivo `index.html` estático optimizado para GitHub Pages.

---

## 📂 Estructura del Repositorio

El repositorio mantiene la estructura limpia y ordenada exigida en la rúbrica:

```plaintext
mi-cv-interactivo/
├── index.html            # Aplicación web completa (HTML, CSS y JS integrados)
├── perfil_cv.json        # Base de conocimiento estructurada para el modelo RAG
├── perfil_cv.txt         # Versión textual legible del perfil profesional
├── guiones_videos.md     # Guiones cronometrados segundo a segundo para Google Vids
├── README.md             # Documentación exhaustiva y guía del proyecto
├── .gitignore            # Exclusión de archivos confidenciales, PDFs y respaldos
└── videos/               # Directorio de medios audiovisuales
    ├── pitch.mp4         # 1. Elevator Pitch (30s)
    ├── proyecto.mp4      # 2. Proyecto Destacado (30s)
    └── habilidades.mp4   # 3. Habilidades Blandas y Motivación en IA (30s)
```

---

## 🎬 Las 3 Píldoras de Vídeo (Google Vids - 30 segundos)

Cada vídeo ha sido diseñado para durar **exactamente 30 segundos** (~68 a 72 palabras de locución):

1. **`videos/pitch.mp4` — Elevator Pitch (30s):**
   - *Contenido:* Presentación de Alfredo, su formación en ESIC University (ADE & Data Science), su experiencia en auditoría en EY y su propuesta de valor híbrida entre negocio y tecnología.
2. **`videos/proyecto.mp4` — Proyecto Destacado (30s):**
   - *Contenido:* Reto técnico real de Data Science (EDA y pipeline predictivo en Python con Pandas/NumPy), explicando el preprocesamiento, el impacto de fiabilidad alcanzado y su publicación en GitHub.
3. **`videos/habilidades.mp4` — Habilidades Blandas y Motivación en IA (30s):**
   - *Contenido:* Trabajo en equipo y liderazgo forjados en el fútbol federado y mérito deportivo como MVP en EE.UU., inmersión internacional en New Hampshire (Inglés C1) y Uruguay, y pasión por el impacto transformador de la Inteligencia Artificial.

*(Consulta [`guiones_videos.md`](guiones_videos.md) para el desglose detallado escena a escena, textos en pantalla y tiempos de locución).*

---

## 🤖 Asistente Conversacional IA (RAG Ligero con Gemini)

### Características del Chatbot:
- **Modelo:** Conectado directamente a `gemini-2.5-flash` (con fallback de resiliencia a `gemini-1.5-flash`) mediante la API REST de Google AI Studio.
- **RAG Ligero:** La información de `perfil_cv.json` se inyecta en el `systemInstruction` para actuar como base de verdad inmutable.
- **Anti-Alucinaciones:** Configurado para responder exclusivamente con datos verificados de Alfredo. Si se le pregunta por tecnologías o certificaciones no presentes (ej. certificaciones cloud de AWS), reconoce con total honestidad y cortesía el límite de su conocimiento.
- **Seguridad Estricta de la API Key:**
  - El usuario introduce su propia clave mediante un campo `<input type="password">`.
  - Se almacena de forma privada en el `localStorage` del navegador.
  - **Cero exposición:** La clave nunca se escribe en el código fuente, repositorios, registros ni commits de Git.
  - Opción de visualización protegida y botón de borrado inmediato.

---

## 🛠️ Cómo Ejecutar el Proyecto en Local

### Opción 1: Abrir directamente en el navegador
Haz doble clic sobre `index.html` o arrástralo a Google Chrome, Microsoft Edge, Safari o Firefox.

### Opción 2: Servidor local ligero
En la raíz del proyecto, ejecuta:
```bash
python -m http.server 8000
```
Y abre en tu navegador: [http://localhost:8000](http://localhost:8000).

---

## 🌐 Despliegue en GitHub Pages

1. Sube los archivos a un repositorio público en GitHub (por ejemplo, `cv-interactivo`):
   ```bash
   git add .
   git commit -m "feat: CV interactivo con videos y Gemini AI"
   git push -u origin main
   ```
2. En GitHub, ve a **Settings** → **Pages**.
3. En **Source**, selecciona **Deploy from a branch**.
4. Elige la rama `main` y la carpeta `/ (root)`. Pulsa **Save**.
5. En 1-2 minutos, tu web estará disponible en:  
   `https://Alfredo-Candela.github.io/cv-interactivo/`

---

## 🔒 Privacidad y Cumplimiento Normativo

Siguiendo las directrices del enunciado y buenas prácticas de protección de datos:
- Se han omitido de forma deliberada el número de teléfono personal, dirección domiciliaria y documentos de identidad.
- Solo se incluye información profesional apta para su difusión pública (nombre, titulación, enlaces a LinkedIn/GitHub y email de contacto).
- El currículum original en PDF no se almacena en el repositorio público.
