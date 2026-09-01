# Como inserir esses arquivos no repositório

Estes arquivos foram feitos assumindo que o site usa **Jekyll** (padrão do GitHub Pages). Não tive acesso direto ao repositório, então alguns ajustes provavelmente serão necessários — principalmente se o site já usa um tema pronto (ex: Minimal Mistakes), que pode ter nomes de layout diferentes dos que usei aqui (`default`).

## Ordem sugerida para colar os arquivos

1. **`_config-snippet.yml`** — não é pra sobrescrever seu `_config.yml` atual. Copie só o bloco `collections:` de dentro dele e cole dentro do seu `_config.yml` existente (na raiz do repositório).

2. **`_data/`** — copie os dois arquivos (`navigation.yml`, `equipe.yml`) para a pasta `_data/` do repositório. Se a pasta não existir, crie-a na raiz.

3. **`_sass/_colecoes.scss`** — copie para dentro de `_sass/` na raiz. Depois, garanta que seu arquivo `assets/css/main.scss` (ou equivalente) tenha a linha `@import "colecoes";` — sem isso, o Sass novo não é carregado.

4. **`_includes/badge-colecao.html`** — copie para `_includes/`.

5. **`_layouts/colecao.html`** e **`_layouts/publicacao.html`** — copie para `_layouts/`. **Atenção**: eles usam `layout: default` como base — se o tema do site já tiver um layout base com outro nome, troque `default` por esse nome no topo dos dois arquivos.

6. **`_publicacoes/`** e **`_eventos/`** — essas são as *collections*. Copie as pastas inteiras (com os arquivos de exemplo dentro) para a raiz do repositório. Os exemplos (`exemplo-manual-restinga.md`, `exemplo-epa.md`) podem ser apagados depois de todos entenderem o formato — sirva de modelo pra cada frente criar os próprios.

7. **`colecoes/`** — copie a pasta inteira (com `ctpm/` e `rbetno/` dentro) para a raiz.

8. **`quem-somos/`** — copie a pasta inteira para a raiz.

9. **`publicacoes.md`**, **`eventos.md`**, **`contato.md`** — copie para a raiz do repositório.

10. **`index.md`** — este é o mais delicado: **não sobrescreva o `index.md` que já existe** sem antes comparar. Ele provavelmente já tem conteúdo (a home atual da CTPM). Use o que mandei aqui como referência de estrutura e mescle manualmente o conteúdo que já existe.

## O que ainda falta preencher

Praticamente todo o *conteúdo de texto* está com placeholders `[preencher — responsável: nome]`, seguindo exatamente a divisão de tarefas do documento de gestão. A estrutura de arquivos e o código (front matter, Liquid) já funcionam — o trabalho de cada frente agora é só editar o texto dentro do arquivo correspondente.

## Se o site não for Jekyll

Se ao abrir o repositório você não encontrar um `_config.yml` na raiz, me avise (ou cole aqui o conteúdo da raiz do repo) que eu refaço esses arquivos para o formato certo.
