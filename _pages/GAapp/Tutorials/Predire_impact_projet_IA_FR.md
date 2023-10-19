---
permalink: /GAapp/Tutorials/predire_impact_projet_IA_FR/

title: "[FR] Utiliser le calculateur Green Algorithms pour prédire l'empreinte carbone d'un project IA"

sidebar:
  nav: GAapp

toc: true
---

Ce tutoriel, encore en construction, est un exemple d'utilisation du calculateur
Green Algorithms pour prédire l'impact environmental d'un projet d'IA _avant_ le début
du projet.

# 1. Définir les différentes étapes du projet

Un projet d'IA peut par exemple inclure une phase de recherche et développement,
où différentes approches sont testées. Suivie d'une ou plusieurs phases d'apprentissage
du ou des modèles finaux et une phase d'inférence, où le modèle retenu fait
des prédictions sur de nouvelles données.

# 2. Pour chaque étape

## 2.1. Faire un inventaire des resources utilisées

En premier les resources physiques:
- Quelles infrastructures vont être utilisées? Ordinateur personel, data centre local, cloud etc.
- Dans le cas des data centres, se renseigner sur le PUE (_Power Usage Effectiveness_, mesurant l'efficacité énergétique du bâtiment).
- La location géographique des équipements.
- Quels processeurs vont être utilisés? CPU et/ou GPU, combien et quels modèles.
- Une estimation de la mémoire vive nécessaire.

Et les temps de calcul (estimés bien sûr). Ceci peuvent être basés sur les modèles
existant auparavent par exemple.

Il est parfois difficile de faire ces estimations pour le temps de calcul et
la mémoire nécessaire. __Des estimations approximatives sont tout à fait
acceptables__ (e.g. 200 heures avec 3 GPUs et 24 GB de mémoire vive).
{: .notice--info}

Quelques indication pour les infrastructures:
- Dans le cas d'ordinateur personel, les modèles de processeurs seront facile à obtenir.
- Dans le cas de data centre, les informations de processeur, location géographique et PUE devraient être disponible sur leur site internet, ou en contactant l'équipe de support technique. Si ce n'est pas le cas, une valeure moyenne de PUE peut être utilisée dans le calculateur.

## 2.2. Utiliser le calculateur pour estimer l'empreinte carbone

# FAQ

> Que faire si le modèle de CPU/GPU n'est pas dans la liste
