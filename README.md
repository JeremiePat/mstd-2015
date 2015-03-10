_La présentation prend la forme d'un dialogue entre 2 développeurs._

#Introduction
- Récupération d'un projet conçu par une autre agence.
- Demande de mise à jour et d'évolutions "pour hier" faites à l'arrache.
- Et maintenant mise au propre du code en vue de la maintenance.


#Documentation
##Dev 1
- OSEF : On peut faire sans
- Il suffit d'analyser le code
- Au pire, demander à l'équipe d'origine : dev, chef de projets, responsable tehnique

##Dev 2
- Perte de temps phénoménale pour chercher l'info
- Méconnaissance absolue de l'environnement de dev et du process de build
- Incertitudes quand au périmètre projet (couple terminal/navigateur)
- Sans spec, un bogue peut être une feature
- Syndrome du chauffeur de bus


#Arborescence
##Dev 1
- Aucune arbo ? Et alors...
- Tout est à la racine, on s'en sort très bien (y a 10/15 fichiers, pas plus)
- Avec un IDE bien configuré, tout va pour le mieux dans le meilleur des mondes

##Dev 2
- Au départ, peu de fichiers. Après, c'est la jungle (fichiers contribués, fichiers sources, fichiers générés, fichiers minifiés)
- Rangement logique = repérage facilité = gain de temps permanent
- Pas de règle immuable : groupement par composant ou par type de fichiers
- L'idéal : utiliser une seule convention pour tous les noms (répertoires, fichiers, fonctions, variables, classes et identifiants)

Le cerveau est une machine à faire des corrélation.   
Profitons-en !


#Règles de nommage
##Dev 1
- Formalisme = overkill
- Analyse rapide du code et basta

##Dev 2
- Langue : français pour projet et équipe francophone, ok.   
Pour le reste, anglais (intervenants étrangers potentiels)
- /!\ aux majuscule : HTML & JS sont sensibles à la casse ! 
- Préférer les noms explicites et descriptifs (que fait le mixin Ctrl ?)
- Aucune prédictibilité possible = source d'erreurs
- Framework = nommenclature prédéfinie : capitaliser dessus pour être raccord
- /!\ aux accents & espaces : dans une URL, c'est des problèmes assurés.


#CSS & Préprocesseur
##Dev 1
- Impossible de s'y retrouver dans les fichiers (extension .scss kesako ?).
- Fichier de prod minifié récupéré et mis à jour directement.
- Surcharges en fin de fichier avec des `!important` lorsque nécessaire.

##Dev 2
- Modif du fichier de prod en direct = régressions inévitables car fichiers sources devenus obsolètes.
- Sources non mises à jour = destruction du build projet : gestion automatisée (concaténation, minification, optimisation, etc.) impossible.
- Surcharge des règles en fin de fichier = plomber les perfs pour rien.   
/!\ Limite de 4095 règles interprétées par IE.   
=> Modifier les déclarations responsables du style incriminé directement.
- Utilisation de `!important` = impossibilité de surcharger simplement.   
=> Accumulation de dette techique (nettoyage futur douloureux).


#Javascript
##Dev 1
- Ajout régie pub en mode « La Rache » = ça semble boguer maintenant.
- Import d'une nouvelle version de jQuery pour faire fonctionner le pugin XYZ exigé par le client (version actuelle incompatible).
- Ça rame méchamment : les perfs sont mauvaises.

##Dev 2
- /!\ Scripts tiers : RTFM !   
=> Se renseigner sur mise en place, périmètre d'action et effets de bord possibles.
- Imports multiples (jQuery, Dojo, etc.) = bombe à retardement. Source d'erreurs difficiles à identifier car imprévisibles.
- Séparer le code en plusieurs petits fichiers JS (concaténés en prod) : plus simples à comprendre et à déboguer.


#HTML
##Dev 1
- Canvas mais support IE 8 ?
- Carrés et points d'interrogations à la place des accents

##Dev 2
- Fonctionnement identique attendu sur tous les couples terminaux/navigateurs ?
- Comportement clef ou pas ?   
=> Oui : Opter pour un choix technologique pertinent : Canvas = pas solution appropriée.   
=> Non : Opter pour de la dégradation élégante : Mettre une image en lieu et place de l'animation.


#Conclusion
- Tout faire en une fois = illusion (demande un certain temps/budget)
- Procéder étape par étape.   
=> Faire évoluer le code au coup par coup lorsqu'on intervient dessus.   
=> Documenter le code lors de sa mise à jour : documentation à posteriori plus compliquée.
