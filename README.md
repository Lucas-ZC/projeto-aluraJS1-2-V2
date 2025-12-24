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
- enter;
- enter;
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
