# Clone viral com o seu rosto ê¢â¬â Hypit + Claude Code + fal

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


[![Clone viral com o seu rosto](guia/assets/banner.jpg)](https://linnoff88-dev.github.io/

**ê°Å¸â¡Â§ê°Å¸â¡Â· [PortuguêÂªs](README.md) êÂ· ê°Å¸â¡Âºê°Å¸â¡Â¸ [English](README.en.md) êÂ· ê°Å¸â¡Âªê°Å¸â¡Â¸ [EspaêÂ±ol](README.es.md)**

## O que êÂ©

Este êÂ© um kit gratuito do ARCKHê, em portuguêÂªs, com mensagens prontas para colar no Claude Code, modelos de arquivo,
checklists e uma tabela de preêÂ§os. Ele ensina a usar o Hypit, uma ferramenta aberta de vêÂ­deo, para refazer um clipe
curto com o seu prêÂ³prio rosto, fazer a versêÂ£o em outra lêÂ­ngua ou trocar a pessoa por personagens fictêÂ­cios. Serve
para quem faz marketing ou cria conteêÂºdo e quer testar vêÂ¡rias versêÂµes de um anêÂºncio sem gravar de novo. VocêÂª precisa
do Claude Code, de uma conta no fal com alguns dêÂ³lares de crêÂ©dito, de um clipe seu e de duas fotos do seu rosto.

## ê°Å¸ââ Guia de uso

Guia completo (landing + passo a passo): **https://linnoff88-dev.github.io/

VêÂ­deo explicativo do kit: **https://linnoff88-dev.github.io/

## Para quem êÂ©

- **Marketing e trêÂ¡fego pago:** um clipe vira 5 a 10 versêÂµes para testar com pouca verba antes de gravar de verdade.
- **Criadores de conteêÂºdo:** a mesma cena em outra lêÂ­ngua, ou com vocêÂª no lugar do apresentador, sem cêÂ¢mera nem estêÂºdio.

## As trêÂªs peêÂ§as

- **[Hypit](https://github.com/hypit-ai/hypit)** ê¢â¬â ferramenta aberta que roda dentro do Claude Code: lêÂª o seu vêÂ­deo,
  planeja um novo, pede aos modelos as imagens e os clipes, pêÂµe legendas e monta tudo no seu computador.
- **[fal](https://fal.ai)** ê¢â¬â serviêÂ§o onde rodam os modelos de imagem e de vêÂ­deo. VocêÂª paga por imagem e por segundo.
- **Claude Code** ê¢â¬â vocêÂª pede em texto; ele escreve os arquivos do Hypit e mostra o plano e o preêÂ§o antes de gastar.

**O Hypit nêÂ£o vem neste repositêÂ³rio.** A licenêÂ§a dele nêÂ£o permite empacotar; o prêÂ³prio Claude instala a partir do
repositêÂ³rio oficial.

## Os 3 passos

1. **Instalar** ê¢â¬â uma mensagem instala o Hypit sêÂ³ no projeto e liga o fal lendo a `FAL_KEY` do ambiente (uns 6 min).
2. **Refazer com o seu rosto** ê¢â¬â primeiro e êÂºltimo quadro com o seu rosto, depois os 8 segundos entre eles.
3. **Conferir, corrigir e fazer versêÂµes** ê¢â¬â rosto, mêÂ£os e texto; modelos premium; outra lêÂ­ngua; personagens fictêÂ­cios.

Toda mensagem termina com **"Me mostre o plano e o preêÂ§o e nêÂ£o construa nada."** ê¢â¬â a frase que faz o Claude orêÂ§ar e
parar antes de gastar crêÂ©dito.

## PreêÂ§os (aproximados, pela tabela de 21/10/2026)

| O quêÂª | Custo aproximado |
|---|---|
| Primeira versêÂ£o com o seu rosto (Seedream 5 Lite + MiniMax H3 768p) | US$ 0,71 |
| VersêÂ£o premium (GPT Image 2.5 + MiniMax H3 Max 1080p) | ~US$ 2 |
| VersêÂ£o em outra lêÂ­ngua | ~US$ 2 |
| MiniMax H3 Recast 1080p (US$ 0,45/s) | US$ 3,60 por clipe de 8 s êÂ· 7 versêÂµes ê¢â°Ë US$ 25,20 êÂ· lote de 8 ê¢â°Ë US$ 28,80 |
| Higgsfield Genjutsu 1080p (US$ 1,632/s, comparaêÂ§êÂ£o) | US$ 13,06 por clipe êÂ· lote de 8 ê¢â°Ë US$ 104,50 |

PreêÂ§o muda: confira as pêÂ¡ginas antes de gastar. Recast e Genjutsu sêÂ£o modelos diferentes; sêÂ³ o preêÂ§o foi comparado.
Fontes e detalhes em [`kit/05-precos-e-links.md`](kit/05-precos-e-links.md).

## ê¢Å¡Â ê¯Â¸Â A regra êÂ©tica

**Use sêÂ³ o seu rosto, ou um rosto que vocêÂª tem permissêÂ£o por escrito para usar. Use sêÂ³ clipes seus, ou clipes que
vocêÂª tem direito de refazer.** Nada de pessoa famosa, de colega sem autorizaêÂ§êÂ£o ou de vêÂ­deo alheio. Os personagens do
kit sêÂ£o fictêÂ­cios. Se o anêÂºncio parece depoimento, avise que êÂ© conteêÂºdo gerado por IA.

## O processo, do inêÂ­cio ao fim

Quem faz: ê°Å¸Â§Â  vocêÂª no Claude Code êÂ· ê¢Å¡â¢ê¯Â¸Â Hypit/script êÂ· ê°Å¸Â¤â modelos no fal.

| # | Passo | O que fazer | Quem faz |
|---|---|---|---|
| 1 | Preparar | Criar a pasta do projeto com `references/meu-clipe.mp4`, `rosto-1.jpg`, `rosto-2.jpg` (para personagens: `references/meu-ugc.mp4` e `characters.json` na raiz); o Claude extrai os quadros ([`kit/01-instalacao/1-o-que-precisa.md`](kit/01-instalacao/1-o-que-precisa.md)) | ê°Å¸Â§Â  |
| 2 | Guardar a chave | `export FAL_KEY="..."` no `~/.zshrc`/`~/.bashrc` (Windows: `setx FAL_KEY "..."`), abrir terminal novo; nunca no chat ([`3-chave-fal-segura.md`](kit/01-instalacao/3-chave-fal-segura.md)) | ê°Å¸Â§Â  |
| 3 | Instalar | Colar a mensagem de instalaêÂ§êÂ£o no Claude Code ([`2-mensagem-de-instalacao.md`](kit/01-instalacao/2-mensagem-de-instalacao.md)); o Hypit êÂ© instalado com `npx skills add hypit-ai/hypit` (sem `-g`) e `@hypit/hypit` | ê°Å¸Â§Â  ê¢â â ê¢Å¡â¢ê¯Â¸Â |
| 4 | OrêÂ§ar o primeiro clipe | Colar a mensagem 1 ([`kit/02-mensagens/1-refazer-com-seu-rosto.md`](kit/02-mensagens/1-refazer-com-seu-rosto.md)); o Claude escreve o `.svml` e mostra plano e preêÂ§o | ê°Å¸Â§Â  ê¢â â ê¢Å¡â¢ê¯Â¸Â |
| 5 | Gerar as imagens | Dizer "pode construir as imagens"; os 2 quadros com o seu rosto saem do fal | ê°Å¸Â¤â |
| 6 | Conferir as imagens | Rosto, mêÂ£os, texto ([`kit/04-checklists/confira-antes-de-corrigir.md`](kit/04-checklists/confira-antes-de-corrigir.md)) | ê°Å¸Â§Â  |
| 7 | Gerar o vêÂ­deo | Dizer "pode construir o clipe"; o fal gera os 8 s e o Hypit monta no seu computador | ê°Å¸Â¤â ê¢â â ê¢Å¡â¢ê¯Â¸Â |
| 8 | Corrigir | Mensagem 2 (premium), orêÂ§ar, conferir, construir | ê°Å¸Â§Â  ê¢â â ê°Å¸Â¤â |
| 9 | Fazer versêÂµes | Mensagem 3 (outra lêÂ­ngua) e/ou 4 (personagens fictêÂ­cios do `characters.json`) | ê°Å¸Â§Â  ê¢â â ê°Å¸Â¤â ê¢â â ê¢Å¡â¢ê¯Â¸Â |
| 10 | Testar | Rodar as versêÂµes como um teste sêÂ³ e ficar com as que retêÂªm mais ([`teste-com-7-versoes.md`](kit/04-checklists/teste-com-7-versoes.md)) | ê°Å¸Â§Â  |

### Onde ficam o guia e o vêÂ­deo deste repositêÂ³rio

| PeêÂ§a | Onde | Quem faz |
|---|---|---|
| Guia (PT/EN/ES) | `guia/index.html`, `guia/en/`, `guia/es/` ê¢â â https://linnoff88-dev.github.io/ | ê°Å¸Â§Â  (sessêÂ£o ARCKHê) ê¢â â ê¢Å¡â¢ê¯Â¸Â GitHub Pages via Actions |
| VêÂ­deo explicativo | arquivo final fora do repo; publicado como release `video-v1.0.0` (MP4 + SRT) e player em `videos/` ê¢â â https://linnoff88-dev.github.io/ | ê¢Å¡â¢ê¯Â¸Â `python3 scripts/publica.py` |

## Estrutura do kit

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
videos/      player do vêÂ­deo explicativo
scripts/     publica.py (sobe o vêÂ­deo como release e gera o player)
```

## LicenêÂ§a do Hypit (resumo)

O Hypit usa a "Hypit Open Source License" (Apache-2.0 com condiêÂ§êÂµes). Em resumo: uso livre para o seu trabalho e o
de clientes, tambêÂ©m comercial; nêÂ£o pode operar como serviêÂ§o hospedado ou multi-inquilino para terceiros; nêÂ£o pode
vender nem empacotar o Hypit ou derivados; precisa manter o nome e o logo. O que vocêÂª cria êÂ© seu; os termos dos
provedores de modelo continuam valendo. Leia a licenêÂ§a completa em https://github.com/hypit-ai/hypit.

## LicenêÂ§a deste kit

[MIT](LICENSE) ê¢â¬â vale sêÂ³ para o texto, os modelos de arquivo e os scripts do ARCKHê.

---

ConteêÂºdo aberto e gratuito do **[ARCKHê AI](https://ARCKHê AI)**.

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>