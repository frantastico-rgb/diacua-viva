# 📝 TEMPLATES DE FORMULARIOS GOOGLE FORMS

## 🎯 Formularios Esenciales a Crear

### 1. FORMULARIO DE VOLUNTARIOS

**URL a crear:** https://forms.google.com

**Estructura sugerida:**

```
TÍTULO: DIACUA VIVA - Registro de Voluntarios

DESCRIPCIÓN:
¡Gracias por tu interés en ser parte del Árbol Cultural de Villavicencio! 
Completa este formulario y nos pondremos en contacto contigo.

--- PREGUNTAS ---

1. Nombre completo *
   [Respuesta corta]

2. Email *
   [Respuesta corta]

3. Teléfono / WhatsApp *
   [Respuesta corta]

4. Edad
   [Selección múltiple]
   - 18-25 años
   - 26-35 años
   - 36-50 años
   - 51-65 años
   - 65+ años

5. ¿En qué área te gustaría colaborar? *
   [Casillas de verificación]
   - Trabajo de campo (encuestas)
   - Transcripción de entrevistas
   - Difusión en redes sociales
   - Apoyo logístico en eventos
   - Diseño gráfico
   - Fotografía/Video
   - Otro: _______

6. ¿Cuántas horas a la semana podrías dedicar?
   [Selección múltiple]
   - 1-3 horas
   - 4-8 horas
   - 9-15 horas
   - Más de 15 horas

7. ¿Tienes experiencia previa en proyectos culturales?
   [Párrafo]

8. ¿Por qué quieres ser voluntario/a de DIACUA VIVA? *
   [Párrafo]

9. Disponibilidad horaria
   [Casillas de verificación]
   - Lunes a Viernes - mañanas
   - Lunes a Viernes - tardes
   - Lunes a Viernes - noches
   - Fines de semana
   - Flexible

--- MENSAJE DE CONFIRMACIÓN ---
¡Gracias! Hemos recibido tu información. 
Nos pondremos en contacto en un plazo de 3-5 días hábiles.
```

**Después de crear:**
1. Enviar → `<>` (código HTML)
2. Copiar URL: `https://docs.google.com/forms/d/e/[ID]/viewform`
3. Pegar en `presentacion.html` línea ~1450:
   ```javascript
   'voluntario': 'TU_URL_AQUI',
   ```

---

### 2. FORMULARIO DE PROPUESTAS COMUNITARIAS

```
TÍTULO: DIACUA VIVA - Enviar Propuesta Cultural

DESCRIPCIÓN:
Comparte tu idea para el desarrollo cultural de Villavicencio.
Las mejores propuestas serán consideradas para el Plan Estratégico Cultural 2026-2030.

--- PREGUNTAS ---

1. Tu nombre *
   [Respuesta corta]

2. Email de contacto *
   [Respuesta corta]

3. Teléfono / WhatsApp
   [Respuesta corta]

4. ¿Representas a algún colectivo u organización?
   [Respuesta corta]
   Ejemplo: Colectivo de Hip-Hop, Casa de la Cultura, Individual

5. Título de tu propuesta *
   [Respuesta corta]
   Ejemplo: "Festival de Memoria Oral"

6. Describe tu propuesta *
   [Párrafo]
   Explica qué quieres hacer, cómo y por qué es importante para Villavicencio.

7. ¿A qué categoría del árbol pertenece? *
   [Selección múltiple]
   - 🌱 Raíces (Identidad y memoria)
   - 🪵 Tronco (Gestión e institucionalidad)
   - 🍃 Ramas (Producción y consumo cultural)
   - 💧 Agua (Participación ciudadana)

8. ¿Qué recursos necesitarías?
   [Casillas de verificación]
   - Financiamiento
   - Espacio físico
   - Difusión
   - Equipo técnico
   - Voluntarios
   - Asesoría especializada
   - Otro: _______

9. ¿Qué población beneficiaría?
   [Casillas de verificación]
   - Niños/as
   - Jóvenes
   - Adultos
   - Adultos mayores
   - Artistas
   - Comunidad general
   - Barrios periféricos

10. ¿Ya has implementado algo similar antes?
    [Respuesta corta]

11. ¿Estarías dispuesto/a a liderar esta propuesta?
    [Selección múltiple]
    - Sí, puedo liderarla
    - Sí, con apoyo de DIACUA VIVA
    - Prefiero solo aportar la idea
    - No estoy seguro/a

12. Enlaces o archivos de soporte (opcional)
    [Párrafo]
    Comparte links a portafolio, videos, PDFs, etc.

--- MENSAJE DE CONFIRMACIÓN ---
¡Propuesta recibida! 
Nuestro equipo la evaluará y te contactaremos en 7-10 días.
Tu idea es valiosa para construir el futuro cultural de Villavicencio.
```

---

### 3. FORMULARIO DE PATROCINADORES

```
TÍTULO: DIACUA VIVA - Oportunidades de Patrocinio

DESCRIPCIÓN:
Sé parte del cambio cultural en Villavicencio. 
Conoce nuestros niveles de patrocinio y beneficios.

--- PREGUNTAS ---

1. Nombre de la empresa / organización *
   [Respuesta corta]

2. Representante legal *
   [Respuesta corta]

3. Cargo
   [Respuesta corta]

4. Email corporativo *
   [Respuesta corta]

5. Teléfono *
   [Respuesta corta]

6. Sector / Industria
   [Selección múltiple]
   - Banca y finanzas
   - Tecnología
   - Comercio
   - Industria
   - Servicios
   - ONG
   - Gobierno/Público
   - Otro: _______

7. ¿Qué tipo de apoyo te interesa? *
   [Casillas de verificación]
   - Patrocinio económico
   - Donación en especie (equipos, espacios)
   - Alianza estratégica
   - Voluntariado corporativo
   - Otro: _______

8. Nivel de patrocinio de interés
   [Selección múltiple]
   - Platino (Financiación completa de una fase)
   - Oro (Apoyo a equipos de investigación)
   - Plata (Financiación de herramientas)
   - Bronce (Apoyo logístico)
   - Deseo más información

9. ¿Qué te motiva a apoyar DIACUA VIVA?
   [Párrafo]

10. ¿Tiene tu empresa programa de RSE (Responsabilidad Social)?
    [Selección múltiple]
    - Sí, con presupuesto asignado
    - Sí, en desarrollo
    - No, pero nos interesa
    - No

11. Presupuesto aproximado para cultura/RSE (anual)
    [Selección múltiple]
    - Menos de $5 millones COP
    - $5-15 millones COP
    - $15-50 millones COP
    - Más de $50 millones COP
    - Prefiero no responder

12. ¿Cuándo sería el mejor momento para contactarte?
    [Respuesta corta]

--- MENSAJE DE CONFIRMACIÓN ---
¡Gracias por tu interés!
Prepararemos una propuesta personalizada y nos comunicaremos 
en los próximos 3-5 días hábiles.
```

---

### 4. ENCUESTA DE CONSUMO CULTURAL (Versión Corta)

```
TÍTULO: Encuesta de Consumo Cultural - Villavicencio

DESCRIPCIÓN:
Ayúdanos a entender el consumo cultural de Villavicencio.
Son solo 10 preguntas (5 minutos). ¡Tu voz importa!

--- PREGUNTAS ---

1. Barrio donde vives *
   [Respuesta corta]

2. Edad *
   [Selección múltiple]
   - 15-25
   - 26-35
   - 36-50
   - 51-65
   - 65+

3. Género
   [Selección múltiple]
   - Femenino
   - Masculino
   - No binario
   - Prefiero no decir

4. ¿Con qué frecuencia asistes a eventos culturales? *
   [Selección múltiple]
   - Varias veces al mes
   - Una vez al mes
   - Algunas veces al año
   - Casi nunca
   - Nunca

5. ¿Qué tipo de eventos culturales has asistido en el último año?
   [Casillas de verificación]
   - Conciertos / festivales
   - Teatro
   - Cine
   - Exposiciones de arte
   - Ferias / festivales gastronómicos
   - Danza
   - Eventos literarios
   - Ninguno

6. ¿Cuál es la principal BARRERA para asistir a eventos culturales? *
   [Selección múltiple]
   - Precio / costo
   - Falta de tiempo
   - No hay eventos que me interesen
   - Quedan lejos de mi barrio
   - No me entero de los eventos
   - Falta de seguridad
   - Otro: _______

7. ¿Practicas alguna actividad artística o cultural?
   [Casillas de verificación]
   - Música
   - Danza
   - Teatro
   - Artes plásticas
   - Escritura
   - Artesanía
   - Fotografía/Video
   - No practico ninguna

8. ¿Qué tipo de eventos culturales te gustaría que hubiera MÁS en Villavicencio? *
   [Párrafo]

9. Del 1 al 10, ¿qué tan orgulloso/a te sientes de la identidad cultural de Villavicencio? *
   [Escala lineal: 1 - 10]
   1 = Nada orgulloso/a
   10 = Muy orgulloso/a

10. ¿Estarías dispuesto/a a participar en un grupo focal sobre cultura? (te contactaríamos)
    [Selección múltiple]
    - Sí, déjame tu email/WhatsApp: _______
    - No, solo quiero responder la encuesta

--- MENSAJE DE CONFIRMACIÓN ---
¡Gracias por tu participación!
Tus respuestas ayudarán a construir un mejor ecosistema cultural en Villavicencio.
```

---

## 🔧 CONFIGURACIÓN POST-CREACIÓN

### Para CADA formulario:

1. **Configurar respuestas:**
   - Responses → Crear hoja de cálculo
   - Nombre: "Respuestas - [Nombre Form]"

2. **Configurar notificaciones:**
   - Settings (engranaje) → Presentation
   - ✅ "Show progress bar"
   - ✅ "Shuffle question order" (para encuesta)
   - Responses → Get email notifications: ✅

3. **Obtener URL de embed:**
   - Send → `<>` tab
   - Copiar `src` del iframe
   - Ejemplo: `https://docs.google.com/forms/d/e/1FAIpQLSc_ABC123/viewform?embedded=true`

4. **Actualizar en presentacion.html:**
   ```javascript
   // Buscar línea ~1450
   const formURLs = {
       'voluntario': 'URL_DEL_PASO_3',
       'propuesta': 'URL_DEL_PASO_3',
       'patrocinar': 'URL_DEL_PASO_3',
       // ...
   };
   ```

---

## 📊 ANÁLISIS DE RESPUESTAS

### Google Sheets automático:
- Cada respuesta = nueva fila
- Timestamp automático
- Exportable a Excel/CSV

### Crear gráficos:
1. En Sheets → Insert → Chart
2. Seleccionar tipo de gráfico
3. Configurar ejes

### Dashboard simple:
- Crear hoja "Dashboard"
- Usar fórmulas:
  ```
  =COUNTIF(Respuestas!B:B, "18-25")  // Contar por edad
  =AVERAGE(Respuestas!J:J)           // Promedio de orgullo cultural
  ```

---

## 🎨 PERSONALIZACIÓN (Opcional)

### Cambiar tema del form:
- Tema (paleta) → Personalizar
- Color primario: `#2d5016` (verde DIACUA VIVA)
- Color de fondo: `#f4f7f0`

### Agregar header image:
- Theme → Add image
- Usar `logo.png` (subir)

---

## ✅ CHECKLIST

- [ ] Formulario 1: Voluntarios creado
- [ ] Formulario 2: Propuestas creado
- [ ] Formulario 3: Patrocinadores creado
- [ ] Formulario 4: Encuesta Cultural creado
- [ ] URLs actualizadas en presentacion.html
- [ ] Notificaciones email activadas
- [ ] Hojas de cálculo vinculadas
- [ ] Probado desde la web (clic en botones)

---

**⏱️ Tiempo estimado:** 1-2 horas para crear los 4 formularios

**💡 Tip:** Crea primero uno, pruébalo completo, luego duplica y modifica para los otros.
