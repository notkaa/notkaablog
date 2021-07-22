+++
author = "Rv"
categories = ["code"]
date = 2020-05-22
description = "comment faire de la photo argentique maintenant"
draft = false
image = ""
slug = "photographie"
tags = ["polaris", "code", "auto hébergement", "musique"]
title ="Installer polaris dans conteneur LXC sur Qnap"

+++

À la recherche d'un player web pour une collection de musique pour un projet personnel, je suis tombé sur [Polaris](https://github.com/agersant/polaris). Il existe une version QPKG mais celle-ci n'est pas à jour et les dernières mises à jour sont importantes pour moi. Je me suis donc mis en tête de le faire tourner dans un contenaire Ubuntu LXC. En voici les étapes :

- Dans containerStation, chercher Ubuntu LXC

![contairerstation](/images/2020/11/polaris/01ubuntuLXC.jpg)

- Le configurer comme ceci :

![conf contairerstation](/images/2020/11/polaris/02containerconf1.jpg)

Sans oublier le montage des répertoires partagés

![répertoire contairerstation](/images/2020/11/polaris/03containerconf2.jpg)




