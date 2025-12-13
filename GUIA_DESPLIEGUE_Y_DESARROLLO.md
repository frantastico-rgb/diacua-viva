# 🚀 GUÍA DE DESPLIEGUE Y DESARROLLO - DIACUA VIVA

## 📋 ÍNDICE
1. [Integración Completada](#integración-completada)
2. [Desarrollo Futuro sobre esta Base](#desarrollo-futuro)
3. [Frameworks Recomendados](#frameworks-recomendados)
4. [Sistema de Recolección de Datos](#recolección-de-datos)
5. [Despliegue en Vercel](#despliegue-vercel)
6. [Formularios con iFrames](#formularios-iframes)
7. [Roadmap Recomendado](#roadmap)
8. [Recursos y Siguientes Pasos](#siguientes-pasos)

---

## ✅ INTEGRACIÓN COMPLETADA

### Logo y Video
- ✅ **Favicon** agregado al `<head>` (logo.png)
- ✅ **Logo animado** en el hero con efecto fadeInScale
- ✅ **Video clip** del logo con autoplay loop en el hero
- ✅ **SEO metatags** para mejor posicionamiento

### Nueva Sección: Propuestas Comunitarias
- ✅ Sección `#propuestas` creada
- ✅ 3 ejemplos de propuestas (María, Juan, Laura)
- ✅ Botón "Publicar Mi Propuesta"
- ✅ Sistema de tags por categoría

---

## 🔨 DESARROLLO FUTURO SOBRE ESTA BASE

### ✅ **SÍ, ES TOTALMENTE FACTIBLE**

Tu archivo HTML actual es una **base sólida** para expandir. Aquí el plan:

#### **Fase 1: Expansión HTML/CSS/JS (Próximos 1-3 meses)**
- ✅ **Mantener HTML puro** para las siguientes secciones:
  - Aspectos legales (agregar PDFs descargables)
  - Financiero (gráficos con Chart.js)
  - Donaciones (integrar PayPal/Stripe)
  - Contacto (mapa de Google Maps)
  - Laboratorio (dashboard con datos estáticos)

**Ventajas:**
- ⚡ Rápido de implementar
- 💰 Sin costos de hosting complejos
- 🎓 Fácil de mantener por voluntarios

**Límites:**
- ❌ No hay base de datos dinámica
- ❌ No hay sistema de usuarios/login
- ❌ Las propuestas no se guardan automáticamente

#### **Fase 2: Migración a Framework (Meses 4-12)**
Cuando necesites funcionalidades avanzadas.

---

## 🛠️ FRAMEWORKS RECOMENDADOS

### **OPCIÓN 1: Next.js + Vercel** ⭐ **RECOMENDADO**

**¿Por qué?**
- ✅ Gratuito para proyectos sin fines de lucro
- ✅ Despliegue automático con Git
- ✅ SEO excelente (importante para visibilidad)
- ✅ Puede iniciar con páginas estáticas y crecer progresivamente
- ✅ Vercel tiene plan gratuito generoso

**Stack completo recomendado:**
```
Frontend: Next.js 14 (React)
Estilos: Tailwind CSS (o mantener CSS puro)
Base de datos: Supabase (PostgreSQL gratis)
Autenticación: NextAuth.js
Forms: React Hook Form
Hosting: Vercel (gratis)
```

**Cuándo migrar:**
- Cuando necesites login de usuarios por rol
- Dashboard personalizado por usuario
- Base de datos de propuestas/eventos
- Sistema de notificaciones

---

### **OPCIÓN 2: WordPress** (Alternativa)

**¿Por qué?**
- ✅ Interfaz visual para que no-programadores editen
- ✅ Plugins para todo (forms, eventos, donaciones)
- ✅ Hosting económico ($3-5/mes)

**Contras:**
- ❌ Menos personalizable que Next.js
- ❌ Puede ser lento sin optimización
- ❌ Requiere mantenimiento de seguridad

---

### **OPCIÓN 3: Webflow/Framer** (No-Code)

**¿Por qué?**
- ✅ Visual, sin programación
- ✅ Diseños profesionales
- ✅ Integración con Airtable/Notion

**Contras:**
- ❌ Costo mensual ($12-20/mes)
- ❌ Menos flexibilidad

---

## 📊 SISTEMA DE RECOLECCIÓN DE DATOS

### **SOLUCIÓN INMEDIATA (Gratis, 0-2 meses)**

#### **Google Forms + Google Sheets** ⭐ **IMPLEMENTAR YA**

**Paso a paso:**

1. **Crear formularios en Google Forms:**
   - Formulario de Voluntarios
   - Formulario de Patrocinadores
   - Formulario de Propuestas Comunitarias
   - Formulario de Investigadores
   - Encuesta de Consumo Cultural (1000+ personas)

2. **Obtener enlaces de inserción:**
   ```
   Google Form → Enviar → Obtener código HTML
   Copiar URL: https://docs.google.com/forms/d/e/[ID]/viewform
   ```

3. **Integrar en tu HTML:**
   - Ya preparé el código con iframes
   - Reemplaza las URLs en la función `showContactForm()`
   - Busca: `'https://docs.google.com/forms/d/e/TU_FORMULARIO_INVESTIGADOR/viewform'`
   - Reemplaza con tu URL real

4. **Ventajas:**
   - ✅ Gratis ilimitado
   - ✅ Respuestas en Google Sheets automáticamente
   - ✅ Gráficos automáticos
   - ✅ Exportable a Excel/CSV
   - ✅ Puede tener lógica condicional

**Ejemplo de código actualizado:**
```javascript
const formURLs = {
    'voluntario': 'https://docs.google.com/forms/d/e/1FAIpQLSc_ABC123/viewform',
    'propuesta': 'https://docs.google.com/forms/d/e/1FAIpQLSc_XYZ789/viewform',
    // ...
};
```

---

### **SOLUCIÓN INTERMEDIA (Meses 3-6)**

#### **Typeform + Airtable** ($0-25/mes)

**Ventajas sobre Google Forms:**
- ✅ Experiencia de usuario superior (conversacional)
- ✅ Airtable como base de datos visual
- ✅ Automatizaciones con Zapier
- ✅ Informes más bonitos

**Ejemplo de flujo:**
```
Typeform (formulario) 
    → Zapier (automatización)
        → Airtable (base de datos)
        → Email de confirmación
        → Slack/WhatsApp notificación
```

---

### **SOLUCIÓN AVANZADA (Mes 6+)**

#### **Backend Propio + Base de Datos**

**Stack:**
- **Base de datos:** Supabase (PostgreSQL gratis hasta 500MB)
- **API:** Next.js API Routes o Supabase Realtime
- **Dashboard:** React + Chart.js

**Tablas necesarias:**
```sql
-- Usuarios
CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  email VARCHAR(255) UNIQUE,
  role VARCHAR(50), -- director, investigador, voluntario, etc.
  created_at TIMESTAMP
);

-- Propuestas
CREATE TABLE proposals (
  id SERIAL PRIMARY KEY,
  user_id INTEGER REFERENCES users(id),
  title VARCHAR(255),
  description TEXT,
  category VARCHAR(50),
  status VARCHAR(50), -- pendiente, aprobada, implementada
  created_at TIMESTAMP
);

-- Encuestas
CREATE TABLE surveys (
  id SERIAL PRIMARY KEY,
  respondent_name VARCHAR(255),
  age_range VARCHAR(20),
  cultural_consumption JSONB, -- datos de la encuesta
  created_at TIMESTAMP
);
```

---

## 🌐 DESPLIEGUE EN VERCEL

### **PASO A PASO**

#### **Opción 1: HTML Estático (Ahora mismo)** ⭐

1. **Crear cuenta en Vercel:**
   - Ve a https://vercel.com
   - Sign up with GitHub

2. **Crear repositorio Git:**
   ```bash
   cd "c:\Users\USUARIO\Desktop\TOTAL NUEVO 2.0\sena  2.0\ADSO\JAVA\DIACUA VIVA"
   git init
   git add .
   git commit -m "Initial commit - DIACUA VIVA"
   ```

3. **Subir a GitHub:**
   - Crea repositorio en GitHub: `diacua-viva`
   - Conecta y sube:
   ```bash
   git remote add origin https://github.com/TU_USUARIO/diacua-viva.git
   git branch -M main
   git push -u origin main
   ```

4. **Conectar con Vercel:**
   - Dashboard Vercel → "New Project"
   - Import Git Repository → Selecciona `diacua-viva`
   - Framework Preset: "Other"
   - Root Directory: `./`
   - Deploy!

5. **Tu sitio estará en:**
   ```
   https://diacua-viva.vercel.app
   ```

6. **Dominio personalizado (opcional):**
   - Compra dominio: `diacuaviva.org` ($10/año en Namecheap)
   - Vercel → Settings → Domains → Agregar dominio
   - Actualizar DNS

---

#### **Opción 2: GitHub Pages (Alternativa gratis)**

```bash
# Desde tu carpeta
git init
git add .
git commit -m "DIACUA VIVA presentación"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/diacua-viva.git
git push -u origin main

# Activar GitHub Pages
# Settings → Pages → Source: main branch
# URL: https://TU_USUARIO.github.io/diacua-viva/
```

---

## 📝 FORMULARIOS CON IFRAMES

### **YA ESTÁ PREPARADO EN TU CÓDIGO** ✅

**Cómo usarlo:**

1. **Crea tus Google Forms:**
   - Voluntarios: https://forms.google.com
   - Estructura sugerida:
     ```
     - Nombre completo
     - Email
     - Teléfono/WhatsApp
     - Rol de interés (dropdown)
     - ¿Por qué quieres participar? (párrafo)
     - Disponibilidad horaria
     ```

2. **Obtén el link de inserción:**
   - Form → Enviar → `<>` (ícono de código)
   - Copia el `src` del iframe
   - Ejemplo: `https://docs.google.com/forms/d/e/1FAIpQLSc_abc123/viewform?embedded=true`

3. **Actualiza el código JavaScript:**
   Busca en `presentacion.html`:
   ```javascript
   const formURLs = {
       'voluntario': 'TU_URL_AQUI',
       'propuesta': 'TU_URL_AQUI',
       // ...
   };
   ```

4. **Reemplaza `'TU_FORMULARIO_VOLUNTARIO'` con tu URL real**

---

### **Alternativa: Usar Typeform embed**

```javascript
const formURLs = {
    'propuesta': 'https://form.typeform.com/to/TU_ID_TYPEFORM',
};
```

Typeform se ve más profesional pero Google Forms es gratis ilimitado.

---

## 🗺️ ROADMAP RECOMENDADO

### **MES 1: CONFIGURACIÓN BÁSICA** (Ahora)
- [x] ✅ Presentación HTML lista
- [ ] Crear Google Forms (5 principales)
- [ ] Actualizar URLs en el código
- [ ] Desplegar en Vercel
- [ ] Configurar email: contacto@diacuaviva.org (Gmail con dominio)
- [ ] Crear redes sociales (Instagram, Facebook)

### **MES 2-3: RECOLECCIÓN DE DATOS**
- [ ] Lanzar campaña de encuestas (1000 personas)
- [ ] Recopilar propuestas comunitarias (20+)
- [ ] Primeros 50 voluntarios registrados
- [ ] Identificar 3-5 patrocinadores potenciales

### **MES 4-6: EXPANSIÓN DE CONTENIDO**
- [ ] Agregar sección "Noticias/Blog" (HTML estático)
- [ ] Publicar primeros resultados de encuestas (gráficos con Chart.js)
- [ ] Sección de eventos con calendario (FullCalendar.js)
- [ ] Galería multimedia de proyectos

### **MES 7-12: MIGRACIÓN A FRAMEWORK (Si se justifica)**
- [ ] Evaluar si el volumen de datos requiere base de datos
- [ ] Migrar a Next.js si tienes >200 usuarios activos
- [ ] Implementar dashboard por roles
- [ ] Sistema de login con NextAuth

---

## 🎯 SIGUIENTES PASOS INMEDIATOS

### **ESTA SEMANA:**

1. **Crear 3 Google Forms esenciales:**
   - ✅ Formulario de Voluntarios
   - ✅ Formulario de Propuestas Comunitarias  
   - ✅ Encuesta de Consumo Cultural (versión corta, 10 preguntas)

2. **Configurar email:**
   - Crear: contacto@diacuaviva.org
   - Puede ser Gmail con dominio ($6/mes Google Workspace)
   - O forwarding gratis desde registrador de dominio

3. **Desplegar en Vercel:**
   - Seguir guía arriba
   - Tendrás URL en 10 minutos

4. **Compartir en redes:**
   - Post en Facebook/Instagram con link
   - WhatsApp a contactos interesados
   - Email a agentes culturales

---

### **PRÓXIMO MES:**

5. **Agregar sección de "Noticias":**
   ```html
   <!-- Crear blog simple con HTML -->
   <div class="blog-post">
       <h3>Título de noticia</h3>
       <p>Fecha: 12 de diciembre 2025</p>
       <p>Contenido...</p>
   </div>
   ```

6. **Integrar Google Analytics:**
   ```html
   <!-- En el <head> -->
   <script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
   ```

7. **Mejorar SEO:**
   - Crear `sitemap.xml`
   - Registrar en Google Search Console
   - Optimizar imágenes (comprimir logo.png)

---

## 💡 SUGERENCIAS ADICIONALES PARA ESTE INICIO

### **1. SISTEMA DE "TESTIMONIOS"**
Agregar sección donde voluntarios/agentes publiquen experiencias:

```html
<div class="testimonial">
    <p>"Participar en DIACUA VIVA me permitió..."</p>
    <strong>- María González, Voluntaria</strong>
</div>
```

### **2. CONTADOR DE IMPACTO EN VIVO**
Actualizar manualmente cada semana:

```html
<div class="impact-counter">
    <h3>Nuestro Impacto</h3>
    <p>✅ 47 Voluntarios registrados</p>
    <p>✅ 12 Propuestas recibidas</p>
    <p>✅ 234 Encuestas completadas</p>
</div>
```

### **3. FAQ (Preguntas Frecuentes)**
Agregar sección tipo accordion:

```html
<div class="accordion-item">
    <div class="accordion-header">
        <span>¿Cómo puedo donar?</span>
    </div>
    <div class="accordion-content">
        <p>Puedes donar a través de...</p>
    </div>
</div>
```

### **4. MAPA INTERACTIVO**
Mostrar dónde están trabajando:

```html
<!-- Usando Google Maps embed -->
<iframe src="https://www.google.com/maps/embed?pb=..." 
        width="100%" height="400"></iframe>
```

### **5. NEWSLETTER SIGNUP**
Formulario simple para email:

```html
<!-- Usar Mailchimp embed gratis (2000 suscriptores) -->
<form action="https://mailchimp.com/..." method="post">
    <input type="email" name="EMAIL" placeholder="Tu email">
    <button type="submit">Suscribirse</button>
</form>
```

---

## 📊 COMPARACIÓN DE SOLUCIONES

| Característica | HTML Actual | + Google Forms | + Next.js | + WordPress |
|----------------|-------------|----------------|-----------|-------------|
| **Costo** | $0 | $0 | $0-25/mes | $5-15/mes |
| **Tiempo setup** | ✅ Listo | 1 día | 1-2 semanas | 2-3 días |
| **Recolecta datos** | ❌ | ✅ | ✅ | ✅ |
| **Dashboard** | ❌ | Sheets | ✅ Custom | ✅ Plugin |
| **Login usuarios** | ❌ | ❌ | ✅ | ✅ |
| **Mantenimiento** | Bajo | Bajo | Medio | Medio-Alto |
| **Escalabilidad** | Baja | Media | Alta | Media |

---

## ✅ CHECKLIST DE LANZAMIENTO

### **FASE PRE-LANZAMIENTO**
- [ ] Logo y video integrados ✅
- [ ] Crear 3 Google Forms
- [ ] Actualizar URLs en código
- [ ] Probar en móvil/desktop
- [ ] Configurar email contacto@
- [ ] Crear cuenta Instagram/Facebook
- [ ] Preparar post de lanzamiento

### **DÍA DE LANZAMIENTO**
- [ ] Desplegar en Vercel
- [ ] Probar todos los formularios
- [ ] Post en redes sociales
- [ ] Email a base de contactos
- [ ] WhatsApp a agentes clave
- [ ] Comunicado de prensa local (medios)

### **SEMANA 1**
- [ ] Monitorear Google Analytics
- [ ] Responder a primeros contactos
- [ ] Agregar primeras propuestas reales
- [ ] Ajustar según feedback

---

## 🆘 SOPORTE Y RECURSOS

### **Documentación:**
- Vercel: https://vercel.com/docs
- Google Forms: https://support.google.com/forms
- Next.js: https://nextjs.org/docs (para futuro)

### **Comunidades:**
- Discord de Vercel
- r/webdev (Reddit)
- Stack Overflow en español

### **Herramientas gratuitas útiles:**
- **Canva**: Diseño de gráficos para redes
- **TinyPNG**: Comprimir imágenes
- **Lighthouse**: Auditar SEO/rendimiento (en Chrome DevTools)

---

## 📧 CONFIGURACIÓN RÁPIDA DE EMAIL

### **Opción 1: Gmail con alias (GRATIS)**
```
1. Comprar dominio: diacuaviva.org
2. Configurar email forwarding en registrador
3. contacto@diacuaviva.org → tu_gmail@gmail.com
4. Responder desde Gmail con "Send mail as"
```

### **Opción 2: Google Workspace ($6/mes)**
```
- Email profesional: contacto@diacuaviva.org
- Drive ilimitado para equipo
- Google Meet para reuniones
```

---

## 🎉 CONCLUSIÓN

**Tu proyecto está en excelente forma para lanzar AHORA MISMO.**

**Plan de acción inmediato:**
1. ✅ Logo y video ya integrados
2. 📝 Crear 3 Google Forms hoy
3. 🚀 Desplegar en Vercel mañana
4. 📣 Lanzar campaña esta semana

**Migración a framework:**
- Espera hasta tener 100+ usuarios activos
- No es urgente ahora
- Next.js será la mejor opción cuando llegue el momento

**¿Necesitas ayuda con algo específico? Estoy aquí para apoyarte en este proceso!** 🌳
