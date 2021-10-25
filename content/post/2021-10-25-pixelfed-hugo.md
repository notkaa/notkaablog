+++
author = "notkaa"
categories = []
date = 2021-10-25T22:00:00Z
tags = ["hugo"]
title = "Insérer une image Pixelfed dans un post Hugo"
draft = false
+++

Petit billet penses bête, mes photos sont hébergées et partagées sur Pixelfed (faites le vous aussi, abandonnez Instagram). 
Le code iFrame est formaté comme ceci :
```php
<iframe src="https://pixelfed.social/p/Notkaa/xxxxxxxxxxx/embed?caption=true&likes=false&layout=full" class="pixelfed__embed" style="max-width: 100%; border: 0" width="400" allowfullscreen="allowfullscreen"></iframe><script async defer src="https://pixelfed.social/embed.js"></script>
```
Pour embraquer une photo Pixelfed, il faut placer un de ces shortcodes que j'ai créé pour l'occasion dans le répertoire :  

/themes/lethemeutilisé/layouts/shortcodes

{{< gist notkaa 43adda6ea60a3b7c54aa3879242b7723 >}}

{{< gist notkaa 758df36da570d970d3b5079e833c5f2f >}}

Puis dans le post l'appeler avec un :  
{{< pixelfed id="xxxxxxxxxxx" >}}
