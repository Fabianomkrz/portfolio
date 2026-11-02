# Portfólio v0

Meu primeiro portfólio publicado: junta as páginas que já fiz (Sobre mim e Receitas da família), ganha uma página nova sobre um hobby e recebe um CSS único para todas as páginas. No fim, vai ao ar no GitHub Pages.

## Problema

Os projetos anteriores existem só no meu computador e em repositórios privados: ninguém consegue abrir e ver. E todos estão sem estilo nenhum. Falta um endereço público, com cara de site, para mostrar o que eu sei fazer.

## Público

Pessoas que avaliam portfólio (recrutadores, colegas de curso) e amigos e família. Elas abrem o link no computador ou no celular e precisam entender em um minuto quem eu sou e o que já construí.

## Escopo

**Entra (só o que já está nos resumos):**
- Estrutura de pastas: `index.html` e `hobby.html` na raiz, `receitas/` com as páginas copiadas do projeto de receitas, `css/style.css`, `img/`.
- HTML semântico (`header`, `nav`, `main`, `section`, `article`, `footer`, `figure`/`figcaption`) e favicon.
- CSS **externo**: reset, cores em hexadecimal no `body`, fonte com fallback, links com cor própria e sem sublinhado, classes, box model (`padding`, `margin`, `margin: 0 auto`), `display`, `:hover` e media queries de 768px e 375px.
- Git com o fluxo completo da aula 05: uma **branch por Issue**, **Pull Request** e merge na `main`.
- Publicação no GitHub Pages.

**Fica de fora:** JavaScript, formulários, Flexbox e Grid (vêm no próximo curso), tag de versão (ainda sem aula) e `target="_blank"`.

**Segurança desta semana (vale para o PR de cada Issue):**
- Nada de senha, token ou chave. `.gitignore` criado na Issue #1.
- Nada de telefone, endereço, documento ou e-mail pessoal. **O repositório e o site serão públicos**: releia nome completo, idade e região antes da Issue #6 e decida o que fica.
- Imagens: suas ou de banco com licença (Unsplash, Pexels), com crédito na legenda.

## Como fazer cada Issue (fluxo da aula 05)

A Issue #1 vai direto na `main`, porque o repositório ainda não existe. Da #2 em diante, sempre:

1. `git checkout main` e `git pull` (começa da versão mais nova).
2. `git checkout -b feat/nome-da-issue` (cria a branch e já entra nela).
3. Faça a Issue, com `git add` e `git commit -m "..."` pequenos pelo caminho.
4. `git push origin feat/nome-da-issue`.
5. No GitHub: aparece o aviso "Compare & pull request". Base `main` ← sua branch. No título, o nome da Issue; na descrição, o que você fez e como testou.
6. Antes do merge, me peça para revisar o PR (é o "alguém revisa" da aula). Depois: **Merge pull request → Confirm merge**.
7. De volta ao computador: `git checkout main` e `git pull`.

## Issues

Marque `[x]` só quando o PR da Issue estiver com merge.

- [X] **#1 Repositório e estrutura.** Criar a pasta, o Git e o repositório no GitHub.
  - Pronto quando: o repositório `portfolio` existe no GitHub, **público**, com a branch `main`; tem este README e um `.gitignore` (mesmo vazio, com uma linha no README dizendo por quê); as pastas `css/`, `img/` e `receitas/` existem no seu computador (o Git só envia pasta que tiver arquivo dentro, então elas aparecem no GitHub a partir da #2).

- [ ] **#2 Trazer as páginas antigas.** Branch `feat/paginas-antigas`.
  - Pronto quando: `index.html` tem o conteúdo do Sobre mim (apresentação e o que estudo), mais uma `section` "Projetos" com links para `receitas/index.html` e `hobby.html`; as páginas de receitas foram copiadas para `receitas/` com as imagens; **todo link funciona nas duas direções**: das receitas de volta ao início usando `../index.html`, e os `src` das imagens apontam para o caminho certo depois da mudança de pasta; cada página tem um só `h1` e um `title` próprio.

- [ ] **#3 CSS base.** Branch `feat/css-base`.
  - Pronto quando: `css/style.css` está ligado por `<link rel="stylesheet">` em **todas** as páginas, inclusive as de `receitas/` (atenção ao caminho); não há `style` inline nem `<style>` interno; tem reset (`*` com `margin: 0` e `padding: 0`); fundo e cor do texto definidos no `body` em hexadecimal; uma `font-family` com fallback genérico; links com cor própria e `text-decoration: none`; favicon com `href` e `type` certos em todas as páginas.

- [ ] **#4 Página do hobby.** Branch `feat/pagina-hobby`. O hobby é seu, à sua escolha.
  - Pronto quando: `hobby.html` tem o mesmo `header` (com a `nav`) e o mesmo `footer` das outras páginas; pelo menos 2 `section` com `h2`, um tema cada; uma `figure` com `figcaption`, `alt` descritivo e crédito; formato da imagem justificado em uma linha nas Notas (com o **porquê**, não só "é foto"); um link de destaque com estilo de botão por classe: `display: block`, `padding`, centralizado com `margin: 0 auto` e cor diferente no `:hover`.

- [ ] **#5 Layout adaptado.** Branch `feat/layout-adaptado`.
  - Pronto quando: há `@media (max-width: 768px)` e `@media (max-width: 375px)` no `style.css`; no modo responsivo do inspetor, nas duas larguras, **nenhuma página tem rolagem para o lado**, o texto continua legível e a imagem do hobby cabe na tela; nenhum `<br>` usado para ajustar o layout; a `meta viewport` está em todas as páginas.

- [ ] **#6 Publicar no GitHub Pages.** Faça direto pelo GitHub (Settings → Pages), sem branch.
  - Pronto quando: o site abre em `usuario.github.io/portfolio`; o link está no topo deste README; o CSS e as imagens aparecem também online (se no seu computador aparece e online não, confira maiúsculas e minúsculas nos nomes dos arquivos e nos caminhos); a decisão sobre nome, idade e região foi tomada antes de publicar.

- [ ] **#7 Teste manual.** Branch `docs/teste-manual`. Siga o roteiro abaixo **no site publicado** e preencha a coluna "Resultado".
  - Pronto quando: todos os passos têm `OK` ou a descrição do que falhou; o que falhou foi corrigido (em outra branch `fix/...`, com PR) e testado de novo.

### Roteiro de teste (Issue #7)

| # | Faça | Esperado | Resultado |
| --- | --- | --- | --- |
| 1 | Abra o link do site | Página inicial com cores e fonte do seu CSS; a URL começa com `https` | |
| 2 | Clique em cada link da `nav`, em **todas** as páginas | Cada um abre a página certa, sem 404 | |
| 3 | Entre numa receita e volte ao início pela `nav` | Volta para o `index.html` | |
| 4 | Olhe todas as imagens | Todas aparecem; nenhuma quebrada | |
| 5 | Passe o mouse no botão do hobby | A cor muda | |
| 6 | Olhe a aba em cada página | `title` próprio e favicon aparecendo | |
| 7 | Inspetor → modo responsivo → 768px, depois 375px, em cada página | Sem rolagem lateral; texto legível; botão centralizado | |
| 8 | Abra o link pelo celular | Mesma coisa do passo 7, no aparelho de verdade | |

## Notas do projeto

*(Preencha ao longo da semana: o que deu certo, onde travou, o que mudaria. Na Issue #4, a justificativa do formato da imagem.)*

.gitignore está vazio, pois ainda não existem arquivos no projeto e também nada a esconder.
