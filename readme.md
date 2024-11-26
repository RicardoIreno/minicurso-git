# Minicurso de git

## Introdução

Este documento é um resumo dos comandos mais usados no git, a ferramenta de controle de versão. 

### Como esse documento funciona

Este documento está salvo em formato markdown (.md), uma linguagem de marcação simples que permite o uso de formatação, links e imagens sem a necessidade de usar marcações mais complexas. 


Exemplo das marcações em markdown:
```md
# título principal
## título 2
### título 3
#### título 4

*itálico*
**negrito**

- ítem de lista
- ítem de lista

1. ítem de lista numerada
2. ítem de lista numerada

[texto do link](http://endereco.do.link)

![Texto alternativo da imagem](http://endereco.da.imagem.jpg)

```
O formato markdown é lido por editores:
- [VS Code](https://code.visualstudio.com) editor de códigos da Microsoft
- [Atom](https://atom-editor.cc) editor de códigos do Github
- [StackEdit](https://stackedit.io) editor de textos online
- [Logsec](https://logseq.com) aplicativo de anotações open source
- [Obsidian](https://obsidian.md) aplicativo de anitações gratuito
- [Notion](https://www.notion.com) aplicativo de anitações freemium


A conversão é para outros formatos como `.html` ou `.doc` pode ser fácilmente feita com o aplitcativo de linha de comando [Pandoc](https://pandoc.org)

## Básico do Git

### 1. Configuração inicial

Após a instalação, use os seguintes comandos no terminal para a configuração básica do git.

```shell
git config --global user.name "seu nome"
git config --global user.email fulanodetal@exemplo.br
git config --global core.editor "editor-de-sua-preferencia"
```

Ao configurar `core.editor`, é preciso que o editor a ser usado esteja configurado na variável PATH do sistema, mas a maioria dos editores de código já faz isso na instalação. O VS Code, por exemplo, adiciona a variável "vscode".


### 2. Repositórios

**Inicializando**

```shell
git init
```

Com o repositório inicializado, se você pretende clonar outro repositório, use o comando ``git remote add endereco-do-repositorio`` para adicionar o endereço deste repositório.

Exemplo: 

Adicionando um repositório local:
```shell
git remote add D:\dev\repositorio
```

Adicionando um repositório que você criou no Github ou Gitlab:

```shell
git remote add git@github.com:seunickname/seurepositotio.git
```

## 3. Conceitos básicos

### O conceito de staging area e commited.

- **staging area:** área intermediária onde você prepara (stage) as alterações antes de confirmá-las (commit). 
- **commit:** é o registro das alterações no repositório. É como um "snapshot", um marco em uma linha do tempo.
- Qualquer arquivo que não foi adicionado ao registro, e também não está na staging area, são mostrados em vermelho.


**Inserir arquivos na *staging area*:**

```shell
git add nome-do-arquivo
```

**Gravar os arquivos no registro (commit)**:

```shell
git commit -m "mensagem"
```

**Verificar o status do repositório:**

```shell
git status
```

**Verificar o histórico de commits:**

```shell
git log
```

Apenas os três últimos:
```shell
git log -3
```

De um commit A  a um commit B:
```shell
git log A...B
```

De um autor específico:
```shell
git log --author=usuario
```

**Para verificar as mudanças no conteúdo de um arquivo:**
```shell
git diff
```

