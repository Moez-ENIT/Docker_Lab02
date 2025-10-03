# Lab 02- Docker

# Applications Web

Dans cet atelier, vous allez déployer un serveur web et mettre en œuvre la technique de load-balancing pour améliorer le temps de réponse. Par la suite vous allez composer plusieurs conteneurs pour mettre en place une application dotée d'une architecture complexe.

---

**Concepts :**

* Dockerfile  
* Load-balancer  
* Volume  
* Docker compose

---

<span style="color:red">
Pour chaque exercice travailler dans le repertoire qui lui correspond.
Mettre les commandes et les reponses dans les fichiers `Readme`.
Le code doit figurer dans le repertoire qui correspond à l'exercice en question.

</span>

---
## Exécuter votre premier serveur web

   1.  Créer une page web qui affiche la date d'aujourd'hui dans le format suivant  (en Francais):

        > Bonjour, aujourd'hui c'est le Lundi 9 Octobre 2023

   2.  Exécuter un conteneur Docker contenant le serveur web Apache qui utilise la page web que vous venez de créer comme page index.

   3.  Créer une image Docker nommée "web-server\_lab"  à  l'aide d'un fichier Dockerfile.

   4.  En utilisant le fichier Dockerfile exécuter votre serveur Web en mode daemon.

   5.  Arrêter le serveur web

   6.  Démarrer le serveur web de nouveau

## Performances du serveur Web

   1.  Utiliser Apache HTTP server benchmarking tool pour tester les performances de votre serveur Web.

   2.  Utilisez setTimeout() pour retarder l'affichage du message de 3 secondes.

   3.  Testez les performances de nouveau. Qu'est ce qui a changé?

   4.  Créer une image Docker nommée "benchmarker"  à l'aide d'un fichier Dockerfile.

   5.  Testez les performances de votre serveur Web en utilisant l'image Docker nommée "benchmarker".

        
      

## Load balancing

   1.  En utilisant le fichier Dockerfile exécuter 2 instances  de votre serveur Web en mode daemon.

   2.  Créez un volume et utilisez le pour partager la page web entre les deux instances du serveur web.

   3.  Utilisez une image NGINX pour implémenter une solution de load-balancing.

   4.  Testez les performances de nouveau. Qu'est ce qui a changé?

   5.  Créer un fichier docker-compose.yml permettant de répliquer votre architecture actuelle (4 conteneurs: 2 instances du serveur web, une instance NGINX et une instance  "benchmarker"). Testez votre solution.

## Back-end

   1.  Créez un service web (avec le language Python) qui renvoie la date d'aujourd'hui dans le format suivant  (en Francais):

      > Lundi 9 Octobre 2023

   2.  Exécuter un conteneur Docker contenant votre service web. Testez.

   3.  Modifiez votre page web afin de consommer le service web offert par le conteneur Docker.

   4.  Mettez à jour votre fichier docker-compose.yml afin d'inclure le service web.

   5.  Testez les performances de nouveau. Qu'est ce qui a changé?

