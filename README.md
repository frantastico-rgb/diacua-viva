# 🌳 DIACUA VIVA - Árbol Cultural Villavicencio

> Proyecto de investigación, monitoreo y gestión cultural con enfoque de arraigo e identidad ancestral territorial.

## 🚀 Inicio Rápido

### Ver la presentación localmente:
1. Abre `presentacion.html` en tu navegador
2. El video y logo cargarán automáticamente

### Desplegar en línea (GRATIS):
```bash
# 1. Instalar Git (si no lo tienes)
# Descarga desde: https://git-scm.com/

# 2. Inicializar repositorio
git init
git add .
git commit -m "DIACUA VIVA - Presentación inicial"

# 3. Subir a GitHub
# Crea repositorio en github.com
git remote add origin https://github.com/TU_USUARIO/diacua-viva.git
git push -u origin main

# 4. Conectar con Vercel
# Ve a vercel.com → Import Project → Selecciona tu repo
# ¡Listo! Tendrás URL en 2 minutos
```

## 📝 Configurar Formularios

### URGENTE: Reemplazar URLs de Google Forms

1. **Crea tus formularios en Google Forms** (https://forms.google.com)
2. **Obtén el link de embed** (Enviar → `<>`)
3. **Actualiza en `presentacion.html`** (línea ~1450):

```javascript
const formURLs = {
    'investigar': 'TU_URL_AQUI',      // ← CAMBIAR
    'voluntario': 'TU_URL_AQUI',      // ← CAMBIAR
    'propuesta': 'TU_URL_AQUI',       // ← CAMBIAR
    // ... resto
};
```

## 📂 Estructura del Proyecto

```
DIACUA VIVA/
├── presentacion.html           # Página principal
├── logo.png                    # Logo del proyecto
├── DIACUA VIV.mp4             # Video clip del logo
├── DIACUA VIVA.txt            # Documento base de investigación
├── GUIA_DESPLIEGUE_Y_DESARROLLO.md  # Guía completa (LEER PRIMERO)
└── README.md                   # Este archivo
```

## ✨ Características

- ✅ **Responsive** (móvil, tablet, desktop)
- ✅ **Secciones expandibles** (acordeón)
- ✅ **Roles interactivos** (8 perfiles diferentes)
- ✅ **Propuestas comunitarias**
- ✅ **Formularios preparados** (iframes)
- ✅ **SEO optimizado**
- ✅ **Logo y video integrados**

## 🎯 Próximos Pasos

1. [ ] Crear Google Forms (ver `TEMPLATES_FORMULARIOS.md`)
2. [ ] Configurar email: contacto@diacuaviva.org
3. [ ] Desplegar en Vercel
4. [ ] Lanzar campaña en redes sociales

## 📊 Tecnologías

- **Frontend:** HTML5, CSS3, JavaScript (Vanilla)
- **Hosting:** Vercel / GitHub Pages (gratis)
- **Forms:** Google Forms / Typeform
- **Analytics:** Google Analytics (próximamente)

## 📧 Contacto

- **Email:** contacto@diacuaviva.org (en configuración)
- **Ubicación:** Villavicencio, Meta, Colombia

## 📄 Licencia

© 2025 DIACUA VIVA. Todos los derechos reservados.
Proyecto sin ánimo de lucro con enfoque comunitario.

---

**💡 ¿Necesitas ayuda?** Lee la [Guía Completa](GUIA_DESPLIEGUE_Y_DESARROLLO.md)
