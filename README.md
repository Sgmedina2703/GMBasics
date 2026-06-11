# 🐾 GM Basics — Tu sitio web con panel de administración

Tu sitio vive en **GitHub Pages** (gratis, siempre en línea, sin servidor propio).
Lo editas desde **admin.html**, un panel donde cambias textos, precios, fotos y
todo lo demás. Al presionar **Publicar cambios**, la web se actualiza sola en 1–2 minutos.

## Archivos

| Archivo | Qué es |
|---|---|
| `index.html` | La página web (no la edites a mano) |
| `content.json` | Todo el contenido editable (lo maneja el panel) |
| `admin.html` | Tu panel de administración |
| `images/` | Carpeta donde el panel guarda las fotos que subes |

---

## Puesta en línea (solo se hace una vez, ~10 minutos)

### Paso 1 — Crear el repositorio
1. Entra a [github.com/new](https://github.com/new) con tu cuenta.
2. En **Repository name** escribe: `gm-basics` (o el nombre que quieras, sin espacios).
3. Deja la opción **Public** marcada y presiona **Create repository**.

### Paso 2 — Subir los archivos
1. En la página del repositorio nuevo, toca el enlace **uploading an existing file**
   (o el botón **Add file → Upload files**).
2. Arrastra estos archivos: `index.html`, `admin.html`, `content.json` y `README.md`.
3. Presiona el botón verde **Commit changes** y espera a que termine.

### Paso 3 — Activar GitHub Pages (esto pone la web en línea)
1. En el repositorio, ve a **Settings → Pages** (menú izquierdo).
2. En **Branch**, elige `main`, deja `/ (root)` y presiona **Save**.
3. Espera 1–2 minutos y recarga la página: arriba aparecerá la dirección de tu web,
   algo como `https://TU-USUARIO.github.io/gm-basics/`.
   **Esa es la dirección pública de tu sitio.** Guárdala.

### Paso 4 — Crear tu token (la "llave" para que el panel pueda publicar)
1. Entra a [github.com/settings/personal-access-tokens/new](https://github.com/settings/personal-access-tokens/new).
2. En **Token name** escribe: `panel-gm-basics`.
3. En **Expiration** elige **No expiration** (o 1 año; si expira, solo creas otro).
4. En **Repository access** elige **Only select repositories** y selecciona tu repositorio `gm-basics`.
5. Abre **Repository permissions** y busca **Contents** → cámbialo a **Read and write**.
6. Presiona **Generate token** y **copia el token** (empieza con `github_pat_`).
   ⚠️ Solo se muestra una vez. Pégalo en un lugar seguro y no lo compartas:
   quien lo tenga puede modificar tu sitio.

### Paso 5 — Conectar el panel
1. Abre el archivo `admin.html` con doble clic (se abre en tu navegador, funciona
   desde cualquier computadora; guárdate una copia).
2. Llena: tu usuario de GitHub, el nombre del repositorio (`gm-basics`) y pega el token.
3. Presiona **Conectar**. ¡Listo! Ya puedes editar todo.

---

## Uso diario

1. Abre `admin.html`.
2. Edita lo que quieras: productos, precios, fotos, textos, colecciones, GMKT, contacto.
3. Presiona **Publicar cambios**.
4. En 1–2 minutos los cambios aparecen en tu web (a veces el navegador guarda la
   versión vieja: recarga con `Ctrl+Shift+R` para verla al instante).

### Consejos
- **Fotos**: cualquier JPG o PNG sirve; el panel las optimiza automáticamente.
- Los cambios **no se ven en la web hasta que publicas**. Si cierras el panel sin
  publicar, se pierden (el panel te avisa antes de cerrar).
- El botón **Recargar** descarta tus cambios sin publicar y trae lo que está en línea.
- Si cambias de computadora, solo necesitas `admin.html` + tu usuario, repositorio y token.

### ¿Quieres tu propio dominio (ej. gmbasics.com)?
Se puede conectar un dominio comprado a GitHub Pages en **Settings → Pages → Custom domain**.

### Problemas comunes
- **"Token inválido"** → el token expiró o no tiene el permiso *Contents: Read and write*. Crea uno nuevo (Paso 4).
- **"No existe content.json"** → falta subir los archivos (Paso 2).
- **No veo mis cambios** → espera 2 minutos y recarga con `Ctrl+Shift+R`.
