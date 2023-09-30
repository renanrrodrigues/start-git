# estudando git e github 

## git --version
- comando para verificar a versão do git


## git init 
- comando para iniciar o git no projeto 
- cria a pasta `.git` onde ficam os arquivos de configuração do git

## git status
- comando para verificar o status do git
- mostra os arquivos que foram alterados e não foram adicionados ao git 
- mostra os arquivos que foram adicionados ao git e não foram commitados
- mostra os arquivos que foram commitados e não foram enviados para o repositório remoto
- mostra os arquivos que foram enviados para o repositório remoto.

## git config
- comando para configurar o git
- `git config --global user.name "nome"` configura o nome do usuário
- `git config --global user.email "email"` configura o email do usuário
- `git config --global --add user.name "nome"` adiciona o nome do usuário
- `git config --global --add user.email "email"` adiciona o email do usuário
- `git config --global --add safe.directory "/mnt/8CBCCBABBCCB8DE0/workspace estudos/git"` adiciona o diretorio seguro


## git add
- comando para adicionar arquivos ao git 
- `git add .` adiciona todos os arquivos
- `git add --all` adiciona todos os arquivos
- `git add -A` adiciona todos os arquivos
- `git add -u` adiciona todos os arquivos que foram alterados
- `git add -p` adiciona os arquivos de forma interativa
- `git add nome_do_arquivo` adiciona o arquivo especificado
- `git add nome_do_arquivo1 nome_do_arquivo2` adiciona os arquivos especificados
- `git add pasta/` adiciona todos os arquivos da pasta
- `git add pasta/nome_do_arquivo` adiciona o arquivo especificado da pasta
- `git add pasta/nome_do_arquivo1 pasta/nome_do_arquivo2` adiciona os arquivos especificados da pasta
- `git add pasta1/ pasta2/` adiciona todos os arquivos das pastas
- `git add pasta1/nome_do_arquivo pasta2/nome_do_arquivo` adiciona os arquivos especificados das pastas
- `git add pasta1/nome_do_arquivo1 pasta1/nome_do_arquivo2 pasta2/nome_do_arquivo1 pasta2/nome_do_arquivo2` adiciona os arquivos especificados das pastas
- `git add *.txt` adiciona todos os arquivos com a extensão .txt
- `git add *.txt *.js` adiciona todos os arquivos com a extensão .txt e .js
- `git add *.txt *.js *.css` adiciona todos os arquivos com a extensão .txt, .js e .css
- `git add *.txt *.js *.css *.html` adiciona todos os arquivos com a extensão .txt, .js, .css e .html2
- `git add *.txt *.js *.css *.html *.php` adiciona todos os arquivos com a extensão .txt, .js, .css, .html e .php
- `git add *.txt *.js *.css *.html *.php *.py` adiciona todos os arquivos com a extensão .txt, .js, .css, .html, .php e .py


## git commit
- comando para salvar as alterações no git 
- `git commit -m "mensagem"` salva as alterações com a mensagem especificada
- `git commit -am "mensagem"` adiciona e salva as alterações com a mensagem especificada
- `git commit -a -m "mensagem"` adiciona e salva as alterações com a mensagem especificada
- -a adiciona todos os arquivos que foram alterados
- -m adiciona a mensagem

## git remote
- comando para adicionar o repositório remoto
- `git remote add origin https://github.com/renanrrodrigues/start-git.git` adiciona o repositório remoto
- `git remote -v` mostra os repositórios remotos
- `git remote rm origin` remove o repositório remoto
- `git remote set-url origin https://github.com/renanrrodrigues/start-git.git` altera o repositório remoto
- `git remote rename origin origin2` renomeia o repositório remoto

## git branch
- comando para criar um branch
- `git branch` mostra os branch
- `git branch -a` mostra os branch locais e remotos
- `git branch nome_do_branch` cria um branch
- `git branch -d nome_do_branch` deleta o branch
- `git branch -D nome_do_branch` deleta o branch forçadamente
- `git branch -m nome_do_branch` renomeia o branch
- `git branch -M nome_do_branch` renomeia o branch forçadamente mesmo se o branch tiver alterações não commitadas agora o branch será renomeado para nome_do_branch

## git push
- comando para enviar as alterações para o repositório remoto
- `git push -u origin main` envia as alterações para o repositório remoto
- `git push -u origin master` envia as alterações para o repositório remoto
- `git push -f origin main` envia as alterações forçadamente para o repositório remoto
- -u faz com que o git lembre que o branch master é o branch remoto
- `git push origin master` envia as alterações para o repositório remoto
- `git push origin nome_do_ramo` envia as alterações para o repositório remoto
- `git push origin :nome_do_ramo` deleta o ramo remoto
- `git push origin --delete nome_do_ramo` deleta o ramo remoto

## git checkout
- comando para trocar de branch, branch é uma linha do tempo
- `git checkout nome_do_branch` troca para o branch especificado
- `git checkout -b "nome_do_branch"` cria e troca para o branch especificado nome do branch não pode ter espaço
- por convenção o nome do branch deve ser o nome da feature que está sendo desenvolvida ex: feature/login ex: feature/cadastro ex: feature/alterar-senha
- convenção para nome de branch: 720-submodules-rc       722-add-billing-module  723-fix-highlighting    728-fix-homepage-css
- exemplo usando convenção:
- `git checkout -b "taskID-fix-home-page-css"` cria e troca para o branch especificado
- `git checkout -b "taskID-fix-button-in-sigin"` cria e troca para o branch especificado
- `git checkout .\index.html` volta o arquivo para o estado que estava no último commit

## git pull
- comando para receber as alterações do repositório remoto
- `git pull origin master` recebe as alterações do repositório remoto
- `git pull origin nome_do_branch` recebe as alterações do repositório remoto
- `git pull origin :nome_do_branch` deleta o branch remoto
- `git pull origin --delete nome_do_branch` deleta o branch remoto
- `git pull origin master --allow-unrelated-histories` recebe as alterações do repositório remoto
-  --allow-unrelated-histories permite que o git receba alterações de repositórios diferentes
- `git pull origin master --allow-unrelated-histories --allow-unrelated-histories` recebe as alterações do repositório remoto

## git merge
- comando para mesclar as alterações de um branch para outro branch
- `git merge nome_do_branch` mescla as alterações do branch especificado para o branch atual
- `git merge nome_do_branch --no-ff` mescla as alterações do branch especificado para o branch atual sem fazer o fast forward
- `git merge nome_do_branch --no-ff -m "mensagem"` mescla as alterações do branch especificado para o branch atual sem fazer o fast forward e adiciona a mensagem
- `git merge nome_do_branch --no-ff -m "mensagem" --no-edit` mescla as alterações do branch especificado para o branch atual sem fazer o fast forward e adiciona a mensagem e não abre o editor de texto
- `git merge nome_do_branch --no-ff -m "mensagem" --no-edit --no-verify` mescla as altera## git log
- comando para ver o histórico de commits
- `git log` mostra o histórico de commits
- `git log --oneline` mostra o histórico de commits de forma resumida
- `git log --oneline --decorate` mostra o histórico de commits de forma resumida e mostra os branch
- `git log --oneline --decorate --graph` mostra o histórico de commits de forma resumida, mostra os branch e mostra o gráfico
- `git log --oneline --decorate --graph --all` mostra o histórico de commits de forma resumida, mostra os branch, mostra o gráfico e mostra todos os branch

- `git log --oneline --decorate --graph --all --author="nome"` mostra o histórico de commits de forma resumida, mostra os branch, mostra o gráfico, mostra todos os branch e mostra os commits do autor especificado

- `git log --oneline --decorate --graph --all --author="nome" --since="data"` mostra o histórico de commits de forma resumida, mostra os branch, mostra o gráfico, mostra todos os branch, mostra os commits do autor especificado e mostra os commits feitos a partir da data especificada

- `git log --oneline --decorate --graph --all --author="nome" --since="data" --until="data"` mostra o histórico de commits de forma resumida, mostra os branch, mostra o gráfico, mostra todos os branch, mostra os commits do autor especificado, mostra os commits feitos a partir da data especificada e mostra os commits feitos até a data especificada

- `git log --oneline --decorate --graph --all --author="nome" --since="data" --until="data" --grep="palavra"` mostra o histórico de commits de forma resumida, mostra os branch, mostra o gráfico, mostra todos os branch, mostra os commits do autor especificado, mostra os commits feitos a partir da data especificada, mostra os commits feitos até a data especificada e mostra os commits que contém a palavra especificada

- `git log --oneline --decorate --graph --all --author="nome" --since="data" --until="data" --grep="palavra" -S"palavra"` mostra o histórico de commits de forma resumida, mostra os branch, mostra o gráfico, mostra todos os branch, mostra os commits do autor especificado, mostra os commits feitos a partir da data especificada, mostra os commits feitos até a data especificada, mostra os commits que contém a palavra especificada e mostra os commits que contém a palavra especificada

- `git log --oneline --decorate --graph --all --author="nome" --since="data" --until="data" --grep="palavra" -S"palavra" --stat` mostra o histórico de commits de forma resumida, mostra os branch, mostra o gráfico, mostra todos os branch, mostra os commits do autor especificado, mostra os commits feitos a partir da data especificada, mostra os commits feitos até a data especificada, mostra os commits que contém a palavra especificada, mostra os commits que contém a palavra especificada e mostra as estatísticas dos commits

- `git log --oneline --decorate --graph --all --author="nome" --since="data" --until="data" --grep="palavra" -S"palavra" --stat --patch` mostra o histórico de commits de forma resumida, mostra os branch, mostra o gráfico, mostra todos os branch, mostra os commits do autor especificado, mostra os commits feitos a partir da data especificada, mostra os commits feitos até a data especificada, mostra os commits que contém a palavra especificada, mostra os commits que contém a palavra especificada, mostra as estatísticas dos commits e mostra as alterações dos commits
ções do branch especificado para o branch atual sem fazer o fast forward e adiciona a mensagem e não abre o editor de texto e não verifica as regras de commit
- `git merge nome_do_branch --no-ff -m "mensagem" --no-edit --no-verify --no-commit` mescla as alterações do branch especificado para o branch atual sem fazer o fast forward e adiciona a mensagem e não abre o editor de texto e não verifica as regras de commit e não faz o commit

## git clean
- comando para limpar o repositório
- `git clean -n` mostra os arquivos que serão excluídos
- `git clean -f` exclui os arquivos
- `git clean -f -d` exclui os arquivos e as pastas
- `git clean -f -d -x` exclui os arquivos, as pastas e os arquivos ignorados


## git stash
- comando para guardar as alterações
- `git stash` guarda as alterações
- `git stash list` mostra as alterações guardadas
- `git stash apply` aplica as alterações guardadas
- `git stash drop` remove as alterações guardadas
- `git stash clear` remove todas as alterações guardadas

## git rm 
- comando para remover arquivos do git 
- `git rm -rf build` remove a pasta build e os arquivos do repositório, e nao do disco!
- `git rm nome_do_arquivo` remove o arquivo
- `git rm -r --cached myFolder` remove a pasta e os arquivos do repositório, e nao do disco!
- `git rm nome_do_arquivo -f` remove o arquivo forçadamente
- `git rm nome_do_arquivo -f --cached` remove o arquivo forçadamente e remove o arquivo do stage 

## git ignore
- arquivo para ignorar arquivos e pastas
- `.gitignore` arquivo para ignorar arquivos e pastas
- `*.log` ignora todos os arquivos com a extensão .log
- `*.config` ignora todos os arquivos com o nome config
- ignorar a pastas e subpastas 
- `node_modules/` ignora a pasta node_modules

'* é usado para corresponder a um caractere curinga'
'/ é usado para ignorar nomes de caminhos relativos ao arquivo .gitignore'
'# é usado para adicionar comentários ao arquivo .gitignore'

Aqui temos um exemplo de como pareceria um arquivo .gitignore:

### Ignore os arquivos de sistema do Mac
.DS_store/
.config/
.test/
pasta1/
pasta2/

### Ignore a pasta node_modules
node_modules/


### Ignore todos os arquivos de texto
*.txt
*.md
*.config
*.log

### Ignore arquivos relacionados às chaves de API
.env

### Ignore arquivos de configuração de SASS
.sass-cache
.sass-cache/


## git log
- comando para ver o histórico de commits
- `git log` mostra o histórico de commits
- `git log --oneline` mostra o histórico de commits de forma resumida
- `git log --oneline --decorate` mostra o histórico de commits de forma resumida e mostra os branch
- `git log --oneline --decorate --graph` mostra o histórico de commits de forma resumida, mostra os branch e mostra o gráfico
- `git log --oneline --decorate --graph --all` mostra o histórico de commits de forma resumida, mostra os branch, mostra o gráfico e mostra todos os branch

- `git log --oneline --decorate --graph --all --author="nome"` mostra o histórico de commits de forma resumida, mostra os branch, mostra o gráfico, mostra todos os branch e mostra os commits do autor especificado

- `git log --oneline --decorate --graph --all --author="nome" --since="data"` mostra o histórico de commits de forma resumida, mostra os branch, mostra o gráfico, mostra todos os branch, mostra os commits do autor especificado e mostra os commits feitos a partir da data especificada

- `git log --oneline --decorate --graph --all --author="nome" --since="data" --until="data"` mostra o histórico de commits de forma resumida, mostra os branch, mostra o gráfico, mostra todos os branch, mostra os commits do autor especificado, mostra os commits feitos a partir da data especificada e mostra os commits feitos até a data especificada

- `git log --oneline --decorate --graph --all --author="nome" --since="data" --until="data" --grep="palavra"` mostra o histórico de commits de forma resumida, mostra os branch, mostra o gráfico, mostra todos os branch, mostra os commits do autor especificado, mostra os commits feitos a partir da data especificada, mostra os commits feitos até a data especificada e mostra os commits que contém a palavra especificada

- `git log --oneline --decorate --graph --all --author="nome" --since="data" --until="data" --grep="palavra" -S"palavra"` mostra o histórico de commits de forma resumida, mostra os branch, mostra o gráfico, mostra todos os branch, mostra os commits do autor especificado, mostra os commits feitos a partir da data especificada, mostra os commits feitos até a data especificada, mostra os commits que contém a palavra especificada e mostra os commits que contém a palavra especificada

- `git log --oneline --decorate --graph --all --author="nome" --since="data" --until="data" --grep="palavra" -S"palavra" --stat` mostra o histórico de commits de forma resumida, mostra os branch, mostra o gráfico, mostra todos os branch, mostra os commits do autor especificado, mostra os commits feitos a partir da data especificada, mostra os commits feitos até a data especificada, mostra os commits que contém a palavra especificada, mostra os commits que contém a palavra especificada e mostra as estatísticas dos commits

- `git log --oneline --decorate --graph --all --author="nome" --since="data" --until="data" --grep="palavra" -S"palavra" --stat --patch` mostra o histórico de commits de forma resumida, mostra os branch, mostra o gráfico, mostra todos os branch, mostra os commits do autor especificado, mostra os commits feitos a partir da data especificada, mostra os commits feitos até a data especificada, mostra os commits que contém a palavra especificada, mostra os commits que contém a palavra especificada, mostra as estatísticas dos commits e mostra as alterações dos commits

