# **Presentación: Git - Comandos Básicos**

## **Diapositiva 1: Portada**
### *Git - Comandos Básicos para Desarrollo de Software*
📌 Facultad de Ingeniería de Software  
🎤 Duración: 20 minutos  
👨‍🏫 Presentado por: [Tu Nombre]

---

## **Diapositiva 2: ¿Qué es Git?**
✅ **Git** es un sistema de control de versiones distribuido.  
✅ Permite gestionar cambios en el código fuente.  
✅ Creado por Linus Torvalds en 2005.  
✅ Ayuda a trabajar en equipo sin conflictos en el código.  

---

## **Diapositiva 3: Instalación de Git**
🔹 **Windows**: Descargar desde [git-scm.com](https://git-scm.com/)  
🔹 **Linux**: `sudo apt install git` (Ubuntu) o `sudo dnf install git` (Fedora)  
🔹 **MacOS**: `brew install git`

Verificar la instalación con:
```bash
 git --version
```

---

## **Diapositiva 4: Configuración Inicial**
Antes de usar Git, debemos configurarlo:
```bash
 git config --global user.name "Tu Nombre"
 git config --global user.email "tuemail@example.com"
```
Ver configuración:
```bash
 git config --list
```

---

## **Diapositiva 5: Creación de un Repositorio**
📌 **Iniciar un repositorio local**:
```bash
 git init
```
📌 **Clonar un repositorio existente**:
```bash
 git clone URL_DEL_REPO
```
Ejemplo:
```bash
 git clone https://github.com/usuario/repositorio.git
```

---

## **Diapositiva 6: Flujo de Trabajo en Git**
🔹 **Working Directory** → Archivos en tu proyecto.  
🔹 **Staging Area** → Cambios preparados para confirmarse.  
🔹 **Repository** → Historial de cambios confirmados.  

---

## **Diapositiva 7: Agregar y Confirmar Cambios**
📌 **Agregar archivos al staging area**:
```bash
 git add nombre_archivo.txt
```
O agregar todos los cambios:
```bash
 git add .
```
📌 **Confirmar cambios con un mensaje**:
```bash
 git commit -m "Mensaje descriptivo del cambio"
```

---

## **Diapositiva 8: Ver Estado del Repositorio**
📌 **Ver archivos modificados, sin seguimiento, o en staging area**:
```bash
 git status
```
📌 **Ver historial de cambios confirmados**:
```bash
 git log --oneline
```

---

## **Diapositiva 9: Trabajando con Ramas**
📌 **Ver ramas existentes**:
```bash
 git branch
```
📌 **Crear una nueva rama**:
```bash
 git branch nueva_rama
```
📌 **Cambiar a otra rama**:
```bash
 git checkout nueva_rama
```
📌 **Crear y cambiar a una rama nueva directamente**:
```bash
 git checkout -b nueva_rama
```

---

## **Diapositiva 10: Subir Cambios a un Repositorio Remoto**
📌 **Agregar un repositorio remoto**:
```bash
 git remote add origin URL_DEL_REPO
```
📌 **Enviar cambios al repositorio remoto**:
```bash
 git push origin main
```
📌 **Descargar cambios de otros colaboradores**:
```bash
 git pull origin main
```

---

## **Diapositiva 11: Fusionar Ramas**
📌 **Unir cambios de una rama a otra**:
```bash
 git merge rama_a_unir
```
📌 **Resolver conflictos si los hay**: Editar los archivos con conflictos y confirmar los cambios.

---

## **Diapositiva 12: Deshacer Cambios**
📌 **Eliminar cambios no confirmados**:
```bash
 git checkout -- nombre_archivo.txt
```
📌 **Revertir el último commit**:
```bash
 git revert HEAD
```
📌 **Resetear un commit (¡Usar con cuidado!)**:
```bash
 git reset --hard HEAD~1
```

---

## **Diapositiva 13: Ejemplo Práctico (5 minutos)**
1️⃣ Crear un repositorio con `git init`
2️⃣ Crear un archivo `index.html` y añadirlo con `git add .`
3️⃣ Confirmar cambios con `git commit -m "Primer commit"`
4️⃣ Crear una nueva rama `git checkout -b nueva_rama`
5️⃣ Editar `index.html` y hacer otro commit
6️⃣ Volver a `main` y hacer `git merge nueva_rama`
7️⃣ Subir el código a GitHub con `git push origin main`

---

## **Diapositiva 14: Conclusión y Preguntas**
✅ Git facilita el trabajo colaborativo en el desarrollo de software.  
✅ Sus comandos básicos permiten gestionar versiones de código de manera eficiente.  
✅ ¡Practicar con Git es clave para dominarlo!  

📢 **¿Preguntas?**  
📌 **Gracias por su atención.** 😃

