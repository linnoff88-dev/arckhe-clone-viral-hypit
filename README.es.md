# Clone viral con tu rostro â€” Hypit + Claude Code + fal

[![Clone viral con tu rostro](guia/assets/banner-es.jpg)](https://linnoff88-dev.github.io/

**ðŸ‡§ðŸ‡· [PortuguÃªs](README.md) Â· ðŸ‡ºðŸ‡¸ [English](README.en.md) Â· ðŸ‡ªðŸ‡¸ [EspaÃ±ol](README.es.md)**

## QuÃ© es

Este es un kit gratuito de ARCKHÉ, en portuguÃ©s, con mensajes listos para pegar en Claude Code, plantillas de archivo,
checklists y una tabla de precios. EnseÃ±a a usar Hypit, una herramienta abierta de video, para rehacer un clip
corto con tu propio rostro, hacer la versiÃ³n en otro idioma o reemplazar a la persona por personajes ficticios. Sirve
para quien trabaja en marketing o crea contenido y quiere probar varias versiones de un anuncio sin volver a grabar. Necesitas
Claude Code, una cuenta en fal con algunos dÃ³lares de crÃ©dito, un clip tuyo y dos fotos de tu rostro.

## ðŸ“– GuÃ­a de uso

GuÃ­a completa (landing + paso a paso): **https://linnoff88-dev.github.io/

Video explicativo del kit: **https://linnoff88-dev.github.io/

## Para quiÃ©n es

- **Marketing y trÃ¡fico pago:** un clip se convierte en 5 a 10 versiones para probar con poco presupuesto antes de grabar de verdad.
- **Creadores de contenido:** la misma escena en otro idioma, o contigo en lugar del presentador, sin cÃ¡mara ni estudio.

## Las tres piezas

- **[Hypit](https://github.com/hypit-ai/hypit)** â€” herramienta abierta que corre dentro de Claude Code: lee tu video,
  planifica uno nuevo, pide a los modelos las imÃ¡genes y los clips, pone subtÃ­tulos y lo monta todo en tu computadora.
- **[fal](https://fal.ai)** â€” servicio donde corren los modelos de imagen y de video. Pagas por imagen y por segundo.
- **Claude Code** â€” tÃº pides en texto; Ã©l escribe los archivos de Hypit y muestra el plan y el precio antes de gastar.

**Hypit no viene en este repositorio.** Su licencia no permite empaquetarlo; el propio Claude lo instala desde el
repositorio oficial.

## Los 3 pasos

1. **Instalar** â€” un mensaje instala Hypit solo en el proyecto y conecta fal leyendo la `FAL_KEY` del entorno (unos 6 min).
2. **Rehacer con tu rostro** â€” primer y Ãºltimo cuadro con tu rostro, luego los 8 segundos entre ellos.
3. **Revisar, corregir y hacer versiones** â€” rostro, manos y texto; modelos premium; otro idioma; personajes ficticios.

Todo mensaje termina con **"MuÃ©strame el plan y el precio y no construyas nada."** â€” la frase que hace que Claude presupueste y
se detenga antes de gastar crÃ©dito.

## Precios (aproximados, segÃºn la tabla del 21/10/2026)

| QuÃ© | Costo aproximado |
|---|---|
| Primera versiÃ³n con tu rostro (Seedream 5 Lite + MiniMax H3 768p) | US$ 0,71 |
| VersiÃ³n premium (GPT Image 2.5 + MiniMax H3 Max 1080p) | ~US$ 2 |
| VersiÃ³n en otro idioma | ~US$ 2 |
| MiniMax H3 Recast 1080p (US$ 0,45/s) | US$ 3,60 por clip de 8 s Â· 7 versiones â‰ˆ US$ 25,20 Â· lote de 8 â‰ˆ US$ 28,80 |
| Higgsfield Genjutsu 1080p (US$ 1,632/s, comparaciÃ³n) | US$ 13,06 por clip Â· lote de 8 â‰ˆ US$ 104,50 |

El precio cambia: revisa las pÃ¡ginas antes de gastar. Recast y Genjutsu son modelos diferentes; solo se comparÃ³ el precio.
Fuentes y detalles en [`kit/05-precos-e-links.md`](kit/05-precos-e-links.md) (el kit estÃ¡ en portuguÃ©s).

## âš ï¸ La regla Ã©tica

**Usa solo tu rostro, o un rostro que tengas permiso por escrito para usar. Usa solo clips tuyos, o clips que
tengas derecho a rehacer.** Nada de personas famosas, de compaÃ±eros sin autorizaciÃ³n ni de videos ajenos. Los personajes del
kit son ficticios. Si el anuncio parece un testimonio, avisa que es contenido generado por IA.

## El proceso, de principio a fin

QuiÃ©n lo hace: ðŸ§  tÃº en Claude Code Â· âš™ï¸ Hypit/script Â· ðŸ¤– modelos en fal.

| # | Paso | QuÃ© hacer | QuiÃ©n lo hace |
|---|---|---|---|
| 1 | Preparar | Crear la carpeta del proyecto con `references/meu-clipe.mp4`, `rosto-1.jpg`, `rosto-2.jpg` (para personajes: `references/meu-ugc.mp4` y `characters.json` en la raÃ­z); Claude extrae los cuadros ([`kit/01-instalacao/1-o-que-precisa.md`](kit/01-instalacao/1-o-que-precisa.md)) | ðŸ§  |
| 2 | Guardar la clave | `export FAL_KEY="..."` en `~/.zshrc`/`~/.bashrc` (Windows: `setx FAL_KEY "..."`), abrir una terminal nueva; nunca en el chat ([`3-chave-fal-segura.md`](kit/01-instalacao/3-chave-fal-segura.md)) | ðŸ§  |
| 3 | Instalar | Pegar el mensaje de instalaciÃ³n en Claude Code ([`2-mensagem-de-instalacao.md`](kit/01-instalacao/2-mensagem-de-instalacao.md)); Hypit se instala con `npx skills add hypit-ai/hypit` (sin `-g`) y `@hypit/hypit` | ðŸ§  â†’ âš™ï¸ |
| 4 | Presupuestar el primer clip | Pegar el mensaje 1 ([`kit/02-mensagens/1-refazer-com-seu-rosto.md`](kit/02-mensagens/1-refazer-com-seu-rosto.md)); Claude escribe el `.svml` y muestra plan y precio | ðŸ§  â†’ âš™ï¸ |
| 5 | Generar las imÃ¡genes | Decir "puedes construir las imÃ¡genes"; los 2 cuadros con tu rostro salen de fal | ðŸ¤– |
| 6 | Revisar las imÃ¡genes | Rostro, manos, texto ([`kit/04-checklists/confira-antes-de-corrigir.md`](kit/04-checklists/confira-antes-de-corrigir.md)) | ðŸ§  |
| 7 | Generar el video | Decir "puedes construir el clip"; fal genera los 8 s y Hypit lo monta en tu computadora | ðŸ¤– â†’ âš™ï¸ |
| 8 | Corregir | Mensaje 2 (premium), presupuestar, revisar, construir | ðŸ§  â†’ ðŸ¤– |
| 9 | Hacer versiones | Mensaje 3 (otro idioma) y/o 4 (personajes ficticios del `characters.json`) | ðŸ§  â†’ ðŸ¤– â†’ âš™ï¸ |
| 10 | Probar | Correr las versiones como una sola prueba y quedarte con las que retienen mÃ¡s ([`teste-com-7-versoes.md`](kit/04-checklists/teste-com-7-versoes.md)) | ðŸ§  |

### DÃ³nde estÃ¡n la guÃ­a y el video de este repositorio

| Pieza | DÃ³nde | QuiÃ©n lo hace |
|---|---|---|
| GuÃ­a (PT/EN/ES) | `guia/index.html`, `guia/en/`, `guia/es/` â†’ https://linnoff88-dev.github.io/ | ðŸ§  (sesiÃ³n ARCKHÉ) â†’ âš™ï¸ GitHub Pages vÃ­a Actions |
| Video explicativo | archivo final fuera del repo; publicado como release `video-v1.0.0` (MP4 + SRT) y reproductor en `videos/` â†’ https://linnoff88-dev.github.io/ | âš™ï¸ `python3 scripts/publica.py` |

## Estructura del kit

```
kit/
â”œâ”€â”€ 00-COMECE-AQUI.md
â”œâ”€â”€ 01-instalacao/
â”‚   â”œâ”€â”€ 1-o-que-precisa.md
â”‚   â”œâ”€â”€ 2-mensagem-de-instalacao.md
â”‚   â””â”€â”€ 3-chave-fal-segura.md
â”œâ”€â”€ 02-mensagens/
â”‚   â”œâ”€â”€ 1-refazer-com-seu-rosto.md
â”‚   â”œâ”€â”€ 2-corrigir-com-premium.md
â”‚   â”œâ”€â”€ 3-nova-lingua.md
â”‚   â””â”€â”€ 4-um-clipe-varias-pessoas.md
â”œâ”€â”€ 03-modelos/
â”‚   â”œâ”€â”€ README.md
â”‚   â”œâ”€â”€ characters.json
â”‚   â”œâ”€â”€ hypit.runtime.example.json
â”‚   â”œâ”€â”€ refazer-com-seu-rosto.svml
â”‚   â””â”€â”€ recast-um-personagem.svml
â”œâ”€â”€ 04-checklists/
â”‚   â”œâ”€â”€ confira-antes-de-corrigir.md
â”‚   â”œâ”€â”€ 3-erros.md
â”‚   â””â”€â”€ teste-com-7-versoes.md
â””â”€â”€ 05-precos-e-links.md
guia/        pÃ¡gina de uso (PT, en/, es/)
videos/      reproductor del video explicativo
scripts/     publica.py (sube el video como release y genera el reproductor)
```

## Licencia de Hypit (resumen)

Hypit usa la "Hypit Open Source License" (Apache-2.0 con condiciones). En resumen: uso libre para tu trabajo y el
de tus clientes, tambiÃ©n comercial; no puede operarse como servicio alojado o multiinquilino para terceros; no se puede
vender ni empaquetar Hypit o derivados; debes mantener el nombre y el logo. Lo que creas es tuyo; los tÃ©rminos de los
proveedores de modelos siguen vigentes. Lee la licencia completa en https://github.com/hypit-ai/hypit.

## Licencia de este kit

[MIT](LICENSE) â€” vale solo para el texto, las plantillas de archivo y los scripts de ARCKHÉ.

---

Contenido abierto y gratuito de **[ARCKHÉ AI](https://ARCKHÉ AI)**.
