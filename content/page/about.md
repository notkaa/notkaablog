---
title: qui ?
subtitle: qui et comment ?
comments: false
---

## qui ?  
Mon nom est Hervé, mais vous pouvez me trouver le plus souvent sur différentes plateformes ou communautés sous le nom de Notkaa. Voici en quelques mots qui je suis :  

* Je fais des photos et des projections vidéos
* Je suis un coureur et plus précisément un marathonien
* Je collectionne les vinyles

Si tout cela vous intéresse alors je suis heureux de partager ces quelques pages rédigées de manières non régulières avec vous.  

## Comment ?  
Le concept d'un site statique pour un blog me parait tout à fait pertinent, d'autant que je ne souhaite pas me perdre dans un formatage compliqué. Ce site est là pour m'amuser, apprendre des choses en le fabriquant et publier deux, trois billets de temps en temps. J'ai donc choisi [Hugo](https://gohugo.io) pour le créer. Par contre je souhaitais aussi pouvoir publier des billets depuis mon iPad. Et premier problème, pour qu'Hugo construise les pages avant de le publier, il faut qu'il tourne sur un ordinateur. En effet il doit compiler les pages. En creusant un peu, je tombe sur la solution [Netlify](https://www.netlify.com) et [Forestry](https://app.forestry.io). En gros, on héberge sur Git, Netlify se charge de faire la compilation à chaque commit et on peu accèder par Forestly pour écrire ses billets. Si vous voulez en savoir plus voici [la méthode](https://healthinnovation.github.io). Ça fonctionne mais ce n'est pas très fluide. Forestly est assez pénible on pert la souplesse d'un site statique.  
Finalement je tombe sur [ce billet](https://hugo.md/post/moving-to-cloudflare-pages/) au hasard de mes recherches. Et là je trouve la solution parfaite pour moi :  
* Hébergement du site sur Github
* Utilisation de [Cloudflare pages](https://developers.cloudflare.com/pages/] pour générer les pages de mon site via Hugo
* DNS de mon nom de domaine géré par Cloudflare.

    Attention il y a une petite subtilité :
    
    Dans les DNS :  
    il faut déclarer un CNAME pointant www vers nomdusite.pages.dev
    
    Dans Rules :   
    il faut créer une règle redirigeant https://nomdusite.xxx/* vers https://wwww.nomdusite/$1 (Status Code: 301 - Permanent Redirect)

* Rédaction directement dans Github sur le web
* Management des fichiers via [Github dev](https://github.dev/) qui ouvre le dépôt en mode Visual Studio Code. Pour cela c'est très simple, il suffit de remplacer le github**.com** par github**.dev** en naviguant sur votre dépôt.

Voilà j'ai exactement ce que je veux, je peux rédiger depuis n'importe quelle machine. Et si elle n'est pas connectée c'est pas grave, je n'ai qu'à uploader le texte rédigé dans n'importe quel éditeur. Il ne me reste plus qu'à me plonger dans la rédaction des shortcodes pour pouvoir mettre mes photos issues de mon Pixelfed et tout sera parfait.  
Quand je vous dis que j'aime apprendre...
