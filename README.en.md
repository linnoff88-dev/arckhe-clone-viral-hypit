# Viral clone with your face â€” Hypit + Claude Code + fal

[![Viral clone with your face](guia/assets/banner-en.jpg)](https://linnoff88-dev.github.io/

**ðŸ‡§ðŸ‡· [Português](README.md) Â· ðŸ‡ºðŸ‡¸ [English](README.en.md) Â· ðŸ‡ªðŸ‡¸ [Espaê±ol](README.es.md)**

## What it is

This is a free kit from ARCKHÉ, in Portuguese, with ready-made messages to paste into Claude Code, file templates,
checklists and a price table. It teaches you to use Hypit, an open video tool, to redo a short clip with your own
face, make a version in another language, or swap the person for fictional characters. It is meant for people who do
marketing or create content and want to test several versions of an ad without filming again. You need Claude Code, a
fal account with a few dollars of credit, a clip of your own and two photos of your face.

## ðŸ“– User guide

Full guide (landing + step by step): **https://linnoff88-dev.github.io/

Kit explainer video: **https://linnoff88-dev.github.io/

## Who it's for

- **Marketing and paid traffic:** one clip becomes 5 to 10 versions to test on a small budget before filming for real.
- **Content creators:** the same scene in another language, or with you in place of the presenter, with no camera or studio.

## The three pieces

- **[Hypit](https://github.com/hypit-ai/hypit)** â€” open tool that runs inside Claude Code: it reads your video,
  plans a new one, asks the models for the images and clips, adds captions and assembles everything on your computer.
- **[fal](https://fal.ai)** â€” service where the image and video models run. You pay per image and per second.
- **Claude Code** â€” you ask in text; it writes the Hypit files and shows the plan and the price before spending anything.

**Hypit is not included in this repository.** Its license does not allow bundling it; Claude itself installs it from
the official repository.

## The 3 steps

1. **Install** â€” one message installs Hypit only in the project and connects fal by reading the `FAL_KEY` from the environment (about 6 min).
2. **Redo it with your face** â€” first and last frame with your face, then the 8 seconds between them.
3. **Check, fix and make versions** â€” face, hands and text; premium models; another language; fictional characters.

Every message ends with **"Show me the plan and the price and don't build anything."** â€” the sentence that makes
Claude estimate the cost and stop before spending credit.

## Prices (approximate, from the 10/21/2026 table)

| What | Approximate cost |
|---|---|
| First version with your face (Seedream 5 Lite + MiniMax H3 768p) | US$0.71 |
| Premium version (GPT Image 2.5 + MiniMax H3 Max 1080p) | ~US$2 |
| Version in another language | ~US$2 |
| MiniMax H3 Recast 1080p (US$0.45/s) | US$3.60 per 8 s clip Â· 7 versions â‰ˆ US$25.20 Â· batch of 8 â‰ˆ US$28.80 |
| Higgsfield Genjutsu 1080p (US$1.632/s, comparison) | US$13.06 per clip Â· batch of 8 â‰ˆ US$104.50 |

Prices change: check the pages before spending. Recast and Genjutsu are different models; only the price was compared.
Sources and details in [`kit/05-precos-e-links.md`](kit/05-precos-e-links.md) (the kit is in Portuguese).

## âš ï¸ The ethics rule

**Use only your own face, or a face you have written permission to use. Use only your own clips, or clips you have the
right to redo.** No famous people, no colleagues without authorization, no videos that belong to someone else. The
characters in the kit are fictional. If the ad looks like a testimonial, say that it is AI-generated content.

## The process, from start to finish

Who does it: ðŸ§  you in Claude Code Â· âš™ï¸ Hypit/script Â· ðŸ¤– models on fal.

| # | Step | What to do | Who does it |
|---|---|---|---|
| 1 | Prepare | Create the project folder with `references/meu-clipe.mp4`, `rosto-1.jpg`, `rosto-2.jpg` (for characters: `references/meu-ugc.mp4` and `characters.json` at the root); Claude extracts the frames ([`kit/01-instalacao/1-o-que-precisa.md`](kit/01-instalacao/1-o-que-precisa.md)) | ðŸ§  |
| 2 | Store the key | `export FAL_KEY="..."` in `~/.zshrc`/`~/.bashrc` (Windows: `setx FAL_KEY "..."`), open a new terminal; never in the chat ([`3-chave-fal-segura.md`](kit/01-instalacao/3-chave-fal-segura.md)) | ðŸ§  |
| 3 | Install | Paste the install message into Claude Code ([`2-mensagem-de-instalacao.md`](kit/01-instalacao/2-mensagem-de-instalacao.md)); Hypit is installed with `npx skills add hypit-ai/hypit` (without `-g`) and `@hypit/hypit` | ðŸ§  â†’ âš™ï¸ |
| 4 | Price the first clip | Paste message 1 ([`kit/02-mensagens/1-refazer-com-seu-rosto.md`](kit/02-mensagens/1-refazer-com-seu-rosto.md)); Claude writes the `.svml` and shows the plan and price | ðŸ§  â†’ âš™ï¸ |
| 5 | Generate the images | Say "go ahead and build the images"; the 2 frames with your face come from fal | ðŸ¤– |
| 6 | Check the images | Face, hands, text ([`kit/04-checklists/confira-antes-de-corrigir.md`](kit/04-checklists/confira-antes-de-corrigir.md)) | ðŸ§  |
| 7 | Generate the video | Say "go ahead and build the clip"; fal generates the 8 s and Hypit assembles it on your computer | ðŸ¤– â†’ âš™ï¸ |
| 8 | Fix | Message 2 (premium), price it, check, build | ðŸ§  â†’ ðŸ¤– |
| 9 | Make versions | Message 3 (another language) and/or 4 (fictional characters from `characters.json`) | ðŸ§  â†’ ðŸ¤– â†’ âš™ï¸ |
| 10 | Test | Run the versions as a single test and keep the ones that hold attention best ([`teste-com-7-versoes.md`](kit/04-checklists/teste-com-7-versoes.md)) | ðŸ§  |

### Where this repository's guide and video live

| Piece | Where | Who does it |
|---|---|---|
| Guide (PT/EN/ES) | `guia/index.html`, `guia/en/`, `guia/es/` â†’ https://linnoff88-dev.github.io/ | ðŸ§  (ARCKHÉ session) â†’ âš™ï¸ GitHub Pages via Actions |
| Explainer video | final file outside the repo; published as release `video-v1.0.0` (MP4 + SRT) and player in `videos/` â†’ https://linnoff88-dev.github.io/ | âš™ï¸ `python3 scripts/publica.py` |

## Kit structure

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
guia/        usage page (PT, en/, es/)
videos/      explainer video player
scripts/     publica.py (uploads the video as a release and generates the player)
```

## Hypit license (summary)

Hypit uses the "Hypit Open Source License" (Apache-2.0 with conditions). In short: free to use for your own work and
for clients, including commercially; it may not be operated as a hosted or multi-tenant service for third parties; you
may not sell or bundle Hypit or derivatives; you must keep the name and the logo. What you create is yours; the terms
of the model providers still apply. Read the full license at https://github.com/hypit-ai/hypit.

## License of this kit

[MIT](LICENSE) â€” covers only the text, the file templates and the ARCKHÉ scripts.

---

Open and free content from **[ARCKHÉ AI](https://ARCKHÉ AI)**.
