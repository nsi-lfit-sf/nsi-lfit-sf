# OSMNx 

### Présentation

OSMnx est une bibliothèque utilisée en Python permettant de récupérer, de modéliser, d'analyser et de visualiser les données des réseaux de rue tout en prenant l'information de la carte à partir d'OpenStreetMap. Il a été développé par Geoff Boeing, directeur du laboratoire des données urbaines (Urban Data Lab) à l'université de Californie du Sud. 

>  ### OpenStreetMap: 
L'OpenStreetMap est un projet collaboratif de cartographie en ligne, mis en route par Steve Coast à l'University College de Londres en 2004, qui vise à constituer une base de données géographiques libre du monde, en utilisant le système GPS et d'autres données libres.

### Fonctionnement

Le code "type" pour la création de la carte de rue géographique avec OSMNx est le suivant :

```
# On installe la bibliothèque OSMNx avec le pip
pip install osmnx

```

```
# Puis on importe OSMNx à partir de la bibliothèque installée
import osmnx as ox   

# On définit ici G comme le nom de la cartographie créee ; 
# Le 'center_point' permet ici de déterminer la place où on veut afficher les réseaux de rue, cela peut être fait à partir des coordonnées, le nom d'une ville, de pays... plus l'échelle deviendra grande, plus le traitement devient évidememnt lourd. 
# 'network_type' permet de régler le type de réseau qu'on veut "cartographier", ici on choisit le réseau de rue de type routier. 
# Le résultat nous affichera donc le réseau routier autour de Kyoto Gyoen, au Japon. 
# Enfin le 'dist' permet de régler la limite de distance que l'on désire afficher à partir du point de centre depuis les coordonnées, ici on règle de 1000 m de distance. 

G = ox.graph_from_point(center_point=(35.02514, 135.76239), network_type='drive', dist=1000)
ox.plot_graph(ox.project_graph(G))
```
Une fois que le réseau routier est récupéré, on peut le construire ensuite dans des graphiques NetworkX.

OSMNx est également capable de vérifier si les noeuds dans la topologie du réseau ont bien leur intersection et des impasses, les corriger automatiquement en cas d'erreur. 

Il peut aussi calculer les chemins les plus courts d'un noeud à un autre:

```
import osmnx as ox
import networkx as nx

G = ox.graph_from_point(center_point=(35.02514, 135.76239), network_type='drive', dist=1000)

orig = ox.get_nearest_node(G, (35.0273781558413,135.75774513168687 ))
dest = ox.get_nearest_node(G, (35.02336407861095,135.7675511280653))
route = nx.shortest_path(G, orig, dest)
fig, ax = ox.plot_graph_route(G, route, route_linewidth=6, node_size=0, bgcolor='k')
```



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

