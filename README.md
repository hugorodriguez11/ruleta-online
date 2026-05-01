# RuletaOnline — Guía de publicación e indexación

## Archivos del proyecto

```
ruletaonline/
├── index.html     ← La página completa
├── robots.txt     ← Le dice a Google que indexe la página
├── sitemap.xml    ← Mapa del sitio para Google
└── README.md
```

---

## Paso 1 — Subir a Vercel

### Opción A: Arrastrar archivos (más fácil, sin GitHub)
1. Ve a https://vercel.com y crea cuenta gratis
2. En el dashboard haz clic en **"Add New Project"**
3. Elige **"Browse"** o arrastra la carpeta `ruletaonline`
4. Vercel detecta que es un sitio estático y lo publica automáticamente
5. Te dará una URL como `ruletaonline-xyz.vercel.app`

### Opción B: Con GitHub (recomendado para actualizaciones fáciles)
1. Crea cuenta en https://github.com
2. Crea repositorio nuevo llamado `ruletaonline`
3. Sube los archivos
4. En Vercel importa ese repositorio
5. Cada vez que cambies algo en GitHub, Vercel se actualiza solo

---

## Paso 2 — Actualizar la URL en los archivos

Una vez que Vercel te dé tu URL real, actualiza estas líneas:

**En `index.html`** busca y reemplaza `ruletaonline.vercel.app` con tu URL real:
- línea `<link rel="canonical" ...>`
- líneas `<meta property="og:url" ...>`
- líneas de Schema.org

**En `robots.txt`:**
```
Sitemap: https://TU-URL-REAL.vercel.app/sitemap.xml
```

**En `sitemap.xml`:**
```xml
<loc>https://TU-URL-REAL.vercel.app/</loc>
```

---

## Paso 3 — Registrar en Google Search Console

1. Ve a https://search.google.com/search-console
2. Inicia sesión con tu cuenta de Google
3. Clic en **"Agregar propiedad"**
4. Elige **"Prefijo de URL"** e ingresa tu URL de Vercel
5. Google te pedirá verificar que eres el dueño — elige la opción de **"Etiqueta HTML"**
6. Te dará un código como: `<meta name="google-site-verification" content="XXXXXXX" />`
7. Pega ese código en el `<head>` del `index.html`, vuelve a subir el archivo
8. En Search Console haz clic en **"Verificar"**

### Una vez verificado:
- Ve a **"Sitemaps"** en el menú izquierdo
- Escribe `sitemap.xml` y haz clic en **"Enviar"**
- Google empezará a rastrear e indexar tu página en los próximos días

---

## Paso 4 — Google AdSense (cuando quieras monetizar)

Requisito previo: tener dominio propio (no funciona con `.vercel.app`)

1. Compra un dominio en https://porkbun.com (~$10/año)
2. Conéctalo a Vercel: Vercel → tu proyecto → Settings → Domains
3. Ve a https://adsense.google.com y solicita aprobación
4. Google te dará un código para pegar en el `<head>` del `index.html`
5. Una vez aprobado, Google pone anuncios automáticamente

---

## Palabras clave objetivo (SEO)

La página ya está optimizada para estas búsquedas:
- "ruleta online gratis"
- "ruleta virtual"
- "amigo secreto online"
- "intercambio de regalos"
- "generador de números aleatorios"
- "sorteo online gratis"
- "números al azar"

---

## Costos

| Servicio | Costo |
|----------|-------|
| Vercel hosting | Gratis |
| Google Search Console | Gratis |
| Dominio (para AdSense) | ~$10/año |
| Google AdSense | Gratis (te pagan a ti) |
