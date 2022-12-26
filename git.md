## Git Basic Commands List

### Nome do seu perfil

* git config --global user.name "nome"

### Seu email do perfil

* git config --global user.email "email"

### Editor de código utilizado

* git config --global core.editor sublime (para outros editores)

* git config --global core.editor 'code --wait' (para vscode)

### Mostrar todas as configurações do git

* git config --list

### Mostrar o username e email

* git config user.name

* git config user.email

### Inicializar repositório local

* git init

### Ver o status do repositório

* git status

- novos arquivos ficam no estágio untracked, para alterar é so dar o comando git add nomedoarquivo que passará a ficar no estágio de pré commit.

- Quando modificada utilizar o mesmo comando para voltar ao estágio de pré commit: git add nomedoarquivo.

### Para comitar

* git commit -m "comentário"

### Para verificar alterações

* git log

### Para verificar alterações de maneira mais detalhada

* git log --decorate

### Para verificar por autores

* git log --author="Nome do usuário ou autor"

### Para verificar os commits em repositórios

* git sl

### Verificando apenas os nomes e quantidade de commits

* git sl -sn

### Verificação em forma gráfica das alterações (branches, merges, commits)

* git log --graph

### Verificação de alterações por meio do hash

* git show "Aqui vai o hash sem aspas"

### Verificação das alterações por linhas

* git diff

### Verificação do nome do arquivo modificado apenas

* git diff --name-only

### Comitar sem adicionar

* git commit -am "Comentário"

### Desfazer modificação recente

* git checkout Nomedoarquivo

### Retirar um arquivo do estágio de staged

* git reset HEAD Nomedoarquivo

### Reset em um arquivo comitado

* git reset --soft hash (reseta o arquivo para um estágio anterior ao commit (staged) sem modificar)

* git reset --mixed hash (reseta o arquivo para dois estágios anteriores ao commit (modified) pronto para staged)

* git reset --hard hash (apaga completamente o arquivo comitado e aponta para o escolhido)

- obs: sempre apontar para o hash do commit anterior ao que quer resetar, se não vai dar erro de apontamento

### Corrigir último commit sem resetar

* git commit --amend -m 'comentário correto'

### Gerar chave ssh

* ssh-keygen -t ed25519 -C "your_email@example.com"

### Diretório padrão para acessar a chave ssh

* cd ~/.ssh/

### Conectando o repositório local com o do github

* git remote add origin git@github.com:nome-usuário/nome-repositório.git

### Checando a existencia do repositório

* git remote

### Mais informações

* git remote -v

### Comandos restantes para transferir do repo local para o do github

* git branch -M main

* git push -u origin main

### Alterando e enviando atualizações do local para o remoto

* git push origin main

### Clonando repositório remoto para local

* git clone git@github.com:usuario/nome-repositorio.git exemplo-nome (nome do repo local da sua escolha)
(vai estar no botão code de cada repositório)

### Fazendo fork (clicar no botão fork em cima do repositório e escolher a organização da sua preferência) (abir pull-request para contribuir com o código)

### Criando branches

* git checkout -b nome_do_branch_novo

### Listando todos os branches

* git branch

### Navegando entre branches

* git checkout nome_do_branch

### Deletando branches

* git branch -D nome_do_branch

### Merge

* git merge (nome do branch que vai juntar ao branch atual que voce está)

### Rebase

* git rebase (nome do branch que vai juntar ao branch atual que voce está)

### Stash

* git stash (salva o arquivo modified em estado WIP e apaga da lista de espera de commits)

### Aplicando o arquivo em WIP em outro banch novo

* git stash apply

### Listando os stashs recentes

* git stash list

### Configurando alias para atalhos de códigos

* git config --global alias.s status (exemplo)

### Tags para versionamento de software

* git tag -a Valordatag -m "mensagem da tag"

### Subindo a tag para o repositório

* git push origin main --tags

### Vendo todas as tags geradas

* git tag

### Apagando modificações sem dar reset

* git revert

### Apagando tags e branchs remotos (GitHub)

* git push origin :000 (tags)

* git push origin :nomedobranch (branches)

### Listando conexões com repo remoto

* git remote -v

### Apagando conexão com repo remoto

* git remote rm Nome_do_repo (ex: Origin)

### Juntando alterações do repositório remoto no diretório local

* git pull

### Listar conflitos existentes no código (diferenças)

* git diff <branch local> <branch alvo>

### Listar todos os conflitos existentes

* git diff

### Remover arquivos do diretório de trabalho

* git rm exemplo.txt