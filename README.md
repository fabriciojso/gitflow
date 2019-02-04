# GitFlow
Fluxo de trabalho com git + github

## Como instalar o gitflow

**Ubuntu**
```bash
sudo apt-get install git-flow
```
*[detalhes](https://github.com/petervanderdoes/gitflow-avh/wiki/Installing-on-Linux,-Unix,-etc.)*

## Como configurar um projeto

**Inicializar projeto**
```git
git flow init
```

## Fluxo de trabalho

**Iniciar uma feature (fix, feature, bug, etc)**
```git
git flow feature start nome-da-feature
```

**Fazer pull request da feature**
```git
git flow feature publish nome-da-feature
```

**Após PR ser aprovado**
```git
git checkout develop
git pull
git branch -d nome-da-feature
```

Caso a branch develop ainda não esteja associada ao `origin` você deverá rodar o seguinte comando:
```git
git branch --set-upstream-to=origin/develop develop
```
