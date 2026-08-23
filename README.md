# RML Image Optimizer

Aplicación web estática para optimizar fotografías de unidades de Multiservicios RML.

## Estructura

```text
rml-image-optimizer/
├── public/
│   └── index.html
├── .gitignore
├── package.json
├── README.md
└── wrangler.jsonc
```

## Cloudflare Workers

El proyecto está configurado para desplegar `public/` como Static Assets.

Comando de deploy:

```bash
npx wrangler deploy
```

También puedes usar:

```bash
npm install
npm run deploy
```

Para probar localmente:

```bash
npm install
npm run dev
```

## Uso del optimizador

1. Abre la aplicación.
2. Escribe el código de unidad, por ejemplo `R090` o `LM12`.
3. Selecciona la carpeta con las fotografías.
4. La principal debe llamarse exactamente `1.jpg`, `1.jpeg`, `1.png`, `1.webp`, `1.heic` o `1.heif`.
5. Las demás pueden tener cualquier nombre.
6. Pulsa **Procesar imágenes**.
7. Guarda la carpeta o descarga el ZIP.

La salida es:

```text
R090/
├── 01.webp
├── 02.webp
├── 03.webp
└── fotos.json
```

La carpeta puede copiarse directamente a:

```text
assets/img/unidades/
```

de la web principal.
