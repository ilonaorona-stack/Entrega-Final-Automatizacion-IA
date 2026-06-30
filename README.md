# 🤖 Entrega Final – Ecosistema de Automatización IA

Proyecto desarrollado para el curso **Automatización e Inteligencia Artificial** de Coderhouse.

---

# 📌 Objetivo

Desarrollar un ecosistema de automatización basado en Inteligencia Artificial capaz de analizar, clasificar y gestionar automáticamente leads comerciales utilizando Make, OpenAI, Notion y Gmail.

La solución permite reducir tareas manuales, estandarizar criterios comerciales y agilizar el proceso de análisis mediante IA.

---

# 🛠 Tecnologías utilizadas

- Make
- OpenAI (GPT)
- Notion
- Gmail
- JSON

---

# ⚙️ Flujo de automatización

El escenario implementado realiza automáticamente el siguiente proceso:

1. Se detecta la creación de un nuevo lead en Notion.
2. Make obtiene toda la información del registro.
3. Los datos son enviados a OpenAI mediante un prompt dinámico.
4. La IA clasifica el lead y devuelve una respuesta estructurada en formato JSON.
5. Parse JSON procesa la respuesta.
6. Se actualiza automáticamente el registro en Notion.
7. Se envía un correo electrónico al responsable comercial para su revisión.

---

# 🧠 Arquitectura

```
Notion
   │
   ▼
Make
   │
   ▼
OpenAI (GPT)
   │
   ▼
Parse JSON
   │
   ▼
Notion (Actualización)
   │
   ▼
Gmail (Notificación)
```

---

# 👤 Human in the Loop

La automatización incorpora una instancia de supervisión humana.

Si bien OpenAI realiza la clasificación automática del lead, el sistema envía un correo electrónico al responsable comercial para que revise el análisis antes de tomar cualquier decisión comercial.

Esto garantiza que la Inteligencia Artificial actúe como herramienta de asistencia y no como reemplazo de la decisión humana.

---

# 🔒 Seguridad del flujo

Durante el desarrollo se aplicaron buenas prácticas para garantizar la estabilidad del escenario:

- Se evita la generación de bucles infinitos utilizando un trigger únicamente sobre nuevos registros.
- El prompt utiliza variables dinámicas provenientes de Notion.
- Los datos mantienen sus tipos correspondientes (texto, números y selecciones).
- La respuesta de OpenAI se procesa exclusivamente mediante JSON estructurado.
- Toda la información es actualizada automáticamente en Notion utilizando los campos correspondientes.

---

# ⚠️ Manejo de errores

El escenario incorpora un **Error Handler (Resume)** de Make.

Esta estrategia permite que una falla puntual en un módulo no detenga completamente la ejecución del escenario, mejorando la robustez y continuidad del proceso.

---

# 📂 Archivos incluidos

- Documentación completa del proyecto (PDF)
- Blueprint del escenario (`.blueprint.json`)
- Carpeta **Screenshots** con evidencias del funcionamiento
- README del proyecto

---

# 📸 Evidencias

La carpeta **Screenshots** contiene capturas de:

- Escenario completo en Make.
- Ejecución exitosa.
- Configuración del módulo OpenAI.
- Prompt utilizado.
- Parse JSON.
- Actualización en Notion.
- Configuración de Gmail.
- Manejo de errores.

---

# 📖 Base de datos (Modo lectura)

https://app.notion.com/p/Entrega-Final-Ecosistema-de-Automatizaci-n-IA-Aut-nomo-para-Negocios-38c01f55c882800699cfddca5ae6e937?source=copy_link

---

# 👩‍💻 Autora

**Ilona Orona**

Curso: **Automatización e Inteligencia Artificial – Coderhouse**
