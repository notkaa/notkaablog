+++
author = "notkaa"
date = 2021-10-25T22:00:00Z
tags = ["hugo"]
title = "Insérer une image Pixelfed dans un post Hugo"
draft = false
+++

Petit billet penses bête, mes photos sont hébergées et partagées sur Pixelfed (faites le vous aussi, abandonnez Instagram). 
Le code iFrame est formaté comme ceci :

{{< gist notkaa 399c386a3708168f9176859cc32588e0 >}}

Pour intégrer une photo Pixelfed dans un post, il faut placer un de ces shortcodes que j'ai créé pour l'occasion dans le répertoire :  

/themes/lethemeutilisé/layouts/shortcodes

{{< gist notkaa 43adda6ea60a3b7c54aa3879242b7723 >}}

{{< gist notkaa 758df36da570d970d3b5079e833c5f2f >}}

Il faut aussi rajouter ces lignes dans config.toml

[markup.goldmark.renderer]  
unsafe = true


