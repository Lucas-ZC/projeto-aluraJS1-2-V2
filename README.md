# Projeto de Treinamento de ***Git*** e ***Github***

![Badge Finalizado](http://img.shields.io/static/v1?label=STATUS&message=FINALIZADO&color=GREEN&style=for-the-badge)

<h2>Sobre </h2>
Projeto utilizado nos cursos do Alura para ensino de Git e Github 
<div align="left">
  <br>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" height="120" alt="git logo" />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" height="120" alt="git logo" />
  <img width="12" />
</div>

<h2>O que foi passado </h2>

<h3>Comandos do Terminal </h3>

- ***git init*** -> inicia o git 
- ***git add .*** -> adiciona todos arquivos ao git
- ***git commit -m “texto”*** -> commit
- ***git add README.md*** -> adiciona read me
- ***git config --global user.email “@gmail.com”*** -> Salvar email
- ***git config --global user.nome “Fulano”*** -> Salvar nome
- ***git branch -M main*** -> Renomeia a branch atual para main
- ***git remote add origin link do ssh do git hub*** -> adiciona um repositório remoto, com o URL do seu repositório no GitHub via SSH
- ***git push -u origin main*** -> Envia seus commits locais para o repositório remoto no GitHub e configura o rastreamento da branch
- ***git status*** -> status das últimas alterações
- ***git remote*** -> listar repositórios remotos
- ***git push origin main*** -> envia os commits do repositório local pro repositório remoto
- ***git pull origin main*** -> pega os commits do repositório remoto pro local
- ***git log*** -> mostra histórico de commits
- ***git revert + id do commit no git log*** -> reverte o commit fazendo um commit
- ***git reset  --hard + passar id do commit anterior, que quer a versão*** -> desfaz commit e mudança no código
- ***git commit –amend -m “mensagem”*** -> altera nome do último commit

<h3>Tutoriais </h3>

***PC não conectado com o git/gerar chave SSH:***
- ssh-keygen -t ed25519 -C "SEU EMAIL AQUI” (terminal);
- enter e depois mais um enter;
- Pasta(do pc);
- Pasta de usuário;
- .ssh;
- Conferir os arquivos e ver qual é a chave pública e copiar;
- Settings (da conta);
- SSH and GPG keys;
- new SSH key; 
- Title: algum nome;
- Key: colar. 
 
***Clonar repositório:***
- Copiar https.git no github;
- Abrir Windows powershell;
- git clone + colar.

***Não mostrar alguns dos arquivos no github:***
- Criar um arquivo .gitignore (no visual studio);
- Escrever os nomes;
- Pra pasta: nome/, pra arquivo especifico: exemplo.txt, pra passar um padrão: *.css.
Dica: site que gera gitignore pra cada linguagem/tecnologia: https://www.toptal.com/developers/gitignore.

***Compartilhar códigos (com o gist):***
- Ir na tela inicial do repositório com o trecho que quer compartilhar;
- Create new (ícone de “+” entre a barra de pesquisa e perfil);
- new gist;
- Preencher campo do nome do arquivo e trecho de código de cada campo, além de preencher a descrição;
- Se tiver mais um trecho que quiser adicionar, clique “Add file”;
- Escolher deixar o gist público ou não, pela seta do lado do “create secret gist”;
- Clicar no create;
- Para compartilhar é só copiar o link da página web: https://gist.github.com/Lucas-ZC/638945c1ac2b8a16f7e3f4126087d00f.

***Adicionar cobra no readme:***
<div align="center">

  ![Snake animation](https://github.com/Lucas-ZC/Lucas-ZC/blob/snake/github-contribution-grid-snake.svg)
</div>

- Ir no repositório do readme do perfil;
- Settings;
- Pages;
- No Build and deployment, se o source for "deploy from a branch" mude pra GitHub Actions;
- Actions;
- New workflow;
- Set up a workflow yourself;
- Veja se o nome está main.yml;
- Copie e cole esse código (Não precisa alterar nada):
  
```
name: Generate Snake Animation
on:
  schedule:
    - cron: "0 14 * * *"
  workflow_dispatch:
  push:
    branches: [ main ]

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5
    
    steps:
      - name: Checkout repository
        uses: actions/checkout@v4
        with:
          token: ${{ secrets.GITHUB_TOKEN }}
          
      - name: Generate snake animation
        uses: Platane/snk@v3
        with:
          github_user_name: usuario <--------------- Alterar aqui
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
          
      - name: Deploy to snake branch
        run: |
          git config --global user.name "github-actions[bot]"
          git config --global user.email "41898282+github-actions[bot]@users.noreply.github.com"
          
          git checkout --orphan snake || git checkout snake
          git rm -rf . || echo "Nothing to remove"
          cp -r dist/* . 2>/dev/null || echo "No files in dist/"
          
          git add .
          git commit -m "Update Snake animation" || echo "No changes"
          git push origin snake --force
  ```
- Commit changes;
- Commit changes;
- Volte em Actions;
- generate animation;
- Run workflow;
- Run workflow;
- Va para seu readme e copiei e cole isso (Alterando "Usuario" pelo seu nome do github):
```
<div align="center">

  ![Snake animation](https://github.com/Usuario/Usuario/blob/snake/github-contribution-grid-snake.svg)
</div>
```
- Va no seu readme do perfil, e veja como ficou.
- Meu perfil de exemplo: https://github.com/Lucas-ZC/Lucas-ZC/blob/main/README.md

***Adicionar pacman no readme:***
<picture>
  <img src="https://raw.githubusercontent.com/Lucas-ZC/Lucas-ZC/output/pacman-contribution-graph-dark.svg" alt="Pac-Man contribution graph" width="100%">
</picture>

- Actions;
- New workflow;
- Set up a workflow yourself;
- Deixe o nome como "pacman.yml";
- Copie e cole esse código (Alterar usuario para seu nome do github): 
```
name: Generate Pac-Man Game
on:
  schedule:
    - cron: "0 12 * * *"
  workflow_dispatch:
  push:
    branches: [ main ]

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5
    
    steps:
      - name: Checkout repository
        uses: actions/checkout@v4
        with:
          token: ${{ secrets.GITHUB_TOKEN }}
          
      - name: Generate pacman-contribution-graph.svg
        uses: abozanona/pacman-contribution-graph@main
        with:
          github_user_name: usuario <--------------- Alterar aqui

      - name: Deploy to output branch
        run: |
          git config --global user.name "github-actions[bot]"
          git config --global user.email "41898282+github-actions[bot]@users.noreply.github.com"
          
          git checkout --orphan output || git checkout output
          git rm -rf . || echo "Nothing to remove"
          cp -r dist/* . 2>/dev/null || echo "No files in dist/"
          
          git add .
          git commit -m "Update Pacman graph" || echo "No changes"
          git push origin output --force
```
- Commit changes;
- Commit changes;
- Volte em Actions;
- Generate Pac-Man Game;
- Run workflow;
- Run workflow;
- Va para seu readme e copiei e cole isso (Alterando "Usuario" pelo seu nome do github):
```
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Usuario/Usuario/output/pacman-contribution-graph-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Usuario/Usuario/output/pacman-contribution-graph.svg">
  <img alt="Pac-Man contribution graph" src="https://raw.githubusercontent.com/Usuario/Usuario/output/pacman-contribution-graph.svg">
</picture>
```
- Va no seu readme do perfil, e veja como ficou.
- Meu perfil de exemplo: https://github.com/Lucas-ZC/Lucas-ZC/blob/main/README.md
