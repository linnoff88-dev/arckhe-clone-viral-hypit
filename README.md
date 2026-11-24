# Clone viral com o seu rosto â€” Hypit + Claude Code + fal

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


[![Clone viral com o seu rosto](guia/assets/banner.jpg)](https://linnoff88-dev.github.io/

**ðŸ‡§ðŸ‡· [PortuguÃªs](README.md) Â· ðŸ‡ºðŸ‡¸ [English](README.en.md) Â· ðŸ‡ªðŸ‡¸ [EspaÃ±ol](README.es.md)**

## O que Ã©

Este Ã© um kit gratuito do ARCKHÉ, em portuguÃªs, com mensagens prontas para colar no Claude Code, modelos de arquivo,
checklists e uma tabela de preÃ§os. Ele ensina a usar o Hypit, uma ferramenta aberta de vÃ­deo, para refazer um clipe
curto com o seu prÃ³prio rosto, fazer a versÃ£o em outra lÃ­ngua ou trocar a pessoa por personagens fictÃ­cios. Serve
para quem faz marketing ou cria conteÃºdo e quer testar vÃ¡rias versÃµes de um anÃºncio sem gravar de novo. VocÃª precisa
do Claude Code, de uma conta no fal com alguns dÃ³lares de crÃ©dito, de um clipe seu e de duas fotos do seu rosto.

## ðŸ“– Guia de uso

Guia completo (landing + passo a passo): **https://linnoff88-dev.github.io/

VÃ­deo explicativo do kit: **https://linnoff88-dev.github.io/

## Para quem Ã©

- **Marketing e trÃ¡fego pago:** um clipe vira 5 a 10 versÃµes para testar com pouca verba antes de gravar de verdade.
- **Criadores de conteÃºdo:** a mesma cena em outra lÃ­ngua, ou com vocÃª no lugar do apresentador, sem cÃ¢mera nem estÃºdio.

## As trÃªs peÃ§as

- **[Hypit](https://github.com/hypit-ai/hypit)** â€” ferramenta aberta que roda dentro do Claude Code: lÃª o seu vÃ­deo,
  planeja um novo, pede aos modelos as imagens e os clipes, pÃµe legendas e monta tudo no seu computador.
- **[fal](https://fal.ai)** â€” serviÃ§o onde rodam os modelos de imagem e de vÃ­deo. VocÃª paga por imagem e por segundo.
- **Claude Code** â€” vocÃª pede em texto; ele escreve os arquivos do Hypit e mostra o plano e o preÃ§o antes de gastar.

**O Hypit nÃ£o vem neste repositÃ³rio.** A licenÃ§a dele nÃ£o permite empacotar; o prÃ³prio Claude instala a partir do
repositÃ³rio oficial.

## Os 3 passos

1. **Instalar** â€” uma mensagem instala o Hypit sÃ³ no projeto e liga o fal lendo a `FAL_KEY` do ambiente (uns 6 min).
2. **Refazer com o seu rosto** â€” primeiro e Ãºltimo quadro com o seu rosto, depois os 8 segundos entre eles.
3. **Conferir, corrigir e fazer versÃµes** â€” rosto, mÃ£os e texto; modelos premium; outra lÃ­ngua; personagens fictÃ­cios.

Toda mensagem termina com **"Me mostre o plano e o preÃ§o e nÃ£o construa nada."** â€” a frase que faz o Claude orÃ§ar e
parar antes de gastar crÃ©dito.

## PreÃ§os (aproximados, pela tabela de 21/10/2026)

| O quÃª | Custo aproximado |
|---|---|
| Primeira versÃ£o com o seu rosto (Seedream 5 Lite + MiniMax H3 768p) | US$ 0,71 |
| VersÃ£o premium (GPT Image 2.5 + MiniMax H3 Max 1080p) | ~US$ 2 |
| VersÃ£o em outra lÃ­ngua | ~US$ 2 |
| MiniMax H3 Recast 1080p (US$ 0,45/s) | US$ 3,60 por clipe de 8 s Â· 7 versÃµes â‰ˆ US$ 25,20 Â· lote de 8 â‰ˆ US$ 28,80 |
| Higgsfield Genjutsu 1080p (US$ 1,632/s, comparaÃ§Ã£o) | US$ 13,06 por clipe Â· lote de 8 â‰ˆ US$ 104,50 |

PreÃ§o muda: confira as pÃ¡ginas antes de gastar. Recast e Genjutsu sÃ£o modelos diferentes; sÃ³ o preÃ§o foi comparado.
Fontes e detalhes em [`kit/05-precos-e-links.md`](kit/05-precos-e-links.md).

## âš ï¸ A regra Ã©tica

**Use sÃ³ o seu rosto, ou um rosto que vocÃª tem permissÃ£o por escrito para usar. Use sÃ³ clipes seus, ou clipes que
vocÃª tem direito de refazer.** Nada de pessoa famosa, de colega sem autorizaÃ§Ã£o ou de vÃ­deo alheio. Os personagens do
kit sÃ£o fictÃ­cios. Se o anÃºncio parece depoimento, avise que Ã© conteÃºdo gerado por IA.

## O processo, do inÃ­cio ao fim

Quem faz: ðŸ§  vocÃª no Claude Code Â· âš™ï¸ Hypit/script Â· ðŸ¤– modelos no fal.

| # | Passo | O que fazer | Quem faz |
|---|---|---|---|
| 1 | Preparar | Criar a pasta do projeto com `references/meu-clipe.mp4`, `rosto-1.jpg`, `rosto-2.jpg` (para personagens: `references/meu-ugc.mp4` e `characters.json` na raiz); o Claude extrai os quadros ([`kit/01-instalacao/1-o-que-precisa.md`](kit/01-instalacao/1-o-que-precisa.md)) | ðŸ§  |
| 2 | Guardar a chave | `export FAL_KEY="..."` no `~/.zshrc`/`~/.bashrc` (Windows: `setx FAL_KEY "..."`), abrir terminal novo; nunca no chat ([`3-chave-fal-segura.md`](kit/01-instalacao/3-chave-fal-segura.md)) | ðŸ§  |
| 3 | Instalar | Colar a mensagem de instalaÃ§Ã£o no Claude Code ([`2-mensagem-de-instalacao.md`](kit/01-instalacao/2-mensagem-de-instalacao.md)); o Hypit Ã© instalado com `npx skills add hypit-ai/hypit` (sem `-g`) e `@hypit/hypit` | ðŸ§  â†’ âš™ï¸ |
| 4 | OrÃ§ar o primeiro clipe | Colar a mensagem 1 ([`kit/02-mensagens/1-refazer-com-seu-rosto.md`](kit/02-mensagens/1-refazer-com-seu-rosto.md)); o Claude escreve o `.svml` e mostra plano e preÃ§o | ðŸ§  â†’ âš™ï¸ |
| 5 | Gerar as imagens | Dizer "pode construir as imagens"; os 2 quadros com o seu rosto saem do fal | ðŸ¤– |
| 6 | Conferir as imagens | Rosto, mÃ£os, texto ([`kit/04-checklists/confira-antes-de-corrigir.md`](kit/04-checklists/confira-antes-de-corrigir.md)) | ðŸ§  |
| 7 | Gerar o vÃ­deo | Dizer "pode construir o clipe"; o fal gera os 8 s e o Hypit monta no seu computador | ðŸ¤– â†’ âš™ï¸ |
| 8 | Corrigir | Mensagem 2 (premium), orÃ§ar, conferir, construir | ðŸ§  â†’ ðŸ¤– |
| 9 | Fazer versÃµes | Mensagem 3 (outra lÃ­ngua) e/ou 4 (personagens fictÃ­cios do `characters.json`) | ðŸ§  â†’ ðŸ¤– â†’ âš™ï¸ |
| 10 | Testar | Rodar as versÃµes como um teste sÃ³ e ficar com as que retÃªm mais ([`teste-com-7-versoes.md`](kit/04-checklists/teste-com-7-versoes.md)) | ðŸ§  |

### Onde ficam o guia e o vÃ­deo deste repositÃ³rio

| PeÃ§a | Onde | Quem faz |
|---|---|---|
| Guia (PT/EN/ES) | `guia/index.html`, `guia/en/`, `guia/es/` â†’ https://linnoff88-dev.github.io/ | ðŸ§  (sessÃ£o ARCKHÉ) â†’ âš™ï¸ GitHub Pages via Actions |
| VÃ­deo explicativo | arquivo final fora do repo; publicado como release `video-v1.0.0` (MP4 + SRT) e player em `videos/` â†’ https://linnoff88-dev.github.io/ | âš™ï¸ `python3 scripts/publica.py` |

## Estrutura do kit

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
videos/      player do vÃ­deo explicativo
scripts/     publica.py (sobe o vÃ­deo como release e gera o player)
```

## LicenÃ§a do Hypit (resumo)

O Hypit usa a "Hypit Open Source License" (Apache-2.0 com condiÃ§Ãµes). Em resumo: uso livre para o seu trabalho e o
de clientes, tambÃ©m comercial; nÃ£o pode operar como serviÃ§o hospedado ou multi-inquilino para terceiros; nÃ£o pode
vender nem empacotar o Hypit ou derivados; precisa manter o nome e o logo. O que vocÃª cria Ã© seu; os termos dos
provedores de modelo continuam valendo. Leia a licenÃ§a completa em https://github.com/hypit-ai/hypit.

## LicenÃ§a deste kit

[MIT](LICENSE) â€” vale sÃ³ para o texto, os modelos de arquivo e os scripts do ARCKHÉ.

---

ConteÃºdo aberto e gratuito do **[ARCKHÉ AI](https://ARCKHÉ AI)**.

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>