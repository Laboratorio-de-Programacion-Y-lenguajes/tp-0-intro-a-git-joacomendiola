[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/PpKsQdkE)
[![Open in Codespaces](https://classroom.github.com/assets/launch-codespace-2972f46106e565e64193e422d61a12cf1da4916b45550586e14ef0a7c637dd04.svg)](https://classroom.github.com/open-in-codespaces?assignment_repo_id=23173743)
# TP 0: Git & GitHub Flow - Glosario Colaborativo 🐍

¡Bienvenido/a a **Laboratorio de Programación y Lenguajes**!  
Este trabajo práctico inicial tiene como objetivo que domines las herramientas que usaremos durante todo el cuatrimestre para construir tus aplicaciones: **Git** y **GitHub**.

---

## 🎯 Objetivos
1. Configurar tu entorno de desarrollo local.
2. Implementar el flujo de trabajo profesional (**Feature Flow**).
3. Resolver conflictos de fusión (*merge conflicts*).
4. Asegurar que tu código sea ejecutable en **Python 3.13+**.

---

## 🛠️ Requisitos Previos
* **Git** instalado (`git --version`).
* **Python 3.13** o superior instalado (`python --version` o `python3 --version`).
* Un editor de código (recomendamos **VS Code** o **PyCharm**).

---

## 🚀 El Desafío: Paso a Paso

### 1. Clonar el repositorio
Copiá la URL de este repositorio y ejecutá en tu terminal:

```bash
git clone [https://github.com/if009-untdf/if009-tp0-git-](https://github.com/if009-untdf/if009-tp0-git-)[tu-usuario].git
cd if009-tp0-git-[tu-usuario]
```

### 2. Crear una rama de característica (Feature Branch)
En esta materia nunca trabajaremos directamente sobre `main`. Creá una rama para tu aporte:

```bash
git checkout -b feature-nuevo-termino
```

### 3. Modificar el código
Abrí el archivo `glosario.py` y realizá los siguientes cambios:
1. Creá una nueva función con un nombre descriptivo (ej: `definicion_django()`).
2. Dentro de la función, definí un término técnico relacionado con la materia (ORM, MVT, Middleware, VirtualEnv, etc.).
3. Llamá a tu función al final del bloque `if __name__ == "__main__":`.

### 4. Commit y Push
Guardá tus cambios en el historial de Git usando mensajes semánticos:

```bash
git add glosario.py
git commit -m "feat: agrega definicion de [Tu Termino]"
git push origin feature-nuevo-termino
```

### 5. Abrir un Pull Request (PR)
1. Andá a la pestaña **Pull Requests** en GitHub.
2. Creá un nuevo PR desde tu rama hacia `main`.
3. Esperá el feedback de Iván o Matías en la sección de comentarios de tu PR.

---

## ⚠️ Fase de Conflicto (Simulación)
Durante el desarrollo, es probable que la rama `main` del servidor avance. Deberás integrar esos cambios en tu rama local y resolver el conflicto que prepararon los profes:

1. Volver a main y actualizar: `git checkout main` y luego `git pull origin main`.
2. Volver a tu rama: `git checkout feature-nuevo-termino`.
3. Intentar el merge: `git merge main`.
4. **Resolución:** Abrí `glosario.py` en tu editor, decidí qué porción de código conservar, eliminá las marcas de Git (`<<<<`, `====`, `>>>>`), guardá el archivo y hacé un nuevo commit.

---

## ✅ Verificación
Antes de avisar que terminaste, asegurate de que el script funciona correctamente:

```bash
python glosario.py
```

*(Debería mostrar la bienvenida, los términos base de los profes y el término que vos agregaste).*

---

> **Tip:** Si tenés dudas con un comando o no sabés dónde estás parado, ejecutá `git status`. Es tu mejor amigo.