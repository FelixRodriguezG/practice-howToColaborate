# 🛠️ Guía para colaborar en un proyecto en GitHub

## 👥 Escoge tu flujo de colaboración

Puedes colaborar en un repositorio de dos formas:

- ✅ **Usando un Fork**: si **no tienes acceso directo** al repositorio original.
- 🛠️ **Colaborando directamente**: si **eres colaborador/a** o miembro del equipo del repositorio original.

---

## 🔁 Opción A — Colaborar usando un Fork

> Ideal cuando no tienes permisos de escritura en el repositorio original.

### 1. Haz un Fork del repositorio
Haz clic en **Fork** para crear una copia del repositorio original en tu cuenta de GitHub.

### 2. Clona tu repositorio

```bash
git clone https://github.com/TuUsuario/NombreRepo.git
cd NombreRepo
```

### 3. Añade el repositorio original como remoto (`upstream`)

```bash
git remote add upstream https://github.com/UsuarioOriginal/NombreRepo.git
git remote -v
```

### 4. Sincroniza tu rama `main` (o `master`)

```bash
git checkout main
git pull --rebase upstream main
```

### 5. Crea una nueva rama para tus cambios

```bash
git checkout -b feature/nombre-de-tu-rama
```

### 6. Realiza cambios, añade y haz commit

```bash
git add .
git commit -m "Descripción clara de los cambios"
```

### 7. Sube tu rama a tu fork

```bash
git push origin feature/nombre-de-tu-rama
```

### 8. Crea un Pull Request desde GitHub

Desde tu repositorio, haz clic en **Compare & pull request**, añade una descripción y envíalo.

---

## 🔧 Opción B — Colaborar directamente en el repositorio original

> Este flujo es válido si tienes permisos para **crear ramas y hacer push** directamente en el repositorio del equipo.

### 1. Clona el repositorio original

```bash
git clone https://github.com/Organizacion/NombreRepo.git
cd NombreRepo
```

### 2. Asegúrate de estar actualizado

```bash
git checkout main
git pull origin main
```

(O `master`, si es la rama principal.)

### 3. Crea una nueva rama para tu trabajo

```bash
git checkout -b feature/nombre-de-tu-rama
```

### 4. Realiza los cambios necesarios

Guarda, añade y haz commit de tus archivos modificados:

```bash
git add .
git commit -m "Implementa nueva funcionalidad X"
```

### 5. Sube la rama al repositorio

```bash
git push origin feature/nombre-de-tu-rama
```

### 6. Crea un Pull Request desde GitHub

En la pestaña **Pull Requests**, haz clic en **New Pull Request**, selecciona tu rama y sigue los pasos para enviar la solicitud.

---

## 🧼 Consejo final: ¡No trabajes nunca directamente en `main`!

Siempre crea una rama específica para tus cambios. Esto facilita las revisiones, evita conflictos y mantiene el historial limpio.

