# Comandos Básicos - Trabalhando com o Git bash:

### Abaixo falaremos de todos os comando básico, entretanto já é o suficiente para começar a trabalhar com o GIT/GITHUB.


## No terminal:

$ pwd -> mostra o caminho completo do diretorio no qual estamos dentro;
$ ls -> lista tudo que está dentro da pasta/repositório no qual estamos dentro (exceto os arquivos/pastas oucultas);
$ ls -a -> lista arqvuivos/pastas ocultas;
$ clear -> limpar toda tela que estamos trabalhando, também podemos usar o atalho do teclado (Ctrl+l);

## Trabalhando com pasta/arquivos:

$ cd.. -> retroceder apenas um nível de pasta;
$ cd + / -> nos leva para diretório base;
$ cd + esapaço + "nome da pasta" -> para entrar em um pasta, que tem dentro da pasta/repositório que estamos;
$ mkdir + esapaço + "nome da pasta" -> para criar uma pasta; 
$ rmdir + "nome da pasta" /S /Q - para remover todo pasta/repositório com tudo que está dentro;
$ echo + "algo" -> imprime algo na tela;
$ echo + > + "nome_do_arquivo.txt" -> cria um arquivo(lembresse de passar a extensão do arquivo que você vai criar);
del - para deletar os arquivos dentro de uma pasta



cat - comando especial para ler o conteudo de uma chave SSH


para inicializar a entidade ssh-agent, entidade que fica responsável por pegar as chaves e lidar com elas:
$ eval $(ssh-agent -s)
----saida
Agent pid 924

agora vamos passar a chave apara o SSH-AGENT:
$ ssh-add id_ed25519
---saida
Enter passphrase for id_ed25519: ----confirma a senha criada
---nova saida
Identity added: id_ed25519 (mxs2003@gmail.com)



''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

$ mv receita.md ./receitas/ - mv(move) o arquivo "receita.md" para pasta "./receitas/"

$git init - para o git começar a versionar nosso código

$ git config --global user.email "mxs2003@gmail.com" - para setar as gonfigurações de forma global
$ git config --global user.name "Mxs"

---- após alternar/para de trabalhar no código 

$ git add *

$ git commit -m "commit inicial"
---- saida ---
[master (root-commit) e7f737b] commit inicial
 1 file changed, 19 insertions(+)
 create mode 100644 receita.md


$ git status

$ git add receita.md receitas/ - add um arquivo e uma pasta que cabamos de modificar/criar

$ git commit -m "cria pasta receitas, move arquivo para receitas"
[master ed7b118] cria pasta receitas, move arquivo para receitas
 1 file changed, 0 insertions(+), 0 deletions(-)
 rename receita.md => receitas/receita.md (100%)

$ git add * - adiciona todos os arquivos, pastas, modificações para área de unistage para ser commitados
$ git add . - adiciona todos os arquivos, pastas, modificações para área de unistage para ser commitados

$ git config --list - vai trazer toda a lista de configuração que está no seu git

para reconfigurar, para apagar as configurações feitas anteriormente

$ git config --global --unset user.email - apaga o e-mail, precisa refazer a config

$ git config --global --unset user.name - apaga o nick-name, precisa refazer a config

após criar um repositório online no site da github, precisamos apontar em nosso git bash:
"informações do site github"
…or push an existing repository from the command line
git remote add origin git@github.com:MoisesXavier/Livro-Receitas.git
git branch -M main
git push -u origin main
...

1º precisamos adicionar a origem REMOTO:
git remote add origin git@github.com:MoisesXavier/Livro-Receitas.git
