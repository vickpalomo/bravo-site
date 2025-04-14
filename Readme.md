# 🌐 Bravo Site - Proyecto Hugo

Este es un sitio generado con [Hugo](https://gohugo.io/), usando el tema [Ananke](https://github.com/theNewDynamic/gohugo-theme-ananke). Contiene formularios para consumir APIs y mostrar datos dinámicos como interés compuesto, chistes aleatorios y clima por ciudad.

---

## 📦 Requisitos

- [Go](https://go.dev/doc/install) (solo si quieres compilar Hugo desde fuente)
- [Hugo](https://gohugo.io/getting-started/installing/) (`v0.120.0` o superior)
- Git

---

## 🚀 Levantar el proyecto en local

1. Clona el repositorio:

```bash
git clone git@github.com:vickpalomo/bravo-site.git
cd bravo-site
```

2. Ejecuta el servidor de desarrollo:

```bash
hugo server
```

3. Abre tu navegador en:

```
http://localhost:1313
```

---

## 🛠 Estructura básica

```
.
├── config.toml          # Configuración del sitio
├── content/             # Contenido en Markdown
├── layouts/             # Plantillas personalizadas
├── static/              # Archivos estáticos (JS, CSS, imágenes)
├── themes/ananke/       # Tema usado
└── public/              # (Se genera al compilar el sitio)
```

---

## 🏗 Generar el sitio estático

```bash
hugo
```

Esto creará una carpeta `public/` con todos los archivos listos para producción.

---

## 🚢 Despliegue en GitHub Pages

Puedes desplegar el contenido del sitio en GitHub Pages usando la rama `gh-pages`.

### 📄 Configuración rápida:

1. Asegúrate de tener este valor en `config.toml`:

```toml
baseURL = "git@github.com:vickpalomo/bravo-site.git"
relativeURLs = true
```

2. Ejecuta:

```bash
hugo
cd public
git init
git remote add origin git@github.com:vickpalomo/bravo-site.git
git checkout -b gh-pages
git add .
git commit -m "Deploy Hugo site"
git push -f origin gh-pages
```

3. En GitHub:
   - Ve a **Settings → Pages**
   - Selecciona `gh-pages` como rama de despliegue

Tu sitio estará disponible en:

```
https://vickpalomo.github.io/bravo-site/
```

---

## 🌤 APIs usadas

- **Interés compuesto**: `POST /api/v1/interes-compuesto`
- **Chiste aleatorio**: `GET /api/v1/jokes/random`
- **Clima por ciudad**: `GET /api/v1/weather/{city}`

> Todas requieren API Key por cabecera: `x-api-key: 42IuTguij6KMv7KTV8MppveAkF6HGAC024d7Z4nKvNkMdKC7jSF3Aas0AitMqwer`

---

## 📸 Demo

(Agrega aquí un enlace o captura si tienes)

---

## 🧑‍💻 Autor

**@vickpalomo** – [GitHub](https://github.com/vickpalomo)

---

## 📝 Licencia

Este proyecto está bajo la licencia [MIT](LICENSE).