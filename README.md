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
- `git add *.txt *.js *.css *.html` adiciona todos os arquivos com a extensão .txt, .js, .css e .html
- `git add *.txt *.js *.css *.html *.php` adiciona todos os arquivos com a extensão .txt, .js, .css, .html e .php
- `git add *.txt *.js *.css *.html *.php *.py` adiciona todos os arquivos com a extensão .txt, .js, .css, .html, .php e .py

## git commit
- comando para salvar as alterações no git 
- `git commit -m "mensagem"` salva as alterações com a mensagem especificada
- `git commit -am "mensagem"` adiciona e salva as alterações com a mensagem especificada
- `git commit -a -m "mensagem"` adiciona e salva as alterações com a mensagem especificada
- -a adiciona todos os arquivos que foram alterados
- -m adiciona a mensagem


## git config
- comando para configurar o git




## git status
- comando para verificar o status do git

