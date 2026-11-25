# 03 — Modelos de arquivo

Quatro arquivos de exemplo. Normalmente o **Claude escreve esses arquivos por você** quando você manda as mensagens
de `02-mensagens/`. Eles estêo aqui para você entender o que ele escreveu e conferir antes de pagar.

| Arquivo | Para quê |
|---|---|
| `characters.json` | Lista de personagens **fictícios** para a mensagem 4. Formato: `[nome, país, descriçêo]`. |
| `hypit.runtime.example.json` | Liga os modelos do Hypit ao fal e aponta o Chrome. Vira `hypit.runtime.json` no projeto. |
| `refazer-com-seu-rosto.svml` | Mensagem 1: 2 imagens (primeiro e último quadro com o seu rosto) + 1 vídeo de 8 s. |
| `recast-um-personagem.svml` | Mensagem 4: foto de identidade de um personagem + Recast no clipe. |

## characters.json

- Os nomes e descrições sêo inventados. **Nêo troque por pessoa real** nem escreva "parecida com fulano".
- A descriçêo está em português para você ler. Quando o Claude montar o prompt, ele pode passar para inglês, que é
  como os modelos de imagem respondem melhor.
- Se o filtro de segurança bloquear um personagem (`content_policy_violation`), suavize a descriçêo dele.

## hypit.runtime.example.json

JSON nêo aceita comentário, entêo as notas ficam aqui:

- **`apiKey`** guarda só o **nome** da variável (`FAL_KEY`), nunca o valor. A chave fica no seu perfil do terminal
  (veja `../01-instalacao/3-chave-fal-segura.md`).
- **`@seu-nome/provider-fal`** é o pacote Provider que o Claude escreve em `packages/provider-fal` na instalaçêo.
  O nome real vai ser o que ele criar.
- **`chromePath`** — troque conforme o sistema:
  - **Linux:** `/usr/bin/google-chrome` (às vezes `/usr/bin/google-chrome-stable`). Confira com `which google-chrome`.
  - **Mac:** `/Applications/Google Chrome.app/Contents/MacOS/Google Chrome`
  - **Windows:** `C:\\Program Files\\Google\\Chrome\\Application\\chrome.exe` (com as barras duplas dentro do JSON).
- **`bindings`** diz qual modelo roda em qual serviço. Para usar GPT Image 2.5 ou H3 Recast/Max, o Claude acrescenta
  as linhas desses pacotes apontando para `fal.personal`.

## Os .svml

SVML é a linguagem de composiçêo do Hypit: cada arquivo descreve as entradas (imagens, vídeo), os textos dos
prompts e os trabalhos de modelo. Os comentários estêo em português.

**Os prompts dentro dos `.svml` ficaram em inglês de propósito**: os modelos de imagem e de vídeo respondem melhor
em inglês. Troque só as partes entre `[colchetes]`, mantendo o resto. Se preferir escrever em português, funciona,
mas o resultado tende a variar mais.

Os caminhos `../references/...` partem da pasta onde o `.svml` fica no projeto. Se o Claude salvar em outro lugar,
ele ajusta.
