# Traitement sur données météo

Disclaimer : Ceci est un projet fictif, la métropole de Toulouse n'a pas mandaté Stack Labs pour un tel projet.

## Objectif

La métropole de Toulouse souhaite disposer d'une application d'analyse de la météo et de la qualité de l'air pour mesurer et appréhender l'impact des actions écologistes qu'elle met en place (Zones Faible Émission, espaces verts, bus électriques, ...). 

Elle vous mandate pour développer un outil qui permet, à partir des stations météo présentes sur le bassin toulousain, de proposer des visualisations de ces données.

La métropole n'a aucune exigence technique car elle n'opérera pas le système elle-même, cela sera vous. Le developpement peut donc s'appuyer sur les technologies Cloud native comme sur des technologies historiques du traitement de données.

La métropole de Toulouse vous met à disposition les données de ses stations météo à travers leur Open Data : https://data.toulouse-metropole.fr/explore/?q=meteo&sort=title&refine.publisher=Toulouse+M%C3%A9tropole

## Attente 

L'idée directrice de cet exercice est de montrer un panel de compétences cohérentes, sa capacité d'apprentissage, le recul sur les paradigmes utilisés. 
Il n'y a pas UNE bonne solution mais DES bonnes solutions. Les spécifications sont volontairement très légères pour laisser de la liberté dans l'exercice. L'essentiel est de faire des hypothèses et d'être capable de défendre les choix de developpement au regard de ces hypothèses.

Le coeur du sujet est autour de la donnée fournie par la métropole (ingestion, stockage, visualisation) mais il est extensible à des problématiques connexes présentées dans les axes optionnels ci-dessous. Une attention particulière sera donc portée sur comment ingérer ces données, comment les stocker et comment les visualiser.

## Axes optionnels

Ces axes ne sont **pas obligatoires** à traiter. Vous pouvez en traiter un comme plusieurs en fonction de votre temps et vos motivations. Ces axes sont là pour pouvoir mettre en avant, si vous le souhaitez, des compétences plus avancées sur le domaine de la Data.

### Live streaming des données jusque dans la visualisation

Les capteurs prennent des mesures à intervalles réguliers et les données fournies par la métropole sont disponibles en streaming. Cet axe propose de se focaliser sur proposer une solution optimale pour faire le streaming de bout en bout de l'application.

### Croiser les données météo avec les données qualité de l'air 

ATMO Occitannie a mis à disposition des données de qualité de l'air sur la région Occitanie. L'idée de cet axe est d'être en mesure d'ingérer une autre source de données et en proposer une intégration jusqu'à la visualisation.

Source de données : https://data-atmo-occitanie.opendata.arcgis.com/

### Enrichissement des données

Tout le pipeline mis en place permet de se poser la question de l'enrichissement de la donnée. En l'état, elle permet d'avoir un suivi dans le temps d'indicateurs proches des stations météo. Il serait intéressant pour la métropole de les enrichir en proposant, sur la base de des données fournies, de la prédiction météo ou de la detection de pics météo (vent violent, grand froid, ...)


### Qualité

Comme vous allez opérer le système en production, il serait intéressant de se poser la question de comment conduire les évolutions futures du produit. Cela amène le développement de "d'artisanat du code" comme les tests de non régression, la chaîne d'intégration continue, le déploiement automatique, ...


## Questions à se poser pour les besoins futurs

* Grenoble voudrait le même produit, quel impact sur mon code ?

* Les capteurs vont bientôt être capables de remonter des données toutes les secondes, quel impact sur la scalabilité de mon code ?

* Toulouse veut désormais plusieurs visualisations en fonction du média de diffusion (écran TV dans le métro, smartphone, ...), quel impact sur mon code ?

## Livrable
* Le code source mis à disposition au travers d'un repository `git` accessible pour les évaluateurs.
* La solution déployée sur un endpoint d'accès (API, site web) ou comment la déployer

Il sera suivi ensuite une code review ensemble pour présenter les choix techniques, leurs avantages/inconvénients sur la base du code livré.
