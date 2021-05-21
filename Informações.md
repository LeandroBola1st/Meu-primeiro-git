#  Coisas que eu devo lembrar do Git :100: 

###  Lista de comandos em Git

##### Geral

```
git help
```

##### Comando específico

```
git help add
git help commit
git help <qualquer_comando_git>
```

##### Setar usuário

```
git config --global user.name "L..."
```

##### Setar email

```
git config --global user.email l....
```

##### Setar editor

```
git config --global core.editor vim
```

##### Setar ferramenta de merge

```
git config --global merge.tool vimdiff
```

##### Setar arquivos a serem ignorados

```
git config --global core.excludesfile ~/.gitignore
```

##### Listar configurações

```
git config --list
```

###  Repositório Local

### Criar novo repositório

```
git init
```

### Verificar estado dos arquivos/diretórios

```
git status
```

### Adicionar arquivo/diretório (staged area)

##### Adicionar um arquivo em específico

```
git add meu_arquivo.txt
```

##### Adicionar um diretório em específico

```
git add meu_diretorio
```

##### Adicionar todos os arquivos/diretórios

```
git add .	
```

##### Adicionar um arquivo que esta listado no .gitignore (geral ou do repositório)

```
git add -f arquivo_no_gitignore.txt
```

###  Comitar arquivo/diretório

##### Comitar um arquivo

```
git commit meu_arquivo.txt
```

##### Comitar vários arquivos

```
git commit meu_arquivo.txt meu_outro_arquivo.txt
```

##### Comitar informando mensagem

```
git commit meuarquivo.txt -m "minha mensagem de commit"
```

### Remover arquivo/diretório

##### Remover arquivo

```
git rm meu_arquivo.txt
```

##### Remover diretório

```
git rm -r diretorio
```

## Repositório Remoto

### Exibir os repositórios remotos

```
git remote

git remote -v
```

### Vincular repositório local com um repositório remoto

```
git remote add origin git@github.com:leocomelli/curso-git.git
```

### Exibir informações dos repositórios remotos

```
git remote show origin
```

### Renomear um repositório remoto

```
git remote rename origin curso-git
```

### Desvincular um repositório remoto

```
git remote rm curso-git
```

###  Enviar arquivos/diretórios para o repositório remoto

O primeiro push de um repositório deve conter o nome do repositório remoto e o branch.

```
git push -u origin master
```

Os demais pushes não precisam dessa informação

```
git push
```

###  Atualizar repositório local de acordo com o repositório remoto

##### Atualizar os arquivos no branch atual

```
git pull
```

##### Buscar as alterações, mas não aplica-las no branch atual

```
git fetch
```

### Clonar um repositório remoto já existente

```
git clone git@github.com:l...
```