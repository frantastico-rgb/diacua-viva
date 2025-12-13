# 🚀 COMANDOS RÁPIDOS DE DESPLIEGUE

## 📦 OPCIÓN 1: Desplegar en Vercel (RECOMENDADO)

### Paso 1: Instalar Git (si no lo tienes)
Descarga e instala desde: https://git-scm.com/download/win

### Paso 2: Abrir PowerShell en tu carpeta
```powershell
# Navega a tu carpeta
cd "c:\Users\USUARIO\Desktop\TOTAL NUEVO 2.0\sena  2.0\ADSO\JAVA\DIACUA VIVA"

# Verifica que estás en la carpeta correcta
Get-Location
```

### Paso 3: Inicializar Git
```powershell
# Inicializar repositorio
git init

# Agregar todos los archivos
git add .

# Hacer primer commit
git commit -m "DIACUA VIVA - Presentación inicial con logo y formularios"

# Verificar status
git status
```

### Paso 4: Subir a GitHub

#### 4a. Crear repositorio en GitHub
1. Ve a https://github.com
2. Sign in / Sign up
3. Click "New repository" (botón verde)
4. Repository name: `diacua-viva`
5. Description: "Proyecto de investigación y gestión cultural para Villavicencio"
6. ✅ Public
7. ❌ NO marcar "Initialize with README" (ya lo tienes)
8. Click "Create repository"

#### 4b. Conectar y subir
```powershell
# Reemplaza TU_USUARIO con tu nombre de usuario de GitHub
git remote add origin https://github.com/TU_USUARIO/diacua-viva.git

# Renombrar branch a main (estándar actual)
git branch -M main

# Subir código
git push -u origin main

# Te pedirá usuario y contraseña de GitHub
```

### Paso 5: Conectar con Vercel

1. **Crear cuenta en Vercel:**
   - Ve a https://vercel.com
   - Click "Sign Up"
   - Selecciona "Continue with GitHub"
   - Autoriza a Vercel

2. **Importar proyecto:**
   - Dashboard de Vercel → "Add New..." → "Project"
   - En "Import Git Repository" verás `diacua-viva`
   - Click "Import"

3. **Configurar (si es necesario):**
   - Framework Preset: **Other** (dejar como está)
   - Root Directory: `./` (dejar como está)
   - Build Command: (dejar vacío)
   - Output Directory: (dejar vacío)
   - Click "Deploy"

4. **¡Listo!** En 1-2 minutos tendrás:
   ```
   https://diacua-viva.vercel.app
   o
   https://diacua-viva-TU_USUARIO.vercel.app
   ```

### Paso 6: Dominio personalizado (Opcional)

1. **Comprar dominio:**
   - Namecheap: https://www.namecheap.com
   - Buscar: `diacuaviva.org` (~$10/año)
   - Comprar

2. **Conectar en Vercel:**
   - Dashboard → Settings → Domains
   - Add: `diacuaviva.org` y `www.diacuaviva.org`
   - Copiar los DNS que te da Vercel

3. **Actualizar DNS en Namecheap:**
   - Domain List → Manage → Advanced DNS
   - Agregar los registros que te dio Vercel
   - Esperar 1-24 horas (usualmente 10-30 minutos)

---

## 📝 OPCIÓN 2: GitHub Pages (Alternativa)

### Ventaja: 100% gratis sin configuración extra
### Desventaja: Solo archivos estáticos, sin servidor

```powershell
# Pasos 1-4 iguales a arriba (Git + GitHub)

# Paso 5: Activar GitHub Pages
# 1. Ve a tu repositorio en GitHub
# 2. Settings → Pages (menú izquierdo)
# 3. Source: "Deploy from a branch"
# 4. Branch: main / (root)
# 5. Save

# Tu sitio estará en:
# https://TU_USUARIO.github.io/diacua-viva/
```

---

## 🔄 ACTUALIZAR EL SITIO (Después del primer despliegue)

### Cuando hagas cambios en `presentacion.html`:

```powershell
# 1. Navegar a la carpeta
cd "c:\Users\USUARIO\Desktop\TOTAL NUEVO 2.0\sena  2.0\ADSO\JAVA\DIACUA VIVA"

# 2. Ver qué archivos cambiaron
git status

# 3. Agregar cambios
git add .

# 4. Hacer commit con mensaje descriptivo
git commit -m "Actualizar URLs de formularios Google Forms"

# 5. Subir cambios
git push

# ¡Listo! Vercel desplegará automáticamente en 1-2 minutos
```

---

## 🛠️ COMANDOS GIT ÚTILES

### Ver historial de cambios
```powershell
git log --oneline
```

### Ver diferencias antes de commit
```powershell
git diff presentacion.html
```

### Deshacer cambios (¡CUIDADO!)
```powershell
# Deshacer cambios en un archivo (volver a la última versión)
git checkout -- presentacion.html

# Deshacer último commit (pero mantener cambios)
git reset HEAD~1
```

### Crear branch para experimentar
```powershell
# Crear y cambiar a nueva rama
git checkout -b experimento

# Hacer cambios y commits
git add .
git commit -m "Probando nuevo diseño"

# Volver a main
git checkout main

# Fusionar si funcionó
git merge experimento
```

---

## 📊 VERIFICAR DESPLIEGUE

### Checklist post-despliegue:

```powershell
# 1. Abrir tu sitio
# https://diacua-viva.vercel.app (o tu URL)

# 2. Probar en diferentes dispositivos:
# - Desktop (Chrome, Firefox)
# - Móvil (Safari iOS, Chrome Android)

# 3. Verificar:
# ✅ Logo se ve correctamente
# ✅ Video se reproduce
# ✅ Todos los links funcionan
# ✅ Formularios abren (aunque tengan URLs temporales)
# ✅ Acordeones se expanden/contraen
# ✅ Modales se abren/cierran
# ✅ Responsive (prueba cambiando tamaño de ventana)
```

---

## 🔐 CREDENCIALES A GUARDAR

Crea un archivo **PRIVADO** (NO subir a Git) con:

```
ARCHIVO: credenciales_privadas.txt (agregar a .gitignore)

=== GITHUB ===
Usuario: TU_USUARIO
URL repo: https://github.com/TU_USUARIO/diacua-viva

=== VERCEL ===
URL producción: https://diacua-viva.vercel.app
Dashboard: https://vercel.com/TU_USUARIO/diacua-viva

=== DOMINIO (si compraste) ===
Registrador: Namecheap
Dominio: diacuaviva.org
Login: email@example.com

=== GOOGLE FORMS ===
Formulario Voluntarios: https://docs.google.com/forms/d/...
Formulario Propuestas: https://docs.google.com/forms/d/...
Formulario Patrocinios: https://docs.google.com/forms/d/...

=== EMAIL ===
Email: contacto@diacuaviva.org
Servicio: Google Workspace / Gmail
```

---

## 🚨 SOLUCIÓN DE PROBLEMAS

### Error: "git not recognized"
```powershell
# Instala Git desde https://git-scm.com
# Reinicia PowerShell después de instalar
```

### Error: "Permission denied (publickey)"
```powershell
# Usa HTTPS en lugar de SSH
git remote set-url origin https://github.com/TU_USUARIO/diacua-viva.git
```

### Error: "Updates were rejected"
```powershell
# Alguien más hizo cambios, primero descárgalos
git pull origin main
# Luego intenta push de nuevo
git push
```

### El sitio no actualiza en Vercel
```powershell
# 1. Verifica que el push funcionó
git log --oneline

# 2. Ve al dashboard de Vercel
# Deployments → Debería mostrar "Building"

# 3. Si falló, revisa los logs en Vercel

# 4. Forzar redespliegue en Vercel:
# Deployments → ... (3 puntos) → Redeploy
```

### Video no se reproduce
```
# Verifica que DIACUA VIV.mp4 está en la misma carpeta
# Verifica el nombre exacto (con espacio)
# Si cambias nombre, actualiza en presentacion.html línea ~200
```

---

## 📱 COMPARTIR EN REDES SOCIALES

### Post sugerido para lanzamiento:

```
🌳 ¡Lanzamos DIACUA VIVA! 

Proyecto de investigación y gestión cultural para Villavicencio.

🔍 Diagnosticamos el metabolismo cultural de nuestra ciudad
🤝 Buscamos voluntarios, investigadores, patrocinadores
💡 Recibimos propuestas comunitarias

👉 Conoce más y súmate: https://diacua-viva.vercel.app

#Villavicencio #CulturaViva #DiacuaViva #GestiónCultural 
#Meta #Colombia #CulturaComunitaria
```

### Imagen para compartir:
- Crear screenshot del hero (logo + video)
- O usar logo.png
- Dimensiones ideales:
  - Instagram: 1080x1080px (cuadrado)
  - Facebook: 1200x630px
  - Twitter: 1200x675px

---

## ✅ CHECKLIST FINAL

Antes de anunciar públicamente:

- [ ] Sitio desplegado en Vercel ✅
- [ ] Probado en móvil y desktop ✅
- [ ] Logo y video funcionan ✅
- [ ] Al menos 1 Google Form creado y vinculado ✅
- [ ] Email de contacto configurado ✅
- [ ] Google Analytics instalado (opcional)
- [ ] Imágenes optimizadas (logo < 500KB)
- [ ] Post de lanzamiento preparado ✅
- [ ] Lista de contactos para compartir ✅

---

## 🎉 ¡FELICITACIONES!

Tu proyecto está en línea. Ahora el trabajo real comienza:
- Promocionar en redes
- Recolectar primeras respuestas
- Responder a interesados
- Iterar y mejorar

**¡Éxito con DIACUA VIVA!** 🌳
