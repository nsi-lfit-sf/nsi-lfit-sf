# OSMNx 

### Présentation

OSMnx est un package utilisé en Python permettant de récupérer, de modéiser, d'analyser et visualiser les données des réseaux routiers tout en prenant l'information de la carte à partir d'OpenStreetMap. Il a été développé par Geoff Boeing, directeur du laboratoire des données urbaines (Urban Data Lab) à l'université de Californie du Sud. 

※ Réseau routier : ensemble de voies de  circulation terrestre, transport des véhivules routiers, surtout les véhicules motorisés (voiture, motos...)

※Package : ensemble de fonction dont sont regroupés les modules 

>  ### OpenStreetMap: 
L'OpenStreetMap est un projet collaboratif de cartographie en ligne, mis en route par Steve Coast à l'University College de Londres en 2004, qui vise à constituer une base de données géographiques libre du monde, en utilisant le système GPS et d'autres données libres.

### Fonctionnement

Une fois que le réseau routier est récupéré, on peut le construire ensuite dans des graphiques NetworkX : OSMNx est également capable de vérifier si les noeuds dans la topologie du réseau ont bien leur intersection et des impasses, les corriger automatiquement en cas d'erreur. Il peut aussi calculer les chemins les plus courts d'un noeud à un autre. 


---



### Sources

*   https://geoffboeing.com/2016/11/osmnx-python-street-networks/ (site exemple "officiel" -- blog de Geoff Boeing, présentation sur OSMNx)

*   https://geoffboeing.com/publications/osmnx-complex-street-networks/ (site exemple "officiel" -- blog de Geoff Boeing, présentation sur OSMNx)

*   https://www.researchgate.net/publication/316444466_OSMnx_A_Python_package_to_work_with_graph-theoretic_OpenStreetMap_street_networks (documentation - article : présentation sur OSMNx)

*   https://fr.wikipedia.org/wiki/OpenStreetMap (présentation OpenStreetMap)


---

# NetworkX 

### Présentation

NetworkX est, tout comme OSMNx, un package utilisé en Python mais permettant ici de créer, manipuler, et étudier la structure des réseaux complexes / des graphes.

Il a été crée en 2002, la version originale par Aric Hagberg, mais la version publique ne sera publiée qu'en 2005. 

### Graphe
C'est un ensemble de noeud reliés par des ponts. Dans NetworkX, les noeuds dans le graphe peuvent être n'importe quel objet hashable, comme par exemple une chaîne de texte, image, graphique , etc.

### Fonctionnement

Il faut d'abord instancier un graphe en utilisant NetworkX. Ensuite pour le visualiser / mémoriser, on importe la bilibliothèque Mathplotlib ou Graphviz. 

---

### Sources

*   https://qiita.com/kzm4269/items/081ff2fdb8a6b0a6112f (site exemple : base d'utilisation de NetworkX)

*   https://he-arc.github.io/livre-python/networkx/index.html (site exemple)

*   https://iut-info.univ-reims.fr/users/blanchard/ISN20181218/utilisation-de-la-bibliotheque-networkx.html (site documentaire : présentation sur NetworkX)

*   https://networkx.org/documentation/stable/index.html (site documentaire : présentation sur NetworkX)

*   https://networkx.org/documentation/stable/tutorial.html (site documentaire : utlisation de Networkx)

