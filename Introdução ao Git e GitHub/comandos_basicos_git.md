# Comandos B�sicos - Trabalhando com o Git bash:

### Abaixo falaremos de todos os comando b�sico, entretanto j� � o suficiente para come�ar a trabalhar com o GIT/GITHUB.


## No terminal:

$ pwd -> mostra o caminho completo do diretorio no qual estamos dentro;
$ ls -> lista tudo que est� dentro da pasta/reposit�rio no qual estamos dentro (exceto os arquivos/pastas oucultas);
$ ls -a -> lista arqvuivos/pastas ocultas;
$ clear -> limpar toda tela que estamos trabalhando, tamb�m podemos usar o atalho do teclado (Ctrl+l);

## Trabalhando com pasta/arquivos:

$ cd.. -> retroceder apenas um n�vel de pasta;
$ cd + / -> nos leva para diret�rio base;
$ cd + esapa�o + "nome da pasta" -> para entrar em um pasta, que tem dentro da pasta/reposit�rio que estamos;
$ mkdir + esapa�o + "nome da pasta" -> para criar uma pasta; 
$ rmdir + "nome da pasta" /S /Q - para remover todo pasta/reposit�rio com tudo que est� dentro;
$ echo + "algo" -> imprime algo na tela;
$ echo + > + "nome_do_arquivo.txt" -> cria um arquivo(lembresse de passar a extens�o do arquivo que voc� vai criar);
del - para deletar os arquivos dentro de uma pasta



cat - comando especial para ler o conteudo de uma chave SSH


para inicializar a entidade ssh-agent, entidade que fica respons�vel por pegar as chaves e lidar com elas:
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

$git init - para o git come�ar a versionar nosso c�digo

$ git config --global user.email "mxs2003@gmail.com" - para setar as gonfigura��es de forma global
$ git config --global user.name "Mxs"

---- ap�s alternar/para de trabalhar no c�digo 

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

$ git add * - adiciona todos os arquivos, pastas, modifica��es para �rea de unistage para ser commitados
$ git add . - adiciona todos os arquivos, pastas, modifica��es para �rea de unistage para ser commitados

$ git config --list - vai trazer toda a lista de configura��o que est� no seu git

para reconfigurar, para apagar as configura��es feitas anteriormente

$ git config --global --unset user.email - apaga o e-mail, precisa refazer a config

$ git config --global --unset user.name - apaga o nick-name, precisa refazer a config

ap�s criar um reposit�rio online no site da github, precisamos apontar em nosso git bash:
"informa��es do site github"
�or push an existing repository from the command line
git remote add origin git@github.com:MoisesXavier/Livro-Receitas.git
git branch -M main
git push -u origin main
...

1� precisamos adicionar a origem REMOTO:
git remote add origin git@github.com:MoisesXavier/Livro-Receitas.git
