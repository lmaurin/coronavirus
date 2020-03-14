# Épidémie, nuage radioactif et distanciation sociale

Le but de ce billet (un peu inhabituel) est d’illustrer de façon simple l’incroyable efficacité potentielle des mesures de distanciation sociale (limiter les rencontres, hygiène, télétravail, fermeture des écoles…) lorsque l’on est face à une épidémie qui vire à la pandémie.

Une épidémie est une réaction en chaîne, et cela change tout sur l’impact potentiel de mesures de ce type, par rapport à d’autres sources de danger.

Pour bien le comprendre, imaginons une autre situation : supposons que l’on ne soit pas face à une épidémie, mais à un danger d’un autre type, disons un nuage radioactif (ou chimique). Du fait de la présence du nuage, imaginons qu’il devienne risqué de sortir, que cela puisse nous rendre malade, voire à terme nous tuer. (Et supposons qu’enfermés  chez soi on ne craigne rien).

Le gouvernement décide de prendre des mesures pour confiner les gens chez eux : fermer certaines écoles, encourager le télétravail, inviter les gens à reporter leurs déplacements, les réunions etc.

Dans ce cas, on peut légitimement imaginer que les vies sauvées seront proportionnées à l’intensité des efforts :

    Si 10% des gens restent chez eux, on évitera 10% des morts;
    Si 50% des gens restent chez eux, on évitera 50% des morts;
    Si 95% des gens restent chez eux, on évitera 95% des morts.

L’effet est linéaire.

Une épidémie, ça n’est pas du tout ça. Une épidémie est une réaction en chaîne, cela implique qu’il y a un effet de seuil sur l’efficacité des mesures, et cet effet de seuil est très fortement non-linéaire.

Même quand on est familier avec les mathématiques associées, il est assez difficile de se représenter cet effet de seuil, alors prenons un exemple concret à partir d’un modèle épidémiologique.

Le modèle que je vais utiliser s’appelle le modèle SIR. C’est un des modèles les plus simples, et l’usage que je vais en faire n’est pas prédictif. Je ne cherche pas à prédire réellement le nombre de morts ou d’infectés : Le modèle est trop simple, les paramètres seront trop imprécis.

Je vais en faire un usage pédagogique, pour illustrer cette notion de seuil, et comment les mesures de distanciation sociales peuvent avoir un effet incroyablement efficace, pas du tout proportionné à l’effort comme dans le cas du nuage radioactif.

Dans ce modèle, on considère que l’on a 3 populations : les sains, les infectés, et les remis (ceux qui ont eu le virus et ont guéri). Et on va modéliser deux phénomènes simples :

    Les gens infectés vont infecter les gens sains.
    Les gens infectés vont progressivement guérir.

Pour cela, on a besoin de 3 paramètres :

    La durée D de la maladie, pendant laquelle on est contagieux.
    Le nombre moyen C de contacts que l’on a chaque jour avec d’autres gens.
    La probabilité P qu’un contact entre un infecté et un sain conduise à une transmission du virus.

Bien souvent, on ne connait pas avec précision ces paramètres, qui d’ailleurs vont dépendre de la définition précise de ce qu’on appelle « un contact ». Mais vous allez voir que ça n’est pas très important.

Prenons un infecté : chaque jour il va croiser C personnes, qu’il contaminera avec une probabilité P. Et cela se produira pendant chacun des D jours que durera sa maladie.

Le nombre total de personne qu’il contaminera sera donc le produit de ces trois termes, que l’on note traditionnellement R0

R_0 = C \times P \times D .

On appelle ce paramètre le taux de reproduction, et même sans faire tourner le modèle mathématique, il n’est pas très compliqué de se convaincre qu’il a une influence déterminante sur le devenir de l’épidémie.

S’il vaut disons 2 : chaque infecté contaminera 2 personnes, qui elles-même contamineront 2 personnes, qui elles-même contamineront 2 personnes etc. On a une réaction en chaîne, le nombre de malades augmente de façon exponentielle, l’épidémie explose.

Maintenant si ce coefficient est inférieur à 1 : chaque infecté refilera la maladie à moins d’une personne, donc le nombre net de malade diminuera et progressivement l’épidémie s’éteindra.

Il y a un effet de seuil monstrueux. Pour éteindre une épidémie de façon « naturelle », il faut que le R0 soit sous le seuil fatidique de 1. Alors combien vaut le R0 dans le cas du Covid-19 ? On n’en sait rien exactement. Probablement entre 2 et 4.

Mais comme vous le voyez, cette valeur n’est pas intrinsèque à la maladie, elle dépend de facteurs comportementaux : combien de contacts quotidiens, quelle probabilité qu’une transmission ait lieu.

En adoptant des mesures de distanciation sociale (moins de contacts, se tenir plus loin, hygiène, suppressions des rassemblements et réunions inutiles, fermeture des établissements scolaires, télétravail, etc.), on peut très facilement faire baisser le R0.

Et le point clé ici, est que le bénéfice ne sera pas du tout proportionné à l’effort. Si on en fait suffisamment pour passer rapidement sous le seuil, c’est gagné.

Imaginons que le R0 soit initialement de 2,5. C’est une hypothèse raisonnable pour le Covid-19. Si on arrive à le diviser par 4 on bloque très très vite la propagation de l’épidémie.

Diviser le R0 par 4 est loin d’être inaccessible : cela peut vouloir dire par exemple avoir 2 fois moins de contacts, et faire en sorte que la probabilité de transmission soit divisée par 2 (par une distance plus importante et une attention particulière à l’hygiène.)

Pour bien illustrer ce point, je me suis amusé à mettre un modèle de type SIR dans Excel (TELECHARGEABLE ICI, sinon voir la fin du billet) , en prenant comme point de départ la situation approximative en France au 11/03/2020.

Encore une fois, le but n’est pas de faire de la prédiction, c’est que vous puissiez voir par vous-même, par l’expérimentation « numérique », que cet effet de seuil du R0 est monstrueux. Ceci est donc un « modèle-jouet ».

Prenons un R0 de 2,5. On peut l’obtenir en disant que la maladie dure 10 jours, et que chaque jour on a 50 contacts avec une probabilité de transmission de 0,5%. Ces deux derniers chiffres ne sont pas important, c’est le produit des deux qui compte.

Le graphique ci-dessous représente le nombre cumulé de cas en fonction du temps (en jours à partir d’aujourd’hui) en France, si on reste à un R0 de 2,5. (Ca n’est pas une prédiction, c’est un « modèle-jouet » !)

On voit qu’en 6 mois, quasi tout le monde aura chopé la maladie. Avec un taux de mortalité de 3%, on est quasi 2 millions de morts (Ca n’est pas une prédiction, c’est un « modèle-jouet » !)

Maintenant imaginons que l’on arrive tout de suite maintenant à diviser par 4 le R0 : deux fois moins de contacts, et des contacts plus distants qui divisent par 2 la probabilité de transmission. Ca parait pas inatteignable, non ? Le R0 sera alors de 0,62. Et voici le résultat

On plafonne à 6000 cas cumulés, et donc 180 morts avec un taux de mortalité de 3% (Ca n’est pas une prédiction, c’est un « modèle-jouet » !)

Une différence monstrueuse, énorme. Totalement disproportionnée par rapport au changement initial qu’on a fait (des « simples » divisions par 2 des contacts et des transmissions).

Une épidémie est une réaction en chaîne. Les mesures de distanciation sociale peuvent avoir un effet totalement disproportionné. C’est très très très différent du cas du nuage radioactif, où les mesures de confinement auraient un effet essentiellement linéaire.

Et c’est évidemment lié au fait que dans le cas du nuage, en faisant attention on ne protège que soi. Ici on protège tout le monde.

C’est tout ce que je voulais illustrer. Prenez le modèle Excel, jouez avec. Ca n’est qu’un modèle, le plus simple de tous en épidémiologie. Il n’a AUCUNE valeur prédictive sur les détails des chiffres. Il est là pour illustrer le principe de réaction en chaîne, qui est au coeur de la notion d’épidémie. Les détails du modèle ne sont pas important, cet effet de réaction en chaine existe dans tous les modèles.

Faire baisser rapidement le R0 est très accessible, sans forcément tomber dans une situation de « pays mort » ou de « loi martiale ». Je pense que fermer les écoles et les établissement d’enseignement pourrait créer le signal nécessaire pour que tout le monde y mette du sien. Et en quelques semaines ce serait plié.

Téléchargez le modèle-jouet. Jouez avec. Voyez par vous même.

Edit du 13/03/2020 : Pas mal de gens ont fait des petites applis qui illustrent le modèle de façon interactive :

https://jflorian.shinyapps.io/SIRmodel/

https://sciencetonnante-epidemie.netlify.com

https://epidemic.phoenix-it-services.com
