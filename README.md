# MOLDES - Planilla Web

## Descripción
Página web para planilla de moldes desarrollada en HTML y publicada en GitHub Pages.

## 🌐 URL de la página
**https://jordymg.github.io/MOLDES/**

---

## 📋 Proceso de Configuración - Documentación Completa

### 1. Configuración Inicial del Repositorio Git

```bash
# Inicializar repositorio local
git init

# Configurar usuario Git para este proyecto
git config user.name "jordymg"
git config user.email "giojordy@gmail.com"
```

### 2. Creación del Repositorio en GitHub

**Pasos manuales realizados:**
1. Ir a: https://github.com/new
2. **Repository name:** `MOLDES`
3. **Visibilidad:** Public (necesario para GitHub Pages gratuito)
4. **NO seleccionar:** README, .gitignore, ni licencia
5. Click en **Create repository**

### 3. Primer Commit y Subida de Archivos

```bash
# Agregar archivo HTML al staging area
git add planilla_moldes_V1.0.html

# Crear primer commit
git commit -m "feat: add initial moldes planilla HTML page"

# Cambiar rama principal a 'main' (estándar actual)
git branch -M main
```

### 4. Configuración de Remote y Push

**Problema inicial con SSH:**
- GitHub sugirió usar SSH: `git@github.com:jordymg/MOLDES.git`
- Error: `Host key verification failed` (falta configuración de llaves SSH)

**Solución - Cambio a HTTPS:**
```bash
# Agregar remote con SSH (inicial - falló)
git remote add origin git@github.com:jordymg/MOLDES.git

# Cambiar a HTTPS (solución exitosa)
git remote set-url origin https://github.com/jordymg/MOLDES.git

# Push exitoso
git push -u origin main
```

### 5. Optimización para GitHub Pages

**Problema:** GitHub Pages busca `index.html` como página principal por defecto.

**Solución:**
```bash
# Renombrar archivo para GitHub Pages
git mv planilla_moldes_V1.0.html index.html

# Commit del cambio
git commit -m "refactor: rename to index.html for GitHub Pages"

# Push final
git push
```

### 6. Activación de GitHub Pages

**Pasos manuales:**
1. Ir a repositorio: https://github.com/jordymg/MOLDES
2. **Settings** → **Pages** (menú lateral)
3. **Source:** Deploy from a branch
4. **Branch:** main
5. **Folder:** / (root)
6. **Save**

---

## 🔧 Comandos Utilizados (Resumen)

```bash
# Configuración inicial
git init
git config user.name "jordymg"
git config user.email "giojordy@gmail.com"

# Gestión de archivos
git add planilla_moldes_V1.0.html
git commit -m "feat: add initial moldes planilla HTML page"
git branch -M main

# Configuración remota
git remote add origin https://github.com/jordymg/MOLDES.git
git push -u origin main

# Optimización para GitHub Pages
git mv planilla_moldes_V1.0.html index.html
git commit -m "refactor: rename to index.html for GitHub Pages"
git push
```

## 🚨 Problemas Encontrados y Soluciones

### 1. **SSH vs HTTPS**
- **Problema:** GitHub sugiere SSH por defecto, pero requiere configuración de llaves
- **Solución:** Cambiar a HTTPS para simplificar el proceso

### 2. **Configuración de Usuario Git**
- **Problema:** Git no tenía usuario configurado
- **Solución:** Configurar user.name y user.email antes del primer commit

### 3. **Nombre de Archivo para GitHub Pages**
- **Problema:** GitHub Pages busca `index.html` como página principal
- **Solución:** Renombrar `planilla_moldes_V1.0.html` a `index.html`

## 📁 Estructura del Proyecto

```
MOLDES/
├── README.md           # Este archivo de documentación
├── index.html          # Página principal (antes: planilla_moldes_V1.0.html)
└── .git/              # Carpeta de control de versiones Git
```

## 🎯 Convenciones Utilizadas

### Commits
- **Formato:** Conventional Commits
- **Ejemplos:**
  - `feat: add initial moldes planilla HTML page`
  - `refactor: rename to index.html for GitHub Pages`

### Branching
- **Rama principal:** `main` (estándar moderno vs `master`)

---

## 🚀 Despliegue Automático

Una vez configurado GitHub Pages:
- **Automático:** Cada push a `main` actualiza la página
- **Tiempo:** ~1-5 minutos para ver cambios
- **URL estable:** https://jordymg.github.io/MOLDES/

## 👤 Autor
**jordymg** - giojordy@gmail.com

---
*Documentación creada: 2025-09-18*