# Git e Github

## Criando um repositorio local com o GIT
Criando uma pasta, e se dirigindo ao terminal, no local da pasta criada, digite **git init** que a pasta selecionada vai passar receber a configuração padrão de um repositorio local.

## Comando git status

O comando serve para verificar qual o status dos arquivos que estão inseridos no repositorio .

## Adicionando arquivos ao git

Ao criar um arquivo dentro do repositorio, num primeiro momento ele é considerado **Untracked**, ou seja, ele foi criado na pasta mas não foi adicionado ao repositorio.

Para adicionar um arquivo, basta digitar o comando **git add nome.do.arquivo**, assim ele passa a ser considerado um arquivo **unmodified**, que foi adicionado e agora pode ser editado. 
Ao ser editado, ele passa a ser considerado um arquivo **modified**, e após isso pode ser **commitado** e assim é salvo um registro (log) da edição, que é chamado de **commit**.

epois do primeiro **commit**, o arquivo volta a ser **unmodified** e assim o ciclo se repete.

## Comando git commit

O comando diz para o repositorio pegar todas as alterações feitas em um determinado arquivo e salvar uma versão do mesmo. 
Isso é feito atraves do comando **git commit -m "A mensagem deve contar as informações referentes as ultimas alterações que o codigo sofreu."**

Ao realizar o commit, o sistema git informa as informações da alteração do arquivo, da seguinte forma.
[master (root-commit) c6ceca8] 
**master** = local onde a versão do arquivo foi salva
**root-commit** = o tipo de alteração que o arquivo sofreu, nesse caso, foi um commit.
**c6ceca8** = é o ID da versão atual do arquivo que foi salvo, assim, atraves dela, pode-se fazer com que o arquivo retorne a essa versão, com esse ID de registro.

## Comando git log

Atraves deste comando, é possivel verificar todo o historico de versões dos arquivos salvos no repositorio. Este historico é visto pelo id (c6ceca8) que o sistema cria, apos cada **commit**. 
Assim ao usar o comando, é possivel ver o **historico de commits**, assim como o autor e a data em que a versão do arquivo foi salva.

* Com o comando **git log --author="nome do autor"**, é possivel fazer pesquisas usando o nome do autor das alterações. 
* Com o comando **git shortlog**, é possivel verificar em ordem alfabetica quais são os autores que estão contribuindo para aquele repositorio, quais foram os seus commits e o numero de commits de um determinado autor.
* com o comando **git log --graph** que mostra em forma grafica o que está acontecendo com os branchs (locais) e as versões dos codigos.

### Comando git show

Ao usar o git log e verificar o ID de uma determinada versão, é possivel usar o comando **git show numero.do.id** para acompanhar qual foi a modificação que o arquivo obteve.

## Comando git diff

Este comando mostra qual foi a alteração que codigo obteve, antes mesmo de ser commitado.
O comando **git diff --name-only**, mostra apenas o nome do arquivo que foi modificado. Assim, é mais facil perceber quais arquivos foram modificados.
