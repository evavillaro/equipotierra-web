# Web de Equipo Tierra

Sitio estático hecho con [Astro](https://astro.build). Landing + bitácora (blog) + páginas legales.

## Trabajar en local
```bash
npm install
npm run dev        # abre http://localhost:4321
```

## Cosas que editar tú (marcadas con TODO)
- `src/pages/index.astro` → las tres constantes de arriba: enlaces de Amazon
  (papel, Kindle) y de tu página de autora, cuando el libro esté publicado.

## Publicar una entrada del blog
Crea un archivo `.md` en `src/content/blog/` copiando el formato de
`bienvenida.md` y pon `borrador: false`. Cada push publica solo.

## Desplegar (Cloudflare Pages)
1. Sube este proyecto a un repositorio de GitHub.
2. En Cloudflare: **Workers & Pages → Create → Pages → Connect to Git** y elige el repo.
3. Framework preset: **Astro** (build `npm run build`, output `dist`). Deploy.
4. **Custom domains** → añade `equipotierra.com` y `www.equipotierra.com`
   (con el dominio en Cloudflare, los DNS se configuran solos).
5. El correo hola@ ya lo tienes con Email Routing — nada más que hacer.

Cada `git push` a la rama principal despliega automáticamente.
