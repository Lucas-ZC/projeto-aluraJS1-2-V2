# Projeto de Treinamento de ***Git*** e ***GitHub***

![Badge Finalizado](http://img.shields.io/static/v1?label=STATUS&message=FINALIZADO&color=GREEN&style=for-the-badge)

<h2>Sobre </h2>
Projeto utilizado no curso do Alura para ensino de Git e GitHub 
<div align="left">
  <br>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" height="120" alt="git logo" />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" height="120" alt="git logo" />
  <img width="12" />
</div>

<h2>O que foi passado </h2>

<h3>Comandos do Terminal </h3>
OBS: onde houver parênteses são variáveis para serem substituídas

- ***git init*** -> inicia o Git
- ***git add .*** -> adiciona todos arquivos ao Git. Se no lugar do ponto for escrito o nome de um dos arquivos, esse arquivo que será adicionado
- ***git add README.md*** -> adiciona README
- ***git commit -m “texto”*** -> faz commit com o título digitado
- ***git config --global user.email “@gmail.com”*** -> salvar email
- ***git config --global user.name “Fulano”*** -> salvar nome
- ***git branch -M main*** -> renomeia a branch atual para main
- ***git status*** -> status das últimas alterações
- ***git remote add origin link do ssh do Git hub*** -> adiciona um repositório remoto, com o URL do seu repositório no GitHub via SSH
- ***git remote*** -> listar repositórios remotos
- ***git push -u origin main*** -> Envia seus commits locais para o repositório remoto no GitHub e configura o rastreamento da branch
- ***git push origin main*** -> envia os commits do repositório local pro repositório remoto
- ***git pull origin main*** -> pega os commits do repositório remoto pro local
- ***git (comando git) --help*** -> mostra um manual completo de como usar o comando git selecionado
- ***git log*** -> mostra histórico de commits
- ***git log --oneline*** -> mostra no terminal apenas o hash (código) e nome do commit
- ***git log -p*** -> mostra git log normal + diff (linhas de código adicionadas e removidas)
- ***git log --graph*** -> mostra o log com várias linhas verticais e ramificações que facilitam localizar commits, merges ou separação de branches
- ***git log --help*** -> mostra um manual de como usar o git log (muito grande) que pode aparecer no terminal ou na guia do navegador. Dica, se aparecer no terminal, digitando “/” seguido da informação que quer buscar, onde essa palavra aparecer, ela será destacada
- ***git log --format=”%H %an”*** -> mostra um log com as informações e ordem escolhidas entre as aspas duplas, neste caso mostra o hash (código) e nome do usuário. Para saber melhor como usar “git log –format”, use “git log --help” e em seguida “/PRETTY FORMATS”, essa é a parte que essas informações estão
- ***git show (hash do commit)*** -> mostra as informações completas do commit escolhido, com hash, autor, data, mensagem e diff, se não tiver nenhum hash ele mostra as informações do último commit
- ***git diff (parâmetro1)..(parâmetro2)*** -> compara dois estados do repositório, que podem ser commits, branches ou referências como HEAD, mostrando as diferenças entre eles
- ***git revert (id do commit no git log)*** -> reverte o commit fazendo um commit
- ***git reset  --hard (hash)*** -> desfaz commits e alterações no código, voltando exatamente ao estado do commit informado
- ***git commit –amend -m “mensagem”*** -> - ***git commit --amend*** -> altera o último commit, permitindo mudar a mensagem e/ou incluir arquivos esquecidos; para incluir arquivos, use git add no arquivo desejado e depois execute o amend
- ***git branch*** -> mostra as branches disponíveis
- ***git branch -d (branch)*** -> deleta a branch digitada
- ***git switch (branch)*** -> troca para a branch digitada
- ***git switch -c (branch)*** -> cria e troca para a branch criada
- ***git merge (branch)*** -> junta a branch informada à branch atual, preservando o histórico, normalmente criando um commit de merge
- ***git rebase (branch)*** -> reaplica os commits da branch atual em cima da branch informada, atualizando a branch ramificada e criando um histórico linear (sem commit de merge)
- ***git stash*** -> guarda mudanças temporariamente sem criar commit ou branch, ou seja, não vai para o histórico do Git. Ele permite trocar de branch sem perder trabalho em andamento. Dica: é útil quando surgem erros mais urgentes e é necessário mudar de branch; usando git stash, as alterações ficam salvas localmente, evitando commits temporários que poluem o histórico
- ***git stash push -m "nome"*** -> faz o mesmo que o git stash, mas é possível nomear o stash criado
- ***git stash pop*** -> libera o que foi salvo no último git stash da lista, e o remove dessa lista
- ***git stash apply (índice)*** -> aplica o stash do índice informado, sem removê-lo da lista. Dica: para ver o índice use 'git stash list'
- ***git stash list*** -> lista o que está salvo no stash
- ***git stash clear*** -> exclui o que está na lista do stash
- ***git restore .*** -> descarta alterações locais e restaura os arquivos para o estado do último commit. O ponto pode ser substituido por um dos arquivos do projeto
- ***git restore --staged (nome do arquivo)*** -> remove arquivos da staging area, desfazendo um git add sem perder as alterações no código
- ***git restore --source=(hash) (nome do arquivo)*** -> restaura o arquivo para a versão presente no commit informado, substituindo a versão atual do arquivo
- ***git tag*** -> lista todas as tags salvas do Git da máquina
- ***git tag "nome da versão" (hash do commit)*** -> cria uma tag que marca o commit informado. Geralmente usada para marcar versões do projeto (ex: v1.0, v2.3.4). Se o hash não for informado, a tag aponta para o commit atual. Por padrão, tags não são enviadas ao GitHub automaticamente
- ***git push origin --tags*** -> manda as tags do repositório local pro remoto. Dica: é possível mandar apenas uma tag específica substituindo o "--tags" pelo nome da tag
- ***git tag -d (tag)*** -> deleta a tag digitada. Dica: se tiver usado push origin dessa tag é necessário tirar do repositório remoto também
- ***git tag -a (tag) -m "mensagem"*** -> cria uma tag com mensagem
- ***git tag -v (tag)*** valida e mostra informações de uma annotated tag, mas se não tiver anotação nela não funciona
- ***git cherry-pick (hash)*** -> puxa um commit especifico de outra branch e aplica
- ***git blame (arquivo)*** -> mostra linha por linha do arquivo, o commit que foi criada ou modificada, hash, quem fez, hora e o que foi alterado


<h3>Tutoriais </h3>

***PC não conectado com o Git/gerar chave SSH:***
- ssh-keygen -t ed25519 -C "SEU EMAIL AQUI” (terminal);
- Enter e depois mais um enter;
- Pasta(do pc);
- Pasta de usuário;
- .ssh;
- Conferir os arquivos e ver qual é a chave pública e copiar;
- settings (da conta);
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
- Pra pasta: nome/, pra arquivo especifico: exemplo.txt, pra passar um padrão: *.css

***Compartilhar códigos (com o gist):***
- Ir na tela inicial do repositório com o trecho que quer compartilhar;
- Create new (ícone de “+” entre a barra de pesquisa e perfil);
- new gist;
- Preencher campo do nome do arquivo e trecho de código de cada campo, além de preencher a descrição;
- Se tiver mais um trecho que quiser adicionar, clique “Add file”;
- Escolher deixar o gist público ou não, pela seta do lado do “create secret gist”;
- Clicar no create;
- Para compartilhar é só copiar o link da página web: https://gist.github.com/Lucas-ZC/638945c1ac2b8a16f7e3f4126087d00f.

***Publicar um release:***
- No canto direito da área code, clique em "Create a new release";
- Select a tag
- Selecione a tag que quer fazer o release
- Em release title, dê um título
- Em Write, escreva sobre o projeto. Dica: Clicando em "generate release notes", quem acessar o link terá acesso a um diff do que teve de diferente do código da tag recente e a tag antecessora.

<h3>Conceitos </h3>
- branch: ramificações ou linhas de trabalho no projeto, por exemplo a main
- head: 'último commit', é a branch que está no código.
- staging area: é a área onde ficam os arquivos preparados para serem commitados. Arquivos entram nela com git add e saem com git restore --staged.
- Repositório: é um local de armazenamento digital, utilizado para gerenciar arquivos, documentos, código-fonte e outros recursos de um projeto.
- Hash: código que é único para cada commit, tendo em torno de 40 caracteres.
- Tag (do Git): rótulo que marca um commit específico, geralmente usado para versões (releases).
- Git: é um sistema de controle de versão local que mantém o histórico completo de alterações do projeto. Ele permite salvar versões do código por meio de commits, facilitando o retorno a estados anteriores. Além disso, possibilita o uso de 
branches, permitindo o desenvolvimento paralelo de funcionalidades e a posterior integração dessas mudanças à branch principal.
- GitHub: é uma plataforma que oferece hospedagem remota para repositórios Git, funcionando como backup e ponto central do projeto. Ele facilita a colaboração entre desenvolvedores por meio de pull requests, revisão de código e issues. Também é amplamente usado como portfólio público e fornece ferramentas adicionais, como GitHub Actions, automação e recursos de CI/CD.

***Adicionar cobra no readme:***
<div align="center">

  ![Snake animation](https://github.com/LucasZanellaCapitanio-dev/LucasZanellaCapitanio-dev/blob/output/github-contribution-grid-snake.svg)
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
- Vá para seu readme e copiei e cole isso (Alterando "Usuario" pelo seu nome do github):
```
<div align="center">

  ![Snake animation](https://github.com/Usuario/Usuario/blob/snake/github-contribution-grid-snake.svg)
</div>
```
- Vá no seu readme do perfil, e veja como ficou.
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
- Vá para seu readme e copiei e cole isso (Alterando "Usuario" pelo seu nome do github):
```
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Usuario/Usuario/output/pacman-contribution-graph-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Usuario/Usuario/output/pacman-contribution-graph.svg">
  <img alt="Pac-Man contribution graph" src="https://raw.githubusercontent.com/Usuario/Usuario/output/pacman-contribution-graph.svg">
</picture>
```
- Vá no seu readme do perfil, e veja como ficou.
- Meu perfil de exemplo: https://github.com/Lucas-ZC/Lucas-ZC/blob/main/README.md
