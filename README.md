# About this repository

À remplir.

# Comment ajouter du contenu

--------------------------------------------------

## Créer une page

Mise à part la page d'accueil `index.md` et la page d'informations `about.md`, Les pages sont dans le dossier de la catégorie qui les concerne : `/guides`, `/sparql` ou `/projects`.

-------------------------

## Ce qu'il faut savoir :

### Instructions

* Une page s'écrit en markdown (cf [cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)), avec l'extension `.md` ou `.markdown`.
* Le menu de gauche (= menu de catégorie) est un fichier séparé situé dans le dossier `/_data`. Il faudra y ajouter la nouvelle page sur le modèle de celles déjà présentes, en prenant soin d'imiter l'indentation présente.
* Il faut ajouter un entête en YML avant le contenu en MarkDown. Cet entête doit au moins contenir comme paramètres (ordre non obligatoire) :
	- le titre du site `title: Data For Humanities`,
	- le sous-titre de la catégorie dans `subtitle` (voir le récapitulatif ci-dessous),
	- le nom du menu de gauche (= menu de catégorie) ` menubar`, qui n'apparaîtra pas sinon (cf récapitulatif),
	- le layout à appliquer `layout: page`,
	- la convocation de la table des matières `toc: true`,
	- le titre pour la table des matières (on peut mettre simplement `toc_title: Contenu`).
* L'ajout d'une barre de séparation avant un `## Titre de partie` est conseillé pour la clarté visuelle (ligne vide + `---` + ligne vide).
* Si vous avez des `?`, `:` ou autres caractères nécessitant une espace insécable avant lui, vous pouvez l'exprimer comme entité HTML en collant `&nbsp;` à la place de l'espace.


### Un exemple

Par exemple, pour la page d'information sur les principes FAIR :

* La page est à l'emplacement `/guides/more-about-fair.md`.
* Voici le début du fichier  `/guides/more-about-fair.md` :
```md
---
title: Data For Humanities
subtitle: Les principes FAIR
layout: page
toc: true
menubar: menu_guides
toc_title: Contenu
---


# Les principes FAIR

------------------------------------------

## Projet "FAIR data" en sciences historiques

Les [principes FAIR](https:www.go-fair.org/fair-principles/) ont pour finalité…
```
* Voici l'entrée de la page dans le menu de catégorie `/_data/menu_guides.yml` :
```yml
    - name: Les données FAIR
      link: /guides/more-about-fair
```

## Récapitulatif

| Catégorie | Dossier | Sous-titre d'entête | Paramètre menubar |
| ------- | ---------- | -------- | -------|
| Guides | `/guides` | `subtitle: Les principes FAIR` | `menubar: menu_guides` |
| Projets | `/projects` | `subtitle: Projets` | `menubar: menu_projects` |
| Données SPARQL | `/sparql` | `subtitle: Points d'accès à des données` | `menubar: menu_sparql` |
* Attention à bien respecter la hiérarchie des titres en MarkDown pour que la table des matières soit générée correctement : `# Titre de page`, `## Titre de partie`, `### Titre de sous-partie`, etc. Ne sautez pas (par exemple) de `##` à `####` pour obtenir une mise en forme particulière, ou les `####` n'apparaîtront pas dans la table des matières.

------------

## Installations

Pour travailler en local sur ce site, il faut :

### Installations générales

* Installer [Git](https://git-scm.com/).
* Installer [Jekyll](https://jekyllrb.com/docs/), attention aux dépendances de Jekyll (Ruby, Ruby Gem…).
* Installer la gem webrick avec `gem install webrick` .
* Installer le thème avec `gem install bulma-clean-theme` (cf [documentation](https://www.csrhymes.com/bulma-clean-theme/docs/getting-started/installation/)).

### Pour le dépôt lui-même

* Clôner le dépôt, le dézipper (cf documentation Git).
* Depuis le dossier parent, exécuter `jekyll new nomdudossierclone` pour pouvoir compiler le dossier clône avec Jekyll.
* Rentrer dans le dossier clône avec `cd nomdudossierclone`.
* Exécuter `bundle install` pour installer les dépendances du site.

### Lancer le serveur local

* Exécuter `bundle exec jekyll serve` et attendre que le terminal affiche `Server running... press ctrl-c to stop.` (Ce processus sera refait automatiquement à chaque fois que vous enregistrerez une modification.)
* Aller dans un navigateur et taper `localhost:4000` comme URL.
