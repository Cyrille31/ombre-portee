# Ombre portée

Simulation de l'ombre portée d'un futur immeuble sur un plan cadastral.

## Lancement

Aucune installation : double-cliquez sur **`ombre-portee.html`**. Le fichier s'ouvre dans votre navigateur (Chrome, Edge ou Firefox, sur PC).
L'application fonctionne hors ligne. Internet n'est nécessaire que pour ouvrir un PDF et pour lire automatiquement la longueur de l'échelle.

## Site à partir d'une adresse (recommandé)

Dans le bloc « Site à partir d'une adresse », tapez l'adresse, choisissez la taille du carré (100 à 800 m) et le fond de plan, puis cliquez sur **Charger le site**. Le logiciel télécharge auprès de l'IGN (Géoplateforme, gratuit, sans compte) :

- le **fond de plan** : plan IGN, photo aérienne et cadastre, à l'échelle exacte, nord en haut. Les dimensions actuelles de la zone s'affichent à côté de « Zone de ». La photo aérienne est le fond par défaut. Les cases « Photo aérienne » (sinon plan IGN) et « Cadastre » changent le fond aussitôt, sans recharger ;
- les **bâtiments** de la BD TOPO, avec leur contour exact, leur hauteur jusqu'au faîtage et l'altitude de leur pied. Là où le LiDAR existe, la **forme du toit** (pentes, pignons) est tirée du modèle de surface ; la hauteur maximale reste réglable par clic droit ;
- le **relief** : modèle de terrain LiDAR HD au demi-mètre, complété par le RGE ALTI là où le LiDAR manque.
- les **arbres** : hauteur de la végétation = modèle de surface LiDAR HD − terrain, hors bâtiments. Chaque houppier est repéré et dessiné en arbre (tronc jusqu'au quart de la hauteur, houppier qui s'évase dès le tiers) ; haies et arbustes restent en masse continue. La case « Arbres » les affiche ou les masque aussitôt, et « Transparence arbres » atténue leur feuillage et leurs ombres (arbres dénudés en hiver).

La latitude, la longitude et l'orientation du nord sont réglées automatiquement. La vue passe en 3D : les bâtiments sont posés sur le relief et les ombres tombent sur le terrain en pente et sur les bâtiments. Placez ensuite votre immeuble (rectangle vert, posé sur le terrain) et ajustez ses dimensions. Un clic droit sur un bâtiment permet de corriger sa hauteur.

Il faut une connexion Internet au moment du chargement. Une fois enregistré, le projet contient toutes les données et s'ouvre hors ligne.

**Agrandir la zone** : des poignées bleues sont placées aux coins et au milieu des bords du plan (en 2D et en 3D). Glissez-en une : le nouveau rectangle s'affiche avec ses dimensions, puis il est rechargé (jusqu'à 1 000 m de côté). Les immeubles ajoutés, la vue et les réglages sont conservés. Les bâtiments sont découpés au bord du plan : seules les parties sur le plan sont gardées.

## Préparer un plan (image ou PDF)

- Une **image** du plan cadastral (PNG, JPG…) ou un **PDF** (seule la page 1 est utilisée).
- L'immeuble projeté est un **rectangle vert**, plein ou en contour. Le bleu clair des piscines est ignoré. Un rectangle bleu franc est encore accepté s'il n'y a pas de vert (anciens plans).
- Un **segment rouge** donne l'échelle. Si un nombre est écrit à côté (par exemple « 20 m » ou « 26,98 m », en noir ou en rouge), le logiciel essaie de le lire automatiquement. Vérifiez la valeur lue, virgule comprise. Sinon, saisissez la longueur dans « Longueur réelle ».
- Les **constructions existantes** sont les aplats orange ou jaunes du cadastre. Elles sont détectées automatiquement, même quand un trait noir les coupe.
- Le nord est supposé en haut du plan. Sinon, indiquez l'angle dans « Nord du plan ».

À l'ouverture, le rectangle vert est détecté puis effacé du fond de plan. Il devient l'immeuble, que l'on peut déplacer et modifier.
Le bouton **Plan de démonstration** permet d'essayer le logiciel sans fichier.

Le lieu par défaut est Toulouse.

## Utilisation

| Action | Comment |
|---|---|
| Changer l'heure ou la date | Molette sur le jour, le mois, l'année, l'heure ou les minutes (Maj = pas fin). On peut aussi glisser verticalement, double-cliquer pour saisir, ou utiliser les curseurs « Heure » et « Jour » (à la souris ou à la molette). |
| Heure locale / TU | Commutateur « Heure locale » / « TU ». L'heure locale applique le fuseau et le changement d'heure européen. |
| Hauteur et dimensions | Molette sur le champ, ou glisser verticalement sur son libellé. On peut aussi saisir la valeur directement. L'emprise au sol (m²) est affichée sous les dimensions. Au départ, la longueur est le grand côté. |
| Sol en pente | Sur un site IGN, l'immeuble est posé sur le relief. La case « Hauteur comptée depuis le point le plus haut du terrain » choisit le point de référence de la hauteur (sinon le point le plus bas). |
| Déplacer ou pivoter l'immeuble | Glisser l'immeuble pour le déplacer. Les poignées carrées le redimensionnent, la poignée ronde le pivote (Maj = pas de 15°). |
| Trajectoire de l'ombre d'un point | Bouton « Trajectoire », puis clic sur un coin (aimanté) ou un point du toit. La courbe de la journée est graduée heure par heure. |
| Scénario | « + Instant courant » ou un modèle : solstices et équinoxes (à l'heure courante, ou à 6 h, 9 h, midi, 15 h, 18 h, 21 h), journée toutes les 3 h, 2 h ou 1 h, le 21 de chaque mois. Les heures des modèles sont légales ou solaires (option). Les instants de nuit sont ignorés. Chaque ombre a sa couleur et une légende qui pointe sur le bord de l'ombre. |
| Échelle | « Tracer l'échelle » pour en définir une, « Effacer l'échelle » pour la supprimer. |
| Panneau de gauche | Cliquer sur le titre d'un bloc (Immeuble, Lieu et orientation…) pour le replier ou le déplier. |
| Vue 3D | Bouton « 3D », ou **Maj + glisser** sur le plan. En 3D : Maj + glisser (ou clic droit + glisser) pour pivoter et incliner, glisser pour déplacer la vue, glisser l'immeuble pour le déplacer, molette pour zoomer. « Vue de dessus » remet le nord en haut. Les ombres de l'instant courant sont projetées sur le sol et sur les bâtiments. |
| Hauteur des constructions voisines | **Clic droit** sur une construction (en 2D ou en 3D) : une fenêtre demande sa hauteur, réglable à la molette. La hauteur reste affichée sur la construction. Un nouveau clic droit permet de la modifier ou de la supprimer. « Hauteur par défaut » s'applique aux constructions sans hauteur saisie (0 = à plat). |
| Modifier l'immeuble | **Double-clic** sur l'immeuble (en 2D ou en 3D) : son toit porte les mêmes poignées qu'en 2D (carrées pour l'étirer, ronde pour le pivoter, Maj = pas de 15°) ; un simple glisser le déplace ; un clic ailleurs masque les poignées. Couleurs du toit et des murs : clic droit sur l'immeuble, ou bloc Immeuble. |
| Éditeur de toit | Clic droit sur un immeuble projeté → « Éditeur de toit ». Glisser depuis un sommet, un bord ou une ligne trace une ligne ; le point ou le segment survolé est entouré de bleu et la ligne s'y accroche à l'endroit exact du clic ; presque parallèle à un côté, elle le devient (seulement si son extrémité reste sous le pointeur) ; en 3D, le point visé est pris exactement sur le pan sous la souris, même très incliné ; une ligne qui s'arrête au milieu sert de départ à d'autres. Les points, segments et pans qu'on peut monter ou descendre sans tordre un pan sont entourés de blanc : clic droit, puis molette ou saisie. On peut monter au-dessus du faîtage : à la fermeture du menu, le point le plus haut revient à la hauteur de l'immeuble et tout le toit descend d'autant. « Décrocher ce pan » (clic droit dans un pan) en fait un toit indépendant, séparé du reste par un mur vertical, puis propose sa hauteur ; il fonctionne aussi pour un pan collé au bord du toit. Une forme dessinée depuis un point libre, au milieu d'un pan, puis refermée (cheminée, édicule…) devient un toit indépendant, sans s'accrocher aux lignes qu'elle croise (à cheval sur le faîtage, son dessus est mis à plat au niveau de son point le plus haut) : sa hauteur se règle par clic droit dedans, vers le haut (cheminée) ou vers le bas (puits de lumière, le pan qui l'entoure est alors percé) ; ses murs vont jusqu'au pan qui la porte. En traçant un rectangle, le 3e côté marque un arrêt (petit carré) quand il atteint la longueur du 1er. Une ligne qui s'arrête au milieu d'un pan ne peut pas être montée ni descendue, et une ligne dont la suppression laisserait un pan gauche (non plan) ne peut pas être supprimée. Clic droit dans un pan : « Couleur du pan » ou « Couleur de tout le toit ». En 3D, les lignes cachées par le toit lui-même sont en pointillés ; hors édition, les arêtes des toits édités sont tracées un peu plus sombres que les deux pans qu'elles séparent (en 2D comme en 3D) ; en 3D, elles sont masquées derrière les arbres (visibles seulement selon leur transparence). Chaque pan est éclairé selon l'angle du soleil sur sa pente (dégradé continu au fil de la journée), en 3D et, plus discrètement, en 2D. Clic droit sur un point en attente ou au milieu d'une ligne droite : le supprimer ; les points devenus inutiles disparaissent seuls. Ctrl+Z : annuler. Échap : terminer. |
| Façades | Dans le menu de l'immeuble (clic droit) : façade unie, logements (fenêtres, balcons, portes), bureaux (vitrage) ou hangar (bardage, porte sectionnelle), dessinées à l'échelle (étages de 2,8 à 3,5 m). Aussi sur les constructions voisines, pour une seule ou pour toutes. Par défaut : logements, pour les immeubles projetés comme pour les constructions voisines. |
| Plusieurs immeubles | « Dessiner un immeuble » en ajoute un, « + Copie » duplique l'immeuble sélectionné, « Supprimer » l'enlève. Clic sur un immeuble pour le sélectionner (boutons n° 1, n° 2… dans le panneau). Chacun a sa hauteur et ses couleurs. Ils sont conservés quand on recharge le site. |
| Boussole, cadran solaire, calendrier | En haut à droite du plan. Clic droit sur chacun pour régler le pas de sa molette (boussole : 10° ; cadran : 1 h ; calendrier : 1 jour, 1 semaine, ½ mois, 1 mois, ½ saison ou 1 saison ; les saisons passent par les solstices et équinoxes, les demi-saisons aussi par les mi-saisons). La flèche du calendrier se glisse aussi sur les douze mois. Le cadran, dans le style des cadrans d'autrefois (chiffres romains, quarts d'heure, devise en petit le long du bord), est orienté comme le plan : l'ombre du style a la même direction que l'ombre des immeubles. Glisser cette ombre change l'heure ; la molette (vers soi = plus tard) saute d'heure en heure, calée sur midi ; un clic remet à midi, en heure légale (ou au midi solaire, au choix dans le menu du clic droit). Dans ce menu, la molette sur la vue agrandit ou réduit le cadran (en % de sa taille), pour lire sa devise ; il reprend sa taille à la fermeture du menu. L'aiguille de la boussole fait tourner la vue, en 2D comme en 3D ; un clic remet le nord en haut. |
| Fond | « Opacité de l'ombre » s'applique en 2D et en 3D. « Luminosité » et « Contraste du fond » (bloc Affichage) éclaircissent ou assombrissent le fond et les arbres, utile avec la photo aérienne. Les curseurs se règlent aussi à la molette ; double-clic pour revenir à la valeur par défaut. |
| Textes d'aide | Le bouton « Aides » en haut du panneau les masque ou les affiche. |
| Animer | « ▶ Animer la journée » : entre le coucher et le lever du soleil, une seconde de nuit. |
| Zoom et déplacement du plan | Molette sur le plan pour zoomer. Glisser le fond pour déplacer la vue (ou Maj + clic droit). **Glisser avec le clic droit** passe en 3D en inclinant la vue ; revenir à la verticale repasse en 2D. L'orientation est conservée. |
| Afficheur | Sous les cadrans : jour et mois, heure et minutes, avec les boutons Animer, vitesse (de très lent à très rapide) et Maintenant (qui arrête l'animation, comme un choix d'heure sur le cadran). Cases « Immeuble » (afficher les immeubles projetés ; décochée, leur ombre reste visible si « Ombre » est cochée), « Ombre » (masquer leur ombre pour mieux lire un scénario), « Photo » (photo aérienne ou plan IGN) et « Arbres » (ces deux dernières une fois un site chargé). |
| Règle | Clic droit sur le fond → « Règle depuis ce point » : la longueur suit la souris (avec le dénivelé si le relief est connu) ; clic gauche pour la fixer ; un nouveau clic l'efface. |
| Clic droit (sans bouger) | Menu local : sur l'immeuble (hauteur, couleurs du toit et des murs), une construction (hauteur, retour à la hauteur d'origine, affichage des hauteurs), un arbre (transparence, bas du feuillage pour cet arbre ou tous), le fond (luminosité, contraste, opacité de l'ombre, photo, cadastre, arbres, immeubles projetés visibles ou non), un cadran (pas de la molette). Le menu du fond propose aussi « Dessiner un nouvel immeuble ». |
| Clavier | ←/→ ±15 min · ↑/↓ ±1 jour · PgPréc/PgSuiv ±1 mois · +/− hauteur · Espace : animer · Échap : annuler |

## Enregistrer et imprimer

- **Enregistrer le projet** (`.ombre.json`) : enregistre le plan et tous les réglages : immeuble, échelle, lieu, scénarios, hauteurs des constructions, vue 2D ou 3D et position de la caméra. Rouvrez-le avec « Ouvrir… » pour retrouver exactement le même état.
- **Enregistrer le plan modifié** (PNG) : le plan d'origine, avec le rectangle vert à sa nouvelle position et à ses nouvelles dimensions.
- **Exporter la vue** (PNG) : la vue actuelle, avec les ombres et les légendes.
- **Imprimer** : la vue actuelle, avec un en-tête qui récapitule les données (date, lieu, dimensions, scénario).

## En cas d'erreur

Si une erreur se produit, une fenêtre l'indique et le logiciel continue de fonctionner. « Copier le rapport » copie un rapport (erreur, dernières actions, état du projet) à coller dans un message pour faire corriger le problème ; « Enregistrer un projet de secours » sauvegarde le travail en cours. Le projet est aussi sauvegardé automatiquement chaque minute dans le navigateur : si la page s'est fermée anormalement, la restauration est proposée au lancement suivant.

## Calcul

La position du soleil suit l'algorithme de la NOAA, avec correction de la réfraction atmosphérique. La précision est d'environ 0,01° sur la période 1950-2050.
Le sol est supposé horizontal. En 2D, l'ombre est la projection du parallélépipède de l'immeuble sur le sol. En 3D (WebGL, sans connexion Internet), les ombres sont calculées par carte d'ombre : elles tombent aussi sur les constructions voisines, qui projettent elles-mêmes leur ombre. 
