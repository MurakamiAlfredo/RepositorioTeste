# Github

Git Para iniciantes

Este é um repositorio teste para ensinar como o git funciona.

Saiba mais no link: bla bla bla

Teste do git diff

Para criar uma conexão remota do git local com o github precisa fazer os seguintes passos.

git remote add "nome qualquer" "ssh do diretorio github"
verificar se fez digitando o seguinte comando

git remote <-- ira listar suas conexões remotas.

git remote -v <-- mostra os links detalhados.

Para puxar as informações do repositorio github e so digitar o seguinte comando:

git pull "nome da conexão remota" "nome da branch"

----------------------------------------------------------------------

editor de texto direto do prompt do git é o comando vim ou vi

Lembrar que os comandos importantes são: 

git log <-- mostra todos os logs dos commits feito pelo git
(
   opcoes do git log:
   --decorate <-- mostra de qual branch para qual branch, tags e merge.
   --author-"passar o nome" <-filtra os commits feitas por um usuario.
   --graph <-- mostra de forma grafica as mudanças feitas no git
)

git shortlog <-- Mostra em ordem alfabetica os nomes de quem fez commit e a quantidade de commit feita pelas pessoas e as descrições do commit
(-sn <-- mostra apenas o nome da pessoa e a quantidade de commits)
 
git diff <-- ver as diferenças das alterações antes de mandar para staged.
git show "valor da hash" <-- mostra as alterações feitas no commit da hash
git status <-- mostra em qual status está o git e os arquivos. 
git commit <-- lembrar de sempre usar o -m "texto do commit"

-----------------------------------------------------------------------

--Caso não deseja fazer a alteração do arquivo e resetar o arquivo.
git checkout "nome do arquivo"

Caso ele esteja já staged
git reset HEAD "nome do arquivo" <--voltar pro ponteiro que ja está, remover do staged o arquivo.

Como voltar as alterações ja feitas
primeiro digite o git log
pegar a hash que deseja fazer voltar
utilize o git reset 
tem 3 tipos o
--soft <-- volta para staged
--mixed <-- volta para modified
--hard <-- apaga o commit inteiro com as alterações.

ex: git reset --soft "codigo hash" <-- lembrar de sempre escolher um antes do que você deseja mudar/alterar. 

--------------------------------------------------------------------------------

para enviar as coisas para o github para atualizar precisa fazer o comando

git push "repositorio remoto" "branch atual"(master se for a principal)

--------------------------------------------------------------------------------
pra clonar um repositorio do github para a maquina é necessario fazer o seguinte

copiar o codigo ssh do repositorio no github. ir até o bash
sair da pasta do repositorio local e ir até um local do computador.
Depois disso digite o seguinte comando

g clone "codigo ssh" "nome da pasta que quer colocar os arquivos"


-------------------------------------------------------------------------------

Criação de Branch
O que é uma Branch <-- é um ponteiro que leva um commit
Ele cria um ponteiro que pode apontar para o ponteiro master que a branch principal do projeto.
Vantagens: 
--Pode modificar sem alterar o local principal (master)
--Facilmente "desligavel" <-- como ele não impacta diretamente ao projeto, ele pode facilmente ser deletado ou desfeito sem atrapalhar o serviço que outras pessoas estão fazendo em outra branch.
--Mutliplas pessoas trabalhando <-- Cada um cria uma branch e todos trabalham em conjunto sem problemas. Onde cada alteração acontece de forma separada. 
--Evita conflitos <-- Como as pessoas trabalham em branchs separadas não há concorrencia de uso de arquivo e modificação. Onde e somente feita após o tratamento dos conflitos pela mesclagem dos arquivos (MERGE).

para criar um Branch e so digitar o comando
git checkou -b "nome da branch"
e pronto o mesmo ja criou uma branch nova e está nela atualmente.

digitando
git branch <-- ele mostra todos os branchs existentes e o que tem asterisco e qual branch você está atualmente.

para alterar de branch é simples você deve usar o comando
git checkout "nome da branch"

se caso deseja apagar uma branch, voce deve fazer o seguinte comando:
git branch -D (precisa ser maiusculo) "nome da branch"

Alteração Teste Computador Mult.
Verificação de Teste Pull
ok.

testar em casa se consigo puxar essa informacao. se ela vier com pull será um grande avanço.

commit do branch master.

Teste Branch

---------------------------------------------------------------------------

Lembrar de fazer o pull na branch master sempre antes, pois pode haver alterações feitas pela outra pessoa.

git pull "nome da conexao remota" master

Funções do Merge

git merge "nome da branch"(nome da outra branch que você ira criar para fazer as alterações e etc). <-- o merge tem que ser feito na branch master.

vai aparecer uma tela informando que vai mesclar a branch na master.
clicar em esc e :wq
e prosseguir.

depois disso é só fazer o push <-- enviar os arquivos para o github.
git push "nome da conexao remota" master
