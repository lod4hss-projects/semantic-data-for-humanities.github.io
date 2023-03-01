---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

title: Data For Humanities
subtitle: Projets aboutis
menubar: menu_projects
toc: true
layout: page
---

# Prosopographie des Chanoines réguliers de Notre-Sauveur (XVIIe-XVIIIe siècles)

------------------------------------------

## Présentation

> Ce chantier est créé exclusivement à titre d’exercice pour participer l’atelier Fairdata du PHN.

Les fichiers utilisés ont été créés par Cédric Andriot dans le cadre de sa thèse : _Les Chanoines réguliers de Notre-Sauveur_, Paris, 2012. Ces fichiers m’avaient été confiés par l’auteur après qu’il eut renoncé à verser ses données dans la BHP du projet symogih.org, sa recherche étant achevée.

Les fichiers donnent des états de la congrégation  à des dates différentes, par maison, ainsi que des listes de professions. Les renseignements concernent les noms et prénoms, le lieu de naissance avec parfois la profession du père, la date et la maison de profession, parfois les emplois dans la congrégation, les effectifs nominatifs des établissements à des dates différentes, la date de décès.

L'objectif n'est pas de refaire le travail de C. Andriot mais d'utiliser ces données comme test pour l'alignement en se formant à l'utilisation d'OntoMe.

------------------------------------------

## Emplacement des données

Les premiers tableaux au format csv sont disponibles ici :
* [enseignants_college_aoste_2.xls.zip](https://phn-wiki.ish-lyon.cnrs.fr/lib/exe/fetch.php?media=fairdata:enseignants_college_aoste_2.xls.zip)
* [professions1780-1785.xls.zip](https://phn-wiki.ish-lyon.cnrs.fr/lib/exe/fetch.php?media=fairdata:professions1780-1785.xls.zip)
* [hommes1790parmaisons_cures.xls.zip](https://phn-wiki.ish-lyon.cnrs.fr/lib/exe/fetch.php?media=fairdata:hommes1790parmaisons_cures.xls.zip)

------------------------------------------

## Analyse du fichier : professions 1780-1785
Source : AD Vosges 2 I 1, Registre des professions  l'abbaye d'Autrey 1780-1785. Cette abbaye sert alors de noviciat à la congrégation des chanoines réguliers de Notre-Sauveur.\\ Les noms des colonnes sont les suivants : Année profession, Année vêture, Nom, Prénom, Lieu naissance, Diocèse (du lieu de naisP27 is participation in P27 is participation in sance), Date naissance, Profession du père, lieu d'exercice de la profession du père.

Selon l'ontologie symogih, ce tableau se décompose ainsi :
* les objets : Actr, CoAc, NaPl (type : lieu habité), NaPl (type : territoire ; classe : division ecclésiastique), SoCh.
* les types d'information : TyIn7 Exercice de la fonction, TyIn13 Union, TyIn14 Naissance, TyIn76 Vêture, TyIn82 Profession religieuse

### Alignement symogih/CIDOC CRM

| Symogih | CIDOC CRM | Alignement |
| -------- | --------- | 	--------- |
| Actr    | E21 Person  | HuBe Human Being |
| CoAc    | E74 Group  |StrCoAc Structured Collectivity |
| NaPl (lieu habité)   | C8 Geographical Place  | InPl Inhabited Place        |
| NaPl (territoire)    | C8 Geographical Place    | Terr Territory  |
| SoCh    | E1 CRM Entity     | C14 Social Character  |
| TyIn7 Exercice de la fonction    | E7 Activity     | TyIn7 Exercice d'une fonction  |
| TyIn13 Union    | C31 Union     | C31 Union |
| TyIn14 Naissance    | E67 Birth     |E67 Birth  |
| TyIn76 Vêture    | E5 Event | ?  |
| TyIn82 Profession religieuse    | E5 Event     | ?  |

### Alignement rôles/properties : TyIn7 exercice de la fonction

| Rôles Symogih | Properties CIDOC CRM |
| -------- | --------- |
| TyRo8 Localiser  | P7 took place at  |
| TyRo12  Exercer  | P35 has social character  |
| TyRo16 Être l'origine   |P2 was initiated by | 
| TyRo21 Être concerné    |P34 pertains to | 
| TyRo47 Être exercé    |P14 carried out by |
| TyRo176 Occasionner la fin    |P3 was terminated by|


