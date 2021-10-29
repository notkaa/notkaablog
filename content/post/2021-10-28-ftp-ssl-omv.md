+++
author = "notkaa"
categories = []
date = 2021-10-28T22:00:00Z
tags = ["notes"]
title = "FTPS dans OpenMediaVault"
+++

Je pose cette petite note ici, car cette configuration m'a donné du fil à retordre.
Voici les différents points sensibles à vérifier sur la configuration :

 - Récupérer le certificat ssl chez Cloudflare (il a l'avantage d'être valide 15 ans)
 - Coller les clés dans Système/Certificats/SSL
 - Ouvrir une plage de ports passifs (49152-65534) sur l'interface et sur la box
 - Mettre l'ip publique dans ***Adresse Mascarade***
 - Mettre : *TLSOptions NoSessionReuseRequired* dans ***Options supplémentaires***

Et voilà !
