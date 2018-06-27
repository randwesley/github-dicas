# Git e Github

## Criando um repositorio local com o GIT
Criando uma pasta, e se dirigindo ao terminal, no local da pasta criada, digite **git init** que a pasta selecionada vai passar receber a configuração padrão de um repositorio local.

## Comando git status

O comando serve para verificar qual o status dos arquivos que estão inseridos no repositorio .

## Adcionando arquivos ao git

Ao criar um arquivo dentro do repositorio, num primeiro momento ele é considerado **Untracked**, ou seja, ele foi criado na pasta mas não foi adicionado ao repositorio.

Para adicionar um arquivo, basta digitar o comando **git add nome.do.arquivo**, assim ele passa a ser considerado um arquivo **unmodified**, que foi adicionado e agora pode ser editado. 
Ao ser editado, ele passa a ser considerado um arquivo **modified**, e após isso pode ser **commitado** e assim é salvo um registro (log) da edição, que é chamado de **commit**.