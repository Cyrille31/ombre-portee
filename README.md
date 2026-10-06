# Ombre portée

Simulation de l'ombre portée d'un futur immeuble sur un plan cadastral.

## Lancement

Aucune installation : double-cliquez sur **`ombre-portee.html`**. Le fichier s'ouvre dans votre navigateur (Chrome, Edge ou Firefox, sur PC).
L'application fonctionne hors ligne. Internet n'est nécessaire que pour ouvrir un PDF et pour lire automatiquement la longueur de l'échelle.

## Préparer le plan

- Une **image** du plan cadastral (PNG, JPG…) ou un **PDF** (seule la page 1 est utilisée).
- L'immeuble projeté est un **rectangle bleu**, plein ou en contour.
- Un **segment rouge** donne l'échelle. Si un nombre est écrit à côté (par exemple « 20 m »), le logiciel essaie de le lire automatiquement. Sinon, saisissez la longueur dans « Longueur réelle ».
- Le nord est supposé en haut du plan. Sinon, indiquez l'angle dans « Nord du plan ».

À l'ouverture, le rectangle bleu est détecté puis effacé du fond de plan. Il devient l'immeuble, que l'on peut déplacer et modifier.
Le bouton **Plan de démonstration** permet d'essayer le logiciel sans fichier.

## Utilisation

| Action | Comment |
|---|---|
| Changer l'heure ou la date | Molette sur le jour, le mois, l'année, l'heure ou les minutes (Maj = pas fin). On peut aussi glisser verticalement, double-cliquer pour saisir, ou utiliser les curseurs. |
| Heure locale / TU | Commutateur « Heure locale » / « TU ». L'heure locale applique le fuseau et le changement d'heure européen. |
| Hauteur et dimensions | Molette sur le champ, ou glisser verticalement sur son libellé. On peut aussi saisir la valeur directement. |
| Déplacer ou pivoter l'immeuble | Glisser l'immeuble pour le déplacer. Les poignées carrées le redimensionnent, la poignée ronde le pivote (Maj = pas de 15°). |
| Trajectoire de l'ombre d'un point | Bouton « Trajectoire », puis clic sur un coin (aimanté) ou un point du toit. La courbe de la journée est graduée heure par heure. |
| Scénario | « + Instant courant » ou un modèle (solstices et équinoxes, journée…). Chaque ombre a sa couleur et une légende, placées sans chevauchement. |
| Animer | « ▶ Animer la journée » (la nuit est sautée). |
| Zoom et déplacement du plan | Molette sur le plan pour zoomer. Glisser le fond, ou clic droit, pour déplacer la vue. |
| Clavier | ←/→ ±15 min · ↑/↓ ±1 jour · PgPréc/PgSuiv ±1 mois · +/− hauteur · Espace : animer · Échap : annuler |

## Enregistrer et imprimer

- **Enregistrer le projet** (`.ombre.json`) : enregistre le plan et tous les réglages (immeuble, échelle, lieu, scénario…). Rouvrez-le avec « Ouvrir… ».
- **Enregistrer le plan modifié** (PNG) : le plan d'origine, avec le rectangle bleu à sa nouvelle position et à ses nouvelles dimensions.
- **Exporter la vue** (PNG) : la vue actuelle, avec les ombres et les légendes.
- **Imprimer** : la vue actuelle, avec un en-tête qui récapitule les données (date, lieu, dimensions, scénario).

## Calcul

La position du soleil suit l'algorithme de la NOAA, avec correction de la réfraction atmosphérique. La précision est d'environ 0,01° sur la période 1950-2050.
Le sol est supposé horizontal. L'ombre est la projection du parallélépipède de l'immeuble sur le sol.
