# Ombre portée

Simulation de l'ombre portée d'un futur immeuble sur un plan cadastral.

## Lancement

Aucune installation : double-cliquez sur **`ombre-portee.html`**. Le fichier s'ouvre dans votre navigateur (Chrome, Edge ou Firefox, sur PC).
L'application fonctionne hors ligne. Internet n'est nécessaire que pour ouvrir un PDF et pour lire automatiquement la longueur de l'échelle.

## Site à partir d'une adresse (recommandé)

Dans le bloc « Site à partir d'une adresse », tapez l'adresse, choisissez la taille du carré (100 à 800 m) et le fond de plan, puis cliquez sur **Charger le site**. Le logiciel télécharge auprès de l'IGN (Géoplateforme, gratuit, sans compte) :

- le **fond de plan** : plan IGN, photo aérienne et cadastre, à l'échelle exacte, nord en haut. Le fond (plan, photo ou blanc) et le cadastre se changent aussitôt, sans recharger ;
- les **bâtiments** de la BD TOPO, avec leur contour exact, leur hauteur jusqu'au faîtage et l'altitude de leur pied. Là où le LiDAR existe, la **forme du toit** (pentes, pignons) est tirée du modèle de surface ; la hauteur maximale reste réglable par clic droit ;
- le **relief** : modèle de terrain LiDAR HD au demi-mètre, complété par le RGE ALTI là où le LiDAR manque.
- les **arbres** : hauteur de la végétation = modèle de surface LiDAR HD − terrain, hors bâtiments. Chaque houppier est repéré et dessiné en arbre (tronc jusqu'au quart de la hauteur, houppier qui s'évase dès le tiers) ; haies et arbustes restent en masse continue. La case « Arbres » les affiche ou les masque aussitôt, et « Transparence arbres » atténue leur feuillage et leurs ombres (arbres dénudés en hiver).

La latitude, la longitude et l'orientation du nord sont réglées automatiquement. La vue passe en 3D : les bâtiments sont posés sur le relief et les ombres tombent sur le terrain en pente et sur les bâtiments. Placez ensuite votre immeuble (rectangle vert, posé sur le terrain) et ajustez ses dimensions. Un clic droit sur un bâtiment permet de corriger sa hauteur.

Il faut une connexion Internet au moment du chargement. Une fois enregistré, le projet contient toutes les données et s'ouvre hors ligne.

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
| Sol en pente | « Niveau / terrain » : hauteur du pied de l'immeuble par rapport au terrain où tombe l'ombre (+ = plus haut, − = plus bas). L'ombre est calculée pour H + niveau. |
| Déplacer ou pivoter l'immeuble | Glisser l'immeuble pour le déplacer. Les poignées carrées le redimensionnent, la poignée ronde le pivote (Maj = pas de 15°). |
| Trajectoire de l'ombre d'un point | Bouton « Trajectoire », puis clic sur un coin (aimanté) ou un point du toit. La courbe de la journée est graduée heure par heure. |
| Scénario | « + Instant courant » ou un modèle : solstices et équinoxes (à l'heure courante, ou à 6 h, 9 h, midi, 15 h, 18 h, 21 h), journée toutes les 3 h, 2 h ou 1 h, le 21 de chaque mois. Les heures des modèles sont légales ou solaires (option). Les instants de nuit sont ignorés. Chaque ombre a sa couleur et une légende qui pointe sur le bord de l'ombre. |
| Échelle | « Tracer l'échelle » pour en définir une, « Effacer l'échelle » pour la supprimer. |
| Panneau de gauche | Cliquer sur le titre d'un bloc (Immeuble, Lieu et orientation…) pour le replier ou le déplier. |
| Vue 3D | Bouton « 3D », ou **Maj + glisser** sur le plan. En 3D : Maj + glisser (ou clic droit + glisser) pour pivoter et incliner, glisser pour déplacer la vue, glisser l'immeuble pour le déplacer, molette pour zoomer. « Vue de dessus » remet le nord en haut. Les ombres de l'instant courant sont projetées sur le sol et sur les bâtiments. |
| Hauteur des constructions voisines | **Clic droit** sur une construction (en 2D ou en 3D) : une fenêtre demande sa hauteur, réglable à la molette. La hauteur reste affichée sur la construction. Un nouveau clic droit permet de la modifier ou de la supprimer. « Hauteur par défaut » s'applique aux constructions sans hauteur saisie (0 = à plat). |
| Plusieurs immeubles | « Dessiner un immeuble » en ajoute un, « + Copie » duplique l'immeuble sélectionné, « Supprimer » l'enlève. Clic sur un immeuble pour le sélectionner (boutons n° 1, n° 2… dans le panneau). Chacun a sa hauteur et son niveau. Ils sont conservés quand on recharge le site. |
| Boussole et cadran solaire | En haut à droite du plan. Glisser l'ombre du style du cadran change l'heure ; un clic le remet à midi solaire. En 3D, glisser l'aiguille fait tourner la vue et un clic remet le nord en haut ; en 2D, l'aiguille règle le « Nord du plan » et un clic revient à la valeur d'origine. |
| Fond | « Luminosité » et « Contraste du fond » (bloc Affichage) éclaircissent ou assombrissent le fond et les arbres, utile avec la photo aérienne. Double-clic sur un curseur pour revenir à la valeur par défaut. |
| Animer | « ▶ Animer la journée » (la nuit est sautée). |
| Zoom et déplacement du plan | Molette sur le plan pour zoomer. Glisser le fond, ou clic droit, pour déplacer la vue. |
| Clavier | ←/→ ±15 min · ↑/↓ ±1 jour · PgPréc/PgSuiv ±1 mois · +/− hauteur · Espace : animer · Échap : annuler |

## Enregistrer et imprimer

- **Enregistrer le projet** (`.ombre.json`) : enregistre le plan et tous les réglages : immeuble, échelle, lieu, scénarios, hauteurs des constructions, vue 2D ou 3D et position de la caméra. Rouvrez-le avec « Ouvrir… » pour retrouver exactement le même état.
- **Enregistrer le plan modifié** (PNG) : le plan d'origine, avec le rectangle vert à sa nouvelle position et à ses nouvelles dimensions.
- **Exporter la vue** (PNG) : la vue actuelle, avec les ombres et les légendes.
- **Imprimer** : la vue actuelle, avec un en-tête qui récapitule les données (date, lieu, dimensions, scénario).

## Calcul

La position du soleil suit l'algorithme de la NOAA, avec correction de la réfraction atmosphérique. La précision est d'environ 0,01° sur la période 1950-2050.
Le sol est supposé horizontal. En 2D, l'ombre est la projection du parallélépipède de l'immeuble sur le sol. En 3D (WebGL, sans connexion Internet), les ombres sont calculées par carte d'ombre : elles tombent aussi sur les constructions voisines, qui projettent elles-mêmes leur ombre. La partie « niveau / terrain » de l'immeuble apparaît en socle brun.
