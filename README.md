#Introduction
- Récupération d'un projet conçu par une autre agence.
- Demande de mise à jour et d'évolutions "pour hier" faites à l'arrache.
- Et maintenant mise au propre du code en vue de la maintenance.


#Documentation
##Cons
- OSEF : On peut faire sans
- Il suffit d'analyser le code
- Au pire, demander à l'équipe d'origine : dev, chef de projets, responsable tehnique

##Pros
- Perte de temps phénoménale pour chercher l'info
- Méconnaissance absolue de l'environnement de dev et du process de build
- Incertitudes quand au périmètre projet (couple terminal/navigateur)
- Sans spec, un bogue peut être une feature
- Syndrome du chauffeur de bus


#Arborescence
##Cons
- Aucune arbo ? Et alors...
- Tout est à la racine, on s'en sort très bien (y a 10/15 fichiers, pas plus)
- Avec un IDE bien configuré, tout va pour le mieux dans le meilleur des mondes

##Pros
- Au départ, peu de fichiers. Après, c'est la jungle (fichiers contribués, fichiers sources, fichiers générés, fichiers minifiés)
- Rangement logique = repérage facilité = gain de temps permanent
- Pas de règle immuable : groupement par composant ou par type de fichiers
- L'idéal : utiliser une seule convention pour tous les noms (répertoires, fichiers, fonctions, variables, classes et identifiants)

Le cerveau est une machine à faire des corrélation. 
Profitons-en !


#Règles de nommage
##Cons
- Formalisme = overkill
- Analyse rapide du code et basta

##Pros
- Langue : français pour projet et équipe francophone, ok. Pour le reste, anglais (intervenants étrangers potentiels)
- /!\ aux majuscule : HTML & JS sont sensibles à la casse ! 
- Préférer les noms explicites et descriptif (que fait le mixin Ctrl ?)
- Aucune prédictibilité possible = source d'erreurs
- Framework = nommenclature prédéfinie : capitaliser dessus pour être raccord
- /!\ aux accents & espaces : dans une URL, c'est des problèmes assurés.
  

#CSS & Préprocesseur
##Cons
  - Je m'y retrouve pas, modif sur le CSS et voilà
  - Je ne connais pas le langage : apprentissage = perte de temps
  - Modif à la fin du fichiers et pis voilà
  - Et si besoin, je mettrais !important

##Pros
  - Modif en direct = aucune tracabilité : régression à la clef
  - Zapper les sources = destruction de la logique du build projet et des automatismes
  - Règles à la fin : alourdit le fichier pour rien 
  - Perd le bénéfice de la cascade et on acumule de la dette techique : impossibilité de modifier précisément - nettoyage à venir douloureux.
  - Limite de 4095 règles interprétées par IE.

#Javascript
##Cons
  - Le marketing m'a demandé de rajouter une régie de pub et j'ai le sentiment ue ça a un peu foutu la merde.
  - On m'a aussi demandé de rajouter ce plugin de jQuery, mais comme il y avait une incompatibilité j'ai réimporté ma version.
  - Mais bon, ça rame un peu (FF / Chrome). Est-ce que tu voudrais pas voir s'il y a moyen d'optimiser un peu ?
  - Ben oui, en m'a dit qu'en prod on ne devait envoyer qu'un seul et même fichier JS. J'ai suivi la reco.

##Pros
  - On importe que ce qui est utile, ni plus, ni moins
  - La multiplicité des imports = bombe à retardement peut faire péter tout un tas de trucs sans signe avant-coureur
  - Oulà, un fichier behaviour de 2Mo. T'arrives pas à l'ouvrir en fichier texte ? Tu m'étonnes
  - Topo sur les outils de débogagge.
  - Comme pour Sass, on suit le process le build. 

#HTML

- CSS nettoyé, JS vérifié. Reste donc le HTML.
- Canvas mais support IE 8 ?

##Cons
  - Dernière remarque : dès que j'ai des accents, j'ai des caractères cabalistiques genre des carré et des points d'interrogations qui s'affichent.

##Pros
  - Fonctionnement iso sur vieux et récents navigateurs (ou pas) ?
  - Comportement clef ou pas ? Si oui : choix technologique pertinent. À l'inverse, comportement triviaux doivent être dégradés élégamment (genre une image en lieu et place de l'anim.)

#Conclusion
- Amélioration progressive : pas tout faire en une fois (pas le temps, ni le budget). On procède par étape au fur et à mesure qu'on met à jour.
- Pareil avec la doc : on peut faire tout faire en une fois.
