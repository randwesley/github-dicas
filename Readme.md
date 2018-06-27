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
