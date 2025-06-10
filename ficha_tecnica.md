# Git - Comandos Básicos para Desarrollo de Software

## 1. Fuentes de información

- **Documentación oficial de Git**: https://git-scm.com/doc
- **Pro Git Book**: https://git-scm.com/book (Libro oficial gratuito)
- **GitHub Docs**: https://docs.github.com/
- **Git Reference**: https://git-scm.com/docs

## 2. Definiciones

### ¿Qué es Git?
Git es un **sistema de control de versiones distribuido** creado por Linus Torvalds en 2005. Permite:
- Rastrear cambios en archivos a lo largo del tiempo
- Colaborar con múltiples desarrolladores
- Mantener un historial completo de modificaciones
- Crear ramas (branches) para desarrollo paralelo
- Fusionar cambios de diferentes fuentes

### Conceptos Fundamentales

**Repository (Repositorio)**: Directorio que contiene todos los archivos del proyecto y su historial de versiones.

**Commit**: Instantánea de los cambios realizados en el repositorio en un momento específico.

**Branch (Rama)**: Línea independiente de desarrollo que permite trabajar en características diferentes simultáneamente.

**Merge**: Proceso de combinar cambios de diferentes ramas.

**Clone**: Copia completa de un repositorio remoto a tu máquina local.

**Push**: Enviar cambios locales a un repositorio remoto.

**Pull**: Descargar cambios desde un repositorio remoto.

### Flujo de Trabajo en Git

```
Working Directory → Staging Area → Repository
     (git add)         (git commit)
```

🔹 **Working Directory**: Archivos en tu proyecto actual  
🔹 **Staging Area**: Cambios preparados para confirmarse  
🔹 **Repository**: Historial de cambios confirmados  

## 3. Demostración práctica

### Instalación de Git

**Windows**: Descargar desde https://git-scm.com/download/win  
**macOS**: `brew install git` o descargar desde el sitio oficial  
**Linux (Ubuntu/Debian)**: `sudo apt install git`  
**Linux (CentOS/RHEL)**: `sudo yum install git`

### Configuración Inicial

```bash
# Configurar nombre de usuario
git config --global user.name "Tu Nombre"

# Configurar email
git config --global user.email "tu.email@ejemplo.com"

# Verificar configuración
git config --list
```

### Creación de un Repositorio

```bash
# Crear nuevo repositorio local
git init nombre-proyecto
cd nombre-proyecto

# O inicializar en directorio existente
cd proyecto-existente
git init
```

### Comandos Básicos Esenciales

#### Agregar y Confirmar Cambios
```bash
# Agregar archivo específico al staging area
git add archivo.txt

# Agregar todos los archivos modificados
git add .

# Confirmar cambios con mensaje
git commit -m "Descripción de los cambios"

# Agregar y confirmar en un solo paso
git commit -am "Mensaje del commit"
```

#### Ver Estado del Repositorio
```bash
# Ver estado actual
git status

# Ver historial de commits
git log

# Ver historial resumido
git log --oneline

# Ver diferencias antes de hacer commit
git diff
```

#### Trabajar con Ramas
```bash
# Crear nueva rama
git branch nombre-rama

# Cambiar a una rama
git checkout nombre-rama

# Crear y cambiar a nueva rama
git checkout -b nombre-rama

# Listar todas las ramas
git branch

# Fusionar rama actual con otra
git merge nombre-rama
```

#### Repositorios Remotos
```bash
# Clonar repositorio remoto
git clone https://github.com/usuario/repositorio.git

# Agregar repositorio remoto
git remote add origin https://github.com/usuario/repositorio.git

# Enviar cambios al repositorio remoto
git push origin main

# Descargar cambios del repositorio remoto
git pull origin main
```

### Ejemplo Práctico Completo

```bash
# 1. Crear proyecto
mkdir mi-proyecto
cd mi-proyecto
git init

# 2. Crear archivo
echo "# Mi Proyecto" > README.md

# 3. Agregar al staging area
git add README.md

# 4. Confirmar cambios
git commit -m "Primer commit: agregar README"

# 5. Crear nueva rama para característica
git checkout -b nueva-caracteristica

# 6. Modificar archivo
echo "Nueva línea de código" >> README.md

# 7. Confirmar cambios en la rama
git add README.md
git commit -m "Agregar nueva característica"

# 8. Volver a rama principal
git checkout main

# 9. Fusionar cambios
git merge nueva-caracteristica
```

## 4. Recomendaciones de uso

### Buenas Prácticas

**Commits Frecuentes**: Realiza commits pequeños y frecuentes con mensajes descriptivos.

**Mensajes Claros**: Usa mensajes de commit que expliquen qué y por qué se hizo el cambio.
- ✅ "Corregir validación de email en formulario de registro"
- ❌ "Arreglar bug"

**Uso de Ramas**: Crea ramas para cada nueva característica o corrección.

**Revisar Antes de Commit**: Usa `git status` y `git diff` antes de confirmar cambios.

### Flujo de Trabajo Recomendado

1. **Actualizar**: `git pull` antes de comenzar a trabajar
2. **Crear rama**: `git checkout -b feature/nueva-funcionalidad`
3. **Desarrollar**: Hacer cambios y commits frecuentes
4. **Probar**: Verificar que todo funciona correctamente
5. **Fusionar**: Cambiar a main y hacer `git merge`
6. **Actualizar remoto**: `git push origin main`
7. **Limpiar**: Eliminar rama local si ya no se necesita

### Comandos de Emergencia

```bash
# Deshacer último commit (mantener cambios)
git reset --soft HEAD~1

# Deshacer cambios no confirmados
git checkout -- archivo.txt

# Ver qué cambió en un commit específico
git show commit-hash

# Buscar en el historial
git log --grep="palabra-clave"
```

## 5. Recursos de aprendizaje

### Documentación y Tutoriales
- **Git Handbook**: https://guides.github.com/introduction/git-handbook/
- **Learn Git Branching**: https://learngitbranching.js.org/ (Tutorial interactivo)
- **Git Cheat Sheet**: https://education.github.com/git-cheat-sheet-education.pdf

### Herramientas Visuales
- **GitKraken**: Cliente Git con interfaz gráfica
- **GitHub Desktop**: Cliente oficial de GitHub
- **VS Code**: Editor con excelente integración Git

### Práctica
- **GitHub**: Crear cuenta y repositorios de práctica
- **GitLab**: Alternativa para proyectos privados gratuitos
- **Bitbucket**: Otra opción para equipos pequeños

### Comandos de Referencia Rápida

| Comando | Descripción |
|---------|-------------|
| `git init` | Inicializar repositorio |
| `git add .` | Agregar todos los archivos |
| `git commit -m "msg"` | Confirmar cambios |
| `git status` | Ver estado |
| `git log` | Ver historial |
| `git branch` | Listar ramas |
| `git checkout -b rama` | Crear y cambiar rama |
| `git merge rama` | Fusionar rama |
| `git push origin main` | Enviar a remoto |
| `git pull origin main` | Descargar de remoto |

### Recursos Adicionales para Profundizar
- **Pro Git Book** (Libro completo gratuito)
- **Git Magic** (Guía avanzada)
- **Git Immersion** (Tutorial paso a paso)
