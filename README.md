#Introduction
  — Corinne : inté senior / Paris-Web / livre BPIW
  — Jérémie : ...
  — Sujet extrèmement serieux : Les mauvaise pratiques de dévelopement web et comment y remédier
  — Mouarf
  — Dévelopement web == n'importe quel développement informatique, il faut organiser et structurer le developement sinon ça devient ingérable et le projet tourne mal.

Site Nicolas (jardinier) : modif urgentes en mode l'arrache.
=> Maintenance


#Documentation
✘✘✘✘✘✘
  - On peut faire sans
  - Analyser le code
  - Demander au dev d'origine / chef de projets / ...

✔✔✔✔✔✔
  - Perte de temps phénoménale
  - Méconnaissance absolue de l'environnement de dev. (NPM, Gulp, etc.)
  - Incertitude quand au périmètre projet (terminal + navigateur)
  - Sans spec, un bogue peut être une feature
  - Syndrome du chauffeur de bus


#Arborescence
✘✘✘✘✘✘
  - Aucune arbo ? Et alors...
  - Pour ce que ça change : tout est à la racine, on s'en sort (y a 10/15 fichiers, pas plus)
  - Avec IDE bien configuré, c'est bon
  - Et puis ils sont bien nommés, tu veux quoi de plus

✔✔✔✔✔✔
  - Bien rangé = repérage facilité = gain de temps permanent (découverte / mise en ligne / export)
  - Départ = peu de fichiers. Puis ajout de données & fichiers. Tri nécessaire (sources vs fichiers générés / fichiers contribués vs fichiers dev)
  - /!\ Fichiers ouverts via l'explorateur pas l'IDE.

  - Pas de règle immuable : groupement par composants ou par types de fichiers
  - Une seule convention pour tout : répertoires, fichiers (CSS, JS et HTML)

=> Cerveau : machine à faire des corrélations. Apprentissage initial et roulez jeunesse 


#Règles de nommage
✘✘✘✘✘✘
  - Formalisme = overkill
  - Analyse rapide du code et basta

✔✔✔✔✔✔
  - Projet français > international (indien / chinois / allemand)
  - JS est sensible à la casse !
  - Nom explicite : long si besoin avec des séparateurs : mixin Ctrl ?
  - Aucune prédictibilité possible = source d'erreurs
  - Si framework : nommenclature prédéfinie ?
  - accent + espace dans une URL, c'est la m...
  

#CSS & Préprocesseur
✘✘✘✘✘✘
  - Je m'y retrouve pas, modif sur le CSS et voilà
  - Je ne connais pas le langage : apprentissage = perte de temps
  - Modif à la fin du fichiers et pis voilà
  - Et si besoin, je mettrais !important

✔✔✔✔✔✔
  - Modif en direct = aucune tracabilité : régression à la clef
  - Zapper les sources = destruction de la logique du build projet et des automatismes
  - Règles à la fin : alourdit le fichier pour rien 
  - Perd le bénéfice de la cascade et on acumule de la dette techique : impossibilité de modifier précisément - nettoyage à venir douloureux.
  - Limite de 4095 règles interprétées par IE.

#Javascript
✘✘✘✘✘✘
  - Le marketing m'a demandé de rajouter une régie de pub et j'ai le sentiment ue ça a un peu foutu la merde.
  - On m'a aussi demandé de rajouter ce plugin de jQuery, mais comme il y avait une incompatibilité j'ai réimporté ma version.
  - Mais bon, ça rame un peu (FF / Chrome). Est-ce que tu voudrais pas voir s'il y a moyen d'optimiser un peu ?
  - Ben oui, en m'a dit qu'en prod on ne devait envoyer qu'un seul et même fichier JS. J'ai suivi la reco.

✔✔✔✔✔✔
  - On importe que ce qui est utile, ni plus, ni moins
  - La multiplicité des imports = bombe à retardement peut faire péter tout un tas de trucs sans signe avant-coureur
  - Oulà, un fichier behaviour de 2Mo. T'arrives pas à l'ouvrir en fichier texte ? Tu m'étonnes
  - Topo sur les outils de débogagge.
  - Comme pour Sass, on suit le process le build. 

=> 26
#HTML
CSS nettoyé, JS vérifié. Reste donc le HTML.
Alors, j'ai vu qu'on utilisais du Canvas, mais par contre je croyais qu'on devait supporter IE8.

✘✘✘✘✘✘
  - Dernière remarque : dès que j'ai des accents, j'ai des caractères cabalistiques genre des carré et des points d'interrogations qui s'affichent.

✔✔✔✔✔✔
  - Fonctionnement iso sur vieux et récents navigateurs (ou pas) ?
  - Comportement clef ou pas ? Si oui : choix technologique pertinent. À l'inverse, comportement triviaux doivent être dégradés élégamment (genre une image en lieu et place de l'anim.)

#Conclusion
- Amélioration progressive : pas tout faire en une fois (pas le temps, ni le budget). On procède par étape au fur et à mesure qu'on met à jour.
- Pareil avec la doc : on peut faire tout faire en une fois.
