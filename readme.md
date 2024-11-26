# Minicurso de git

## Introdução

Este documento é um resumo dos comandos mais usados no git, a ferramenta de controle de versão. 

### Como esse documento funciona

Este documento está salvo em formato markdown (.md), uma linguagem de marcação simples que permite o uso de formatação, links e imagens sem a necessidade de usar marcações mais complexas. 


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

## Git

### Configuração inicial

Após a instalação, use os seguintes comandos no terminal para a configuração básica do git.

```shell
git config --global user.name "seu nome"
git config --global user.email fulanodetal@exemplo.br
git config --global core.editor "editor-de-sua-preferencia"
```

Ao configurar `core.editor`, é preciso que o editor a ser usado esteja configurado na variável PATH do sistema, mas a maioria dos editores de código já faz isso na instalação. O VS Code, por exemplo, adiciona a variável "vscode".
