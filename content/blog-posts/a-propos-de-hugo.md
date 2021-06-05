+++
author = "Philippe Sthely"
date = 2021-06-04T22:00:00Z
hero = "/images/what-is-hugo.png"
title = "Générateurs de sites statiques et CDN"
type = "blog"

+++
Les générateurs de sites statiques sont des outils qui génèrent des sites web entièrement statiques, c'est à dire prêt à afficher dans un navigateur. Le site est pré-construit en amont à partir des données de contenu et de configuration qu'on lui a donné, et servi directement sans traitement supplémentaire lorsqu'un client fait une requête.

Les architectures client-serveur traditionnelles fonctionnent en flux tendu entre les requêtes client et les traitements serveur. A chaque requête client, le serveur effectue un traitement spécifique pour servir la page demandée. Avec beaucoup de requêtes simultanées, le serveur peut être surchargé et peut même planter. Il y a donc un aspect de scaling, de mise à l'échelle à prendre en compte dans ce cas. Ça peut devenir un vrai casse-tête.

De plus, la centralisation des données sur un même serveur n'est pas ce qu'il y a de plus sécurisant et résiliant. On l'a vu récemment avec les incendies des datacentres OVH qui ont mis à mal quelques applications. Malheureusement, cette architecture monolithique est encore nécessaire dans beaucoup de projets qui n'ont pas d'autres alternatives.

Mais dans le domaine des sites web, il existe énormément de projets qui n'ont tout simplement pas besoin de traitements des données en flux tendu.

Et là, les sites statiques tirent leur épingle du jeu de façon brillante :

* déploiement continu simplifié grâce à des services de CDN comme Netlify ou GitHub
* administration des serveurs délégué au service de CDN (sécurité, décentralisation, résilience)
* traitement des données en amont, réponses quasi instantanées aux requêtes client

Un service de CDN comme Netlify propose une importante liste de services concernant l'administration de la logique de déploiement des sites statiques en ce qui concerne les tests, les gestions de versions, les DNS, la configuration des builds, etc. Tout cela de façon sécurisée et user-friendly.

Plus concrètement, j'utilise GitHub comme dépôt de code source, Hugo pour générer la sortie statique des sites web, Forestry comme CMS et Netlify comme CDN. Le tout en ligne de commande ou avec des scripts Shell pour automatiser certaines tâches... C'est presque magique.

Voici quelques liens intéressants :

* Jamstatic - Netlify en 10 fonctionnalités [https://jamstatic.fr/2018/01/07/netlify-en-10-fonctionnalites/](https://jamstatic.fr/2018/01/07/netlify-en-10-fonctionnalites/ "https://jamstatic.fr/2018/01/07/netlify-en-10-fonctionnalites/")
* Netlify - Modern Web Development on the Jamstack [https://www.netlify.com/oreilly-jamstack/](https://www.netlify.com/oreilly-jamstack/ "https://www.netlify.com/oreilly-jamstack/")
* GitHub - Hugo [https://github.com/gohugoio/hugo](https://github.com/gohugoio/hugo "https://github.com/gohugoio/hugo")
* GitHub - Forestry [https://github.com/forestryio/forestry.io](https://github.com/forestryio/forestry.io "https://github.com/forestryio/forestry.io")