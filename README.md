# Desafio sobre o projeto de Git/GitHub da dio
Repositório criado para o desafio de projeto

## 1 - Inicie o git na sua pasta através do git bash ou terminal
### Todo repositørio Git armazena as informações dentro de uma pasta oculta chamada “/.git”. Para que os arquivos de uma pasta possam ser versionados pelo Git, é preciso iniciar o repositório. Basta executar o comando abaixo:
```r
$ git init
```

## 2 - Apagando um repositório
### Há momentos em que não queremos apagar nossos arquivos, mas queremos remover as informações sobre aquele repositório criado com o $ git init (talvez criar um repositório novo com os mesmos arquivos). Para isso não usamos o Git. Lembre-se que um repositório Git armazena as informações dentro de uma pasta oculta chamada /.git. Então basta apagar esta pasta oculta que o seu atual diretório deixará de ser um repositório.
```r
$ rm -rf .git
```

## 3 - Listando Arquivos Modificados
### Esse comando indica o estado do seu repositório. Em outras palavras, ele vai listar todos os arquivos que foram modificados desde o seu último commit.
```r
$ git status
```

## 4 - Desfazendo Alterações
### Poderíamos ter um post inteiro apenas falando sobre como desfazer alterações no Git, já que há vários cenários possíveis. Mas vamos resumir os principais:

##4.1 - Arquivos não monitorados
Se o arquivo foi modificado mas você ainda não executou git add, um simples git checkout removerá as alterações, deixando o arquivo como ele estava no último commit. Passe o nome do arquivo a ter as alterações desfeitas ou . para desfazer as alterações em todos os arquivos modificados. Muito útil se você está apenas experimentando um código mas não quer que ele seja salvo.
```r
git checkout .
```

### Esse comando não apaga novos arquivos. Para apagar novos arquivos que ainda não foram adicionados ao Stage, execute:
```r
git clean -df
```

## 4.2 - Removendo arquivos do Stage
### Se você executou git add e quer desfazer, use o reset.
```r
git reset
```
## 4.3 - Desfazendo o último commit
### Caso você tenha feito alterações e já tenha chegado a realizar um commit, para desfazer é necessário usar o revert.
```r
git revert HEAD
```

## 5 - Renomear Commit
### Escreveu algo errado no último commit? Esse comando te permite renomear a mensagem do último commit feito:
```r
git commit --amend
```

## 6 - Branches
### Sempre é bom não trabalhar apenas na main para evitar problemas e ter um projeto mais flexível.

## 6.1 - Listando Branches
Esse comando lista todas as branches presentes no repositório do seu computador.
```r
git branch
```

### Caso você queira que ele liste também as branches que estão no repositório remoto, adicione -a:
```r
git branch -a
```

## 6.2 - Indo para outra branch
### Para mudar para uma outra branch basta usar o comando checkout, passando o nome da branch.
```r
git checkout minha-branch
```

### Se você adicionar -b, uma nova branch será criada.
```r
git checkout -b minha-nova-branch
```

## 6.3 - Excluindo branches
### Para excluir uma branch local basta executar o comando branch com -d ou -D, passando o nome da branch que você quer apagar.
```r
git branch -d nome-da-branch
git branch -D nome-da-branch
```

## 6.4 - Renomeando branches
### Para renomear a sua atual branch local, execute o comando branch com a opção -m, passando o novo nome.
```r
git branch -m novo-nome-da-branch
```
### Se você estiver em uma branch e quiser renomear outra, você deve passar primeiro o nome atual da branch que quer renomear:
```r
git branch -m nome-atual novo-nome
```

## 7 - Visualizando o Histórico de Commits
### Para visualizar o histórico de commits basta usar o seguinte comando:
```r
git log
```

## Desfazendo o último commit

## Links Úteis
[Sintaxe Básica Markdown](https://www.markdownguide.org/extended-syntax#:~:text=The%20basic%20Markdown%20syntax%20allows%20you%20to%20create,the%20lines%20before%20and%20after%20the%20code%20block.)
