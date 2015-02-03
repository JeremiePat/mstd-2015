#Introduction
— (C) Bonjour, je suis Corinne
— (J) Et je suis Jérémie
— (C) On va vous parler d'un sujet extrèmement serieux : Les mauvaise pratiques de dévelopement web et comment y remédier
— (J) Oui, ok, mais enfin bon, sérieux... ça va quoi
— (C) Ah ben si, le developement web c'est comme n'importe quel développement informatique, il faut organiser et structurer le developement sinon ça devient ingérable et le projet tourne mal.
=> D'ailleurs à ce propos, on nous a demandé de faire des modifs sur le site de Nicolas le Jardinier. Ca te dise qu'on y jette un oeil ensemble ?


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
1) À quoi ça sert
2) Bon, OK, c'est important mais comment on fait ?
✘✘✘✘✘✘
  - Aucune arbo ? Et alors...
  - Pour ce que ça change : tout est à la racine, on s'en sort (y a 10/15 fichiers, pas plus)
  - Avec IDE bien configuré, c'est bon
  - Et puis ils sont bien nommés, tu veux quoi de plus

✔✔✔✔✔✔
  - Bien rangé = plus facile de s'y retrouver = gain de temps permanent (découverte / mise en ligne / export)
  - Au départ : peu de fichiers, au fur et à mesure, ça va grandir, on va fractionner, ranger, faire le tri entre sources et fichiers générés
  - /!\ Sur le web, fichiers textes donc ouverts via l'explorateurs, pas forcément via ton IDE.
  - Pas de règle immuable : groupement par composants ou par types de fichiers
  - Une seule convention pour tout : répertoires, fichiers (CSS, JS et HTML)

=> Cerveau : machine à faire des corrélations. Si tu utilises une seule et même convention, on apprend la convention 1 fois et après, intuitivement comment ça marche. Ca accomagne l'effort de documentation : on la liste / s'en rapeelle une fois et après roulez jeunesse 


#Règles de nommage
✘✘✘✘✘✘
  - Formalisme = overkill
  - Analyse rapide du code et basta

✔✔✔✔✔✔
  - Projet français > international (indien / chinois / allemand)
  - Et une fois que tu as utilisé les lettres les plus communes, tu fais quoi, tu passes en revue tout l'alphabet ? Un mixin Ctrl, j'ai aucune idée de ce qu'il fait.
  - Aucune prédictibilité possible = source d'erreurs
  - Si framework, vérifier s'il y a une nommenclature prédéfinie
  - accent + espace dans une URL, c'est la m...
  

#CSS & Préprocesseur
✘✘✘✘✘✘
  - Je m'y retrouve pas, modif sur le CSS et voilà
  - Je ne connais pas le langage : apprentissage = perte de temps
  - Modif à la fin du fichiers et pis voilà
  - Et si besoin, je mettrais !important

✔✔✔✔✔✔
  - Modif en direct = aucune tracabilité, impossibilité de revenir en arrière car régression à la clef
  - Zapper les sources = destruction de toute la logique et du build projet (et avantage des automatisme déjà mis en place)
  - Alourdit le fichier pour rien : on va certainement se trimballer des règles devenues inutiles
  - Perd le bénéfice de la cascade et c'est une plaie à surcharger derrière
=> Course à l'armement : on acumule de la dette techique qui va être monstrueuse à nettoyer le jour ou on en aura besoin. Il va être impossible de faire une frappe chirurgicale pour modifier quoi que ce soit.
(Attention à la limite du nombre de sélecteurs que IE accepte 4096 sélecteurs)

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
