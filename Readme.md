# Git e Github

## Criando um repositorio local com o GIT
Criando uma pasta, e se dirigindo ao terminal, no local da pasta criada, digite **git init** que a pasta selecionada vai passar receber a configuração padrão de um repositorio local.

## Comando git status

O comando serve para verificar qual o status dos arquivos que estão inseridos no repositorio .

## Adicionando arquivos ao git

Ao criar um arquivo dentro do repositorio, num primeiro momento ele é considerado **Untracked**, ou seja, ele foi criado na pasta mas não foi adicionado ao repositorio.

Para adicionar um arquivo, basta digitar o comando **git add nome.do.arquivo**, assim ele passa a ser considerado um arquivo **unmodified**, que foi adicionado e agora pode ser editado. 
Ao ser editado, ele passa a ser considerado um arquivo **modified**, e assim, passa para o proximo passo, que é o **staged**, com isso pode ser **commitado** e assim é salvo um registro (log) da edição, que é chamado de **commit**.

Depois do primeiro **commit**, o arquivo volta a ser **unmodified** e assim o ciclo se repete.

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

### Comando git checkout

**git checkout nome.do.arquivo** Com este comando, o arquivo que sofreu alteração, retorna para o estado em que estava no ultimo commit, **esse comando é interessante para consertar erros antes de realizar o commit do arquivo**

#### Comando git reset

**git reset nome.do.arquivo** Este comando anula o envio das informações para o repositorio, cancelando assim o **git add**, que é feito antes de qualquer commit. Retirando assim o arquivo do **stage**.

Com ele, podemos também desfazer commits. através de duas formas: 
* **git reset HEAD~1**: Assim o commit é desfeito, mas as alterações no arquivo ainda ainda estão presentes. 

* **git reset --hard HEAD~1**: Assim tanto o commit, quanto a alteração no arquivo é desfeita.

#### Usando o git reset através do id de um commit

Existem três formas resetar um commit, cada uma com caractetisticas bem marcantes. sendo: 
* **soft** git reset --soft id.do.commit: retorna o arquivo pra um momento anterior ao commit. ao usa-lo, o commit é apagado, mas as alterações no arquivo permanecem.
* **mixed** git reset --mixed: retorna o arquivo pra o momento do modified
* **hard** git reset --hard: ignora o commit e tudo o que foi feito.


# Usando o Merge

O **merge = Mesclar**, vai unir os commits que foram feitos em **branchs diferentes**. mas ao fazer isso, ele vai criar um commit extra que serve como elo de ligação entre branchs.
* **git merge nome.do.branch**: Os commits realizados neste branch secundario, serão unidos aos commits realizados no branch master.

## Branchs

Um branch é um local onde todas as informações de um arquivo estão salvas. o primeiro branch a ser criado é o branch master, mas outros branchs podem ser criados para trabalhar de forma isolada num arquivo e depois mesclar as alterações feitas, ao arquivo no branch principal.

<strong id='#criaBranch'>**git checkout -b nome.do.branch**</strong>: Com esse comando cria-se um novo branch

**git branch**: Mostra os branchs existentes

**git checkout nome.do.branch**: Assim é possivel navegar  entre os branchs

**git branch -D nome.do.branch**: Com esse comando é possivel deletar um branch

# Contribuindo com a comunidade.

O melhor jeito de iniciar as contribuições para outros projetos, é fazendo o **fork** em um determinado projeto.
E o clonando para o seu repositorio (git) local.

* **git clone link.do.repositorio**: Assim é possivel clonar um projeto forkado que já vem com todos o historico de commits.

após fazer isso, é necessario <a href="#criaBranch">criar uma nova branch de trabalho</a>