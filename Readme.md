# Github

Git Para iniciantes

Este é um repositorio teste para ensinar como o git funciona.

Saiba mais no link: bla bla bla

Teste do git diff

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

