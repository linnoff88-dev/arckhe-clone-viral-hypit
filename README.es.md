# Clone viral con tu rostro ê¢â¬â Hypit + Claude Code + fal

[![Clone viral con tu rostro](guia/assets/banner-es.jpg)](https://linnoff88-dev.github.io/

**ê°Å¸â¡Â§ê°Å¸â¡Â· [PortuguêÂªs](README.md) êÂ· ê°Å¸â¡Âºê°Å¸â¡Â¸ [English](README.en.md) êÂ· ê°Å¸â¡Âªê°Å¸â¡Â¸ [EspaêÂ±ol](README.es.md)**

## QuêÂ© es

Este es un kit gratuito de ARCKHê, en portuguêÂ©s, con mensajes listos para pegar en Claude Code, plantillas de archivo,
checklists y una tabla de precios. EnseêÂ±a a usar Hypit, una herramienta abierta de video, para rehacer un clip
corto con tu propio rostro, hacer la versiêÂ³n en otro idioma o reemplazar a la persona por personajes ficticios. Sirve
para quien trabaja en marketing o crea contenido y quiere probar varias versiones de un anuncio sin volver a grabar. Necesitas
Claude Code, una cuenta en fal con algunos dêÂ³lares de crêÂ©dito, un clip tuyo y dos fotos de tu rostro.

## ê°Å¸ââ GuêÂ­a de uso

GuêÂ­a completa (landing + paso a paso): **https://linnoff88-dev.github.io/

Video explicativo del kit: **https://linnoff88-dev.github.io/

## Para quiêÂ©n es

- **Marketing y trêÂ¡fico pago:** un clip se convierte en 5 a 10 versiones para probar con poco presupuesto antes de grabar de verdad.
- **Creadores de contenido:** la misma escena en otro idioma, o contigo en lugar del presentador, sin cêÂ¡mara ni estudio.

## Las tres piezas

- **[Hypit](https://github.com/hypit-ai/hypit)** ê¢â¬â herramienta abierta que corre dentro de Claude Code: lee tu video,
  planifica uno nuevo, pide a los modelos las imêÂ¡genes y los clips, pone subtêÂ­tulos y lo monta todo en tu computadora.
- **[fal](https://fal.ai)** ê¢â¬â servicio donde corren los modelos de imagen y de video. Pagas por imagen y por segundo.
- **Claude Code** ê¢â¬â têÂº pides en texto; êÂ©l escribe los archivos de Hypit y muestra el plan y el precio antes de gastar.

**Hypit no viene en este repositorio.** Su licencia no permite empaquetarlo; el propio Claude lo instala desde el
repositorio oficial.

## Los 3 pasos

1. **Instalar** ê¢â¬â un mensaje instala Hypit solo en el proyecto y conecta fal leyendo la `FAL_KEY` del entorno (unos 6 min).
2. **Rehacer con tu rostro** ê¢â¬â primer y êÂºltimo cuadro con tu rostro, luego los 8 segundos entre ellos.
3. **Revisar, corregir y hacer versiones** ê¢â¬â rostro, manos y texto; modelos premium; otro idioma; personajes ficticios.

Todo mensaje termina con **"MuêÂ©strame el plan y el precio y no construyas nada."** ê¢â¬â la frase que hace que Claude presupueste y
se detenga antes de gastar crêÂ©dito.

## Precios (aproximados, segêÂºn la tabla del 21/10/2026)

| QuêÂ© | Costo aproximado |
|---|---|
| Primera versiêÂ³n con tu rostro (Seedream 5 Lite + MiniMax H3 768p) | US$ 0,71 |
| VersiêÂ³n premium (GPT Image 2.5 + MiniMax H3 Max 1080p) | ~US$ 2 |
| VersiêÂ³n en otro idioma | ~US$ 2 |
| MiniMax H3 Recast 1080p (US$ 0,45/s) | US$ 3,60 por clip de 8 s êÂ· 7 versiones ê¢â°Ë US$ 25,20 êÂ· lote de 8 ê¢â°Ë US$ 28,80 |
| Higgsfield Genjutsu 1080p (US$ 1,632/s, comparaciêÂ³n) | US$ 13,06 por clip êÂ· lote de 8 ê¢â°Ë US$ 104,50 |

El precio cambia: revisa las pêÂ¡ginas antes de gastar. Recast y Genjutsu son modelos diferentes; solo se comparêÂ³ el precio.
Fuentes y detalles en [`kit/05-precos-e-links.md`](kit/05-precos-e-links.md) (el kit estêÂ¡ en portuguêÂ©s).

## ê¢Å¡Â ê¯Â¸Â La regla êÂ©tica

**Usa solo tu rostro, o un rostro que tengas permiso por escrito para usar. Usa solo clips tuyos, o clips que
tengas derecho a rehacer.** Nada de personas famosas, de compaêÂ±eros sin autorizaciêÂ³n ni de videos ajenos. Los personajes del
kit son ficticios. Si el anuncio parece un testimonio, avisa que es contenido generado por IA.

## El proceso, de principio a fin

QuiêÂ©n lo hace: ê°Å¸Â§Â  têÂº en Claude Code êÂ· ê¢Å¡â¢ê¯Â¸Â Hypit/script êÂ· ê°Å¸Â¤â modelos en fal.

| # | Paso | QuêÂ© hacer | QuiêÂ©n lo hace |
|---|---|---|---|
| 1 | Preparar | Crear la carpeta del proyecto con `references/meu-clipe.mp4`, `rosto-1.jpg`, `rosto-2.jpg` (para personajes: `references/meu-ugc.mp4` y `characters.json` en la raêÂ­z); Claude extrae los cuadros ([`kit/01-instalacao/1-o-que-precisa.md`](kit/01-instalacao/1-o-que-precisa.md)) | ê°Å¸Â§Â  |
| 2 | Guardar la clave | `export FAL_KEY="..."` en `~/.zshrc`/`~/.bashrc` (Windows: `setx FAL_KEY "..."`), abrir una terminal nueva; nunca en el chat ([`3-chave-fal-segura.md`](kit/01-instalacao/3-chave-fal-segura.md)) | ê°Å¸Â§Â  |
| 3 | Instalar | Pegar el mensaje de instalaciêÂ³n en Claude Code ([`2-mensagem-de-instalacao.md`](kit/01-instalacao/2-mensagem-de-instalacao.md)); Hypit se instala con `npx skills add hypit-ai/hypit` (sin `-g`) y `@hypit/hypit` | ê°Å¸Â§Â  ê¢â â ê¢Å¡â¢ê¯Â¸Â |
| 4 | Presupuestar el primer clip | Pegar el mensaje 1 ([`kit/02-mensagens/1-refazer-com-seu-rosto.md`](kit/02-mensagens/1-refazer-com-seu-rosto.md)); Claude escribe el `.svml` y muestra plan y precio | ê°Å¸Â§Â  ê¢â â ê¢Å¡â¢ê¯Â¸Â |
| 5 | Generar las imêÂ¡genes | Decir "puedes construir las imêÂ¡genes"; los 2 cuadros con tu rostro salen de fal | ê°Å¸Â¤â |
| 6 | Revisar las imêÂ¡genes | Rostro, manos, texto ([`kit/04-checklists/confira-antes-de-corrigir.md`](kit/04-checklists/confira-antes-de-corrigir.md)) | ê°Å¸Â§Â  |
| 7 | Generar el video | Decir "puedes construir el clip"; fal genera los 8 s y Hypit lo monta en tu computadora | ê°Å¸Â¤â ê¢â â ê¢Å¡â¢ê¯Â¸Â |
| 8 | Corregir | Mensaje 2 (premium), presupuestar, revisar, construir | ê°Å¸Â§Â  ê¢â â ê°Å¸Â¤â |
| 9 | Hacer versiones | Mensaje 3 (otro idioma) y/o 4 (personajes ficticios del `characters.json`) | ê°Å¸Â§Â  ê¢â â ê°Å¸Â¤â ê¢â â ê¢Å¡â¢ê¯Â¸Â |
| 10 | Probar | Correr las versiones como una sola prueba y quedarte con las que retienen mêÂ¡s ([`teste-com-7-versoes.md`](kit/04-checklists/teste-com-7-versoes.md)) | ê°Å¸Â§Â  |

### DêÂ³nde estêÂ¡n la guêÂ­a y el video de este repositorio

| Pieza | DêÂ³nde | QuiêÂ©n lo hace |
|---|---|---|
| GuêÂ­a (PT/EN/ES) | `guia/index.html`, `guia/en/`, `guia/es/` ê¢â â https://linnoff88-dev.github.io/ | ê°Å¸Â§Â  (sesiêÂ³n ARCKHê) ê¢â â ê¢Å¡â¢ê¯Â¸Â GitHub Pages vêÂ­a Actions |
| Video explicativo | archivo final fuera del repo; publicado como release `video-v1.0.0` (MP4 + SRT) y reproductor en `videos/` ê¢â â https://linnoff88-dev.github.io/ | ê¢Å¡â¢ê¯Â¸Â `python3 scripts/publica.py` |

## Estructura del kit

```
kit/
ê¢âÅê¢ââ¬ê¢ââ¬ 00-COMECE-AQUI.md
ê¢âÅê¢ââ¬ê¢ââ¬ 01-instalacao/
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ 1-o-que-precisa.md
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ 2-mensagem-de-instalacao.md
ê¢ââ   ê¢ââê¢ââ¬ê¢ââ¬ 3-chave-fal-segura.md
ê¢âÅê¢ââ¬ê¢ââ¬ 02-mensagens/
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ 1-refazer-com-seu-rosto.md
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ 2-corrigir-com-premium.md
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ 3-nova-lingua.md
ê¢ââ   ê¢ââê¢ââ¬ê¢ââ¬ 4-um-clipe-varias-pessoas.md
ê¢âÅê¢ââ¬ê¢ââ¬ 03-modelos/
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ README.md
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ characters.json
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ hypit.runtime.example.json
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ refazer-com-seu-rosto.svml
ê¢ââ   ê¢ââê¢ââ¬ê¢ââ¬ recast-um-personagem.svml
ê¢âÅê¢ââ¬ê¢ââ¬ 04-checklists/
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ confira-antes-de-corrigir.md
ê¢ââ   ê¢âÅê¢ââ¬ê¢ââ¬ 3-erros.md
ê¢ââ   ê¢ââê¢ââ¬ê¢ââ¬ teste-com-7-versoes.md
ê¢ââê¢ââ¬ê¢ââ¬ 05-precos-e-links.md
guia/        pêÂ¡gina de uso (PT, en/, es/)
videos/      reproductor del video explicativo
scripts/     publica.py (sube el video como release y genera el reproductor)
```

## Licencia de Hypit (resumen)

Hypit usa la "Hypit Open Source License" (Apache-2.0 con condiciones). En resumen: uso libre para tu trabajo y el
de tus clientes, tambiêÂ©n comercial; no puede operarse como servicio alojado o multiinquilino para terceros; no se puede
vender ni empaquetar Hypit o derivados; debes mantener el nombre y el logo. Lo que creas es tuyo; los têÂ©rminos de los
proveedores de modelos siguen vigentes. Lee la licencia completa en https://github.com/hypit-ai/hypit.

## Licencia de este kit

[MIT](LICENSE) ê¢â¬â vale solo para el texto, las plantillas de archivo y los scripts de ARCKHê.

---

Contenido abierto y gratuito de **[ARCKHê AI](https://ARCKHê AI)**.
