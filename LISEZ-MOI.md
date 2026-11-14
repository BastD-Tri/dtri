# D Tri Training

Ton application de triathlon sur téléphone Android : journal de toutes tes activités, séances de natation, vélo et course, renfo, poids, nutrition, ressenti, plans d'entraînement et bilans mensuels. Le vélo se pilote en direct sur ton home trainer Wahoo KICKR.

## Ce que fait l'app

- **Journal** : toutes tes activités au même endroit. Tes activités Garmin Connect arrivent toutes seules (clé API personnelle Garmin), tes nages FORM via intervals.icu ; tu peux aussi les saisir à la main ou importer des fichiers .FIT/.zip exportés de Garmin Connect. Un fichier de triathlon donne une activité par sport.
- **Vélo** : tes séances KICKR en mode ERG (l'app règle la puissance), avec 55 séances prêtes (dont des séances de cadence et de vélocité), des séances surprise et le ramp test. Envoi direct sur Strava ; fichier .FIT pour Garmin Connect.
- **Course** : 23 séances (footing, sortie longue, seuil, VMA, côtes, enchaînements, tests) et des séances surprise. Les cibles sont des allures calculées sur ton allure seuil, ou des zones de fréquence cardiaque. Chaque séance s'envoie sur ta montre.
- **Séances à la durée de ton choix** : sur chaque séance (vélo, course, natation), choisis le temps dont tu disposes (20 à 120 min). L'app recalcule la séance : nombre de répétitions, durée des blocs, échauffement et retour au calme. Une 30/30 VMA de 55 min devient ainsi 10 × 30/30 en 30 min. Dans Séances, le réglage « Temps dont je dispose » adapte toute la liste d'un coup. Les tests gardent leur durée.
- **Natation** : 15 séances (technique, endurance, CSS, vitesse, eau libre, test CSS) calculées sur ta CSS. Chaque séance a une « fiche piscine » à lire au bord du bassin ou à photographier pour les lunettes FORM.
- **Renfo** : 12 circuits réglables avec minuteur guidé, 33 exercices avec schéma animé et fiche « comment faire », et saisie libre des séries, répétitions, durées et charges.
- **Étirements** : 8 routines par sport (mobilité avant, étirements après), 28 étirements avec schéma animé, minuteur guidé, et un sport « Étirements » dans le journal.
- **Ressenti et nutrition** : après chaque activité, tu notes l'effort perçu, tes sensations et des repères (fringale, crampes…), puis ce que tu as mangé et bu (gels, bidons, barres…). L'app calcule glucides par heure, liquides et sodium, compare aux repères usuels selon la durée, et fait le lien entre nutrition et sensations sur tes séances longues.
- **Poids** : suivi des pesées avec tendance sur 7 jours.
- **Plan** : plan triathlon S, M, L (70.3) ou XL (Ironman), cross triathlon (VTT + trail), vélo (route ou VTT) ou course à pied (route ou trail). Il tient compte de ta date de course, tes jours libres, tes heures, ton niveau dans chaque sport et ton sport faible. Au programme : périodisation, semaines allégées, enchaînements vélo-course, renfo, tests et affûtage. Tu peux déplacer, changer, ajouter ou retirer des séances, en vue semaine ou mois. Version IA (Claude) en option. Les étirements y sont placés selon tes séances, et le plan a une vue d'ensemble, le prévu face au réalisé, « Alléger cette semaine » et une check-list de la semaine de course.
- **Bilan** : récapitulatif de chaque mois (heures, distances et charge par sport, calendrier, charge par semaine, forme/fatigue, poids, renfo, nutrition et ressenti).

## La cadence sur le home trainer

- Le KICKR mesure ta cadence et l'app l'enregistre à chaque seconde (fichiers .FIT et .TCX, Strava, Garmin).
- Certaines étapes ont une consigne de cadence : séances haute cadence à 110 rpm, vélocité progressive 90 → 120, force à 55-60 rpm, force-vélocité alternée, Sweet Spot en sur-vélocité, pré-enchaînement. La séance surprise propose aussi le type « Cadence ».
- Pendant la séance, la consigne s'affiche à côté de la puissance. La tuile cadence passe au vert quand tu es à ±5 rpm de la cible. Si tu t'en écartes de plus de 8 rpm pendant 10 s, l'app t'avertit à l'écran, à la voix et par vibration.
- Après la séance, le tableau des intervalles compare la cadence réalisée à la cible, et la courbe de cadence s'ajoute au graphique.
- Tu as un capteur de cadence Bluetooth sur la manivelle ? Connecte-le dans Accueil → Home trainer. Il devient prioritaire sur la mesure du KICKR. Il est facultatif.
- Dans tes propres séances, ajoute `c95` à une étape pour fixer une cadence, par exemple `5x(3m@75 c110, 2m@60 c90)`.

## Séances libres (tapis et home trainer)

Pour faire ta propre séance en pilotant la machine depuis le téléphone, sans choisir de séance : Accueil → Appareils → **Tapis libre** ou **Vélo libre** (aussi dans Séances).

- **Tapis libre** : cinq boutons de vitesse (4, 8, 10, 12, 14 km/h par défaut, modifiables dans Réglages du tapis) et des réglages fins −0,5 / −0,1 / +0,1 / +0,5 km/h. Si le tapis tourne déjà, la séance démarre tout de suite et l’app prend la main. S’il est à l’arrêt, un appui sur une vitesse lance un compte à rebours de 3 s, puis la bande démarre à cette vitesse. Le bouton « Arrêter le tapis » reste toujours visible. Un changement fait sur la console est suivi par l’app.
- **Vélo libre** : les tuiles KICKR et pédales sont toujours affichées ; si les pédales ne sont pas connectées, le bouton « Connecter les pédales » de leur tuile les ajoute en pleine séance. En mode Puissance (ERG), cinq boutons calés sur ta FTP (Récup, Endurance, Tempo, Seuil, PMA) et des réglages fins de ±5 / ±10 W. En mode Pente, le KICKR simule une pente de 0 à 8 % (réglages de ±0,5 / ±1 %) et tu gères l’effort avec tes vitesses. Avec les pédales Assioma, KICKR et pédales s’affichent côte à côte.
- **Affichage** : vitesse ou puissance en grand avec la consigne, puis temps, distance, allure (actuelle et moyenne) ou cadence, FC, calories ou kJ, moyenne et graphique de la séance.
- **Tours** : chaque bouton de préréglage ouvre un nouveau tour ; le bouton « Tour » en ajoute un quand tu veux. Ils apparaissent comme intervalles dans la fiche de l’activité.
- **Terminer** enregistre la séance dans le Journal (avec export Strava et Garmin, comme les autres).

## Forme du jour

- **Vélo** : dans la fiche d’une séance, « Forme du jour » affiche la puissance de l’effort le plus dur. Baisse-la ou monte-la par pas de 5 W, ou choisis un raccourci (Fatigué −10 %, −5 %, Normal, +3 %, En forme +5 %) : toutes les consignes de la séance changent dans la même proportion.
- **Tapis** : même principe sur l’écran de départ « Sur le tapis », avec la vitesse de l’effort le plus rapide, par pas de 0,1 km/h. Si la séance dépasse ta vitesse maximale autorisée, l’app te propose de tout réduire en proportion plutôt que de seulement plafonner les passages rapides.
- **Sans limite** : touche la valeur (watts ou km/h) pour taper directement celle que tu veux, par exemple 12 km/h sur un programme prévu à 8 km/h. Seules restent les limites physiques : sur le tapis, aucune consigne ne dépasse ta vitesse maximale autorisée ni ne descend sous la vitesse mini du tapis.
- Le réglage est retenu pour la journée, séparément pour le vélo et la course : les autres séances du jour partent avec la même forme. Les tests (FTP, seuil) ne sont jamais modifiés.
- En cours de séance, les boutons – / + du lecteur ajustent encore de 2 % en 2 %. La fiche de l’activité rappelle le pourcentage utilisé.

## Pédales Favero Assioma Duo

- **Connexion** : Accueil → Home trainer → Pédales Assioma Duo → Connecter, puis choisis l’appareil dont le nom commence par ASSIOMA. Le KICKR apparaît aussi dans la liste, car il mesure lui aussi la puissance : ne le choisis pas.
- **Avant de connecter** : fais tourner les manivelles pour réveiller les pédales et ferme l’app Favero Assioma. En Bluetooth, les pédales ne se connectent qu’à un seul appareil à la fois. Ta Forerunner peut rester appairée en ANT+, ça ne gêne pas.
- **Réglage Favero** : laisse la transmission Bluetooth sur un seul canal, pas « Dual channel L/R ». Sinon l’app ne reçoit que la moitié de la puissance (elle te prévient si elle le détecte).
- **Pendant la séance** : dès que tu as connecté tes pédales une fois, les tuiles KICKR et pédales s’affichent à chaque séance, avec « Connecter les pédales » si elles ne le sont pas encore. Le grand chiffre est la puissance de référence (les pédales par défaut). En dessous, deux tuiles montrent côte à côte le KICKR (puissance, cadence, résistance réglée) et les pédales (puissance, cadence, équilibre gauche/droite). La tuile encadrée est la référence.
- **ERG calé sur les pédales** : les pédales lisent souvent quelques watts de plus que le KICKR. L’app apprend cet écart et règle la résistance du KICKR pour que les pédales affichent exactement la cible. Tu peux le désactiver, ou choisir le KICKR comme référence, dans Réglages des pédales.
- **Cadence du KICKR** : le KICKR n’a pas de capteur de cadence, il l’estime d’après les à-coups du pédalage (« rpm est. »). En récupération ou avec un petit braquet, il affiche souvent la moitié de la vraie cadence : sa tuile l’indique alors (« cadence ≈ ½ »). L’app utilise toujours la cadence des pédales quand elles sont connectées (affichage, consignes, fichier envoyé à Strava et Garmin).
- **Si les pédales décrochent** : le KICKR prend le relais automatiquement et la séance continue.
- **Après la séance** : la fiche compare les deux capteurs (moyennes, écart en %, équilibre gauche/droite), et le graphique trace les deux puissances. Le fichier .FIT envoyé à Strava et Garmin contient la puissance de référence et l’équilibre gauche/droite.
- **Étalonnage** : les Assioma font leur zéro toutes seules. Le bouton « Étalonner maintenant » force un zéro (pieds hors des pédales, manivelles immobiles).

## Tapis de course (Domyos Run 100 et tapis FTMS)

- **Une seule fois** : dans l’app Domyos E-Connected, active le FTMS, ferme E-Connected, puis éteins et rallume le tapis.
- **Connexion** : Accueil → Appareils → Tapis de course → Connecter, puis choisis le tapis (nom commençant souvent par DOMYOS, pas ton KICKR). L’app indique si le tapis accepte qu’elle règle sa vitesse (« vitesse pilotable ») ou s’il envoie seulement ses données (« lecture seule »).
- **Lancer une séance** : ouvre une séance de course → « Sur le tapis » → « Je suis prêt ». Clé de sécurité en place, appuie sur START sur la console (ou « Lancer le tapis depuis l’app », avec un compte à rebours de 3 s). La séance démarre quand la bande tourne : l’app ne démarre jamais la bande toute seule.
- **Pendant la séance** : l’app règle la vitesse à chaque étape et annonce le changement 5 s avant. Elle envoie la consigne un peu en avance pour compenser le temps que met la bande à accélérer. Les étapes en distance (800 m…) suivent la distance du tapis. Les étapes en fréquence cardiaque ajustent la vitesse de 0,2 km/h toutes les 30 s pour rester dans la zone.
- **Reprendre la main** : un appui sur + ou – de la console (ou de la télécommande) et l’app ne touche plus à la vitesse jusqu’à l’étape suivante. Les boutons – / + de l’app accélèrent ou ralentissent toutes les consignes de 2 %.
- **Sécurité** : STOP ou clé retirée mettent la séance en pause. La vitesse maximale autorisée se règle dans Réglages du tapis (14 km/h par défaut, le maximum du Run 100) : une consigne plus rapide est plafonnée.
- **Si le tapis est en lecture seule** : l’app suit et enregistre la séance, et annonce à la voix la vitesse à régler sur la console.
- **Après la séance** : l’activité « course sur tapis » apparaît dans le Journal avec les allures visées et réalisées pour chaque intervalle, la FC et la distance. Elle s’envoie sur Strava comme une course en intérieur et sur Garmin Connect en fichier .FIT. Si tu enregistres aussi la séance avec ta Forerunner, n’envoie qu’une des deux sur Strava pour éviter le doublon.

## Programmes du tapis (Calories, Fractionné, Endurance)

Les 30 programmes intégrés du Run 100 (manuel, pages 9 à 11) sont dans **Séances → Course → Tapis de course** (raccourci « Programmes du tapis » sur l’accueil et dans la fiche du tapis). Dans « Toutes », une seule carte y mène, pour ne pas noyer les autres séances.

- **Calories 1 à 10** (15 à 60 min, jusqu’à 11 km/h) : variations d’allure modérées.
- **Fractionné 1 à 10** (« Interval training », 30 à 80 min, jusqu’à 13,2 km/h) : accélérations d’une minute entre des récupérations.
- **Endurance 1 à 10** (20 à 80 min, jusqu’à 9 km/h) : longs paliers stables avec une ou deux relances.
- **Sur le tapis**, l’app règle la vitesse minute par minute comme la console, mais avec en plus la forme du jour (–10 %, –5 %…), la reprise en main à la console, les annonces vocales et l’enregistrement complet (intervalles, FC, Strava, .FIT). Ils s’envoient aussi à la Forerunner, avec une fenêtre d’allure de ±0,2 km/h autour de chaque palier.
- **Durée fixe** : ce sont les programmes du fabricant, on ne les raccourcit pas. Choisis un autre numéro de la même famille.
- **Précision** : les profils ont été relevés sur les graphiques du manuel (paliers d’une minute, à ±0,3 km/h près). Les vitesses max de la famille Endurance correspondent au tableau du manuel, sauf Endurance 2, lue à 7,8 km/h sur le graphique contre 8,4 dans le tableau.

## Renfo : circuits et exercices

Dans **Séances → Renfo** :

- **Circuits** : 12 circuits rangés par objectif. Il y en a pour le corps entier (dont « Mon circuit habituel », un cardio express et un circuit en salle), pour le tronc et le gainage, pour la course (force, prévention, pliométrie douce), pour le vélo et pour la natation.
- **Tout se règle** dans la fiche d'un circuit :
  - **l'enchaînement** : en circuit (tous les exercices puis on recommence) ou série par série ;
  - **la mesure** : en répétitions (avec « Fait » quand tu as fini) ou au temps (même durée pour chaque exercice) ;
  - **le nombre de tours ou de séries**, **le temps d'effort**, **la récup entre exercices** et **la récup entre tours**, avec – / + ou en touchant la valeur pour la taper (« 45 », « 1:30 ») ;
  - **les répétitions ou la durée de chaque exercice**, et la charge en kg pour les exercices de salle ;
  - **les exercices** eux-mêmes : en ajouter, en retirer, changer l'ordre (↑ ↓).
- La durée estimée se met à jour à chaque réglage. Tes réglages d'un circuit sont retenus pour la prochaine fois (« réglé » sur la carte), et « Revenir au circuit d'origine » les annule. « Copier dans Mes circuits » en fait ton propre circuit, avec le nom que tu veux. « Créer un circuit » part de zéro.
- **Exercices** : les 33 exercices avec un schéma animé, filtrables par sport ou « sans matériel ». La fiche de chaque exercice donne les muscles travaillés, les étapes, le point clé et une version plus facile et plus dure. Touche un exercice dans un circuit pour voir sa fiche.
- **Minuteur guidé** (« Démarrer ») :
  - 10 s pour te mettre en place, puis l'enchaînement est automatique ;
  - le schéma animé de l'exercice, un grand chrono ou le nombre de répétitions, et le point clé ;
  - pendant la récup, l'exercice suivant et son schéma, avec « +15 s » si tu as besoin de plus ;
  - bips à 3-2-1, annonces vocales et vibrations ; les exercices d'un côté puis de l'autre ont un « Change de côté » de 5 s ;
  - Pause, Passer, et ⏮ pour refaire l'exercice précédent.
- À la fin, ou si tu t'arrêtes avant, ce qui a été fait s'enregistre dans le journal (exercices, séries, durée), puis tu notes ton ressenti. « Noter sans minuteur » remplit directement la saisie avec le circuit, à ajuster.
- Les séances de renfo du plan ouvrent le circuit correspondant, avec les mêmes réglages.

## Étirements

Dans **Séances → Étirements** (ou le bouton « Étirements » de l'accueil) :

- **Routines** par sport :
  - **Course** : « Mobilité avant la course » (balanciers de jambe, talons-fesses, montées de genoux, fentes bras au ciel) et « Après la course » (mollets, ischios, quadriceps, fléchisseurs de hanche, fessiers, côté de la hanche, adducteurs).
  - **Vélo** : « Après le vélo » (hanches, cuisses, dos, poitrine, nuque) et « Dos et nuque du cycliste ».
  - **Natation** : « Mobilité des épaules avant de nager » et « Après la natation » (épaules, triceps, pectoraux, grand dorsal, chevilles, nuque).
  - **Récupération** : « Récupération complète du triathlète » et « Détente du soir ».
- **Avant l'effort, seulement de la mobilité** : des mouvements doux et amples, jamais d'étirement tenu à froid. Les étirements tenus sont pour après.
- **Tout se règle** :
  - **Passages** : la routine une ou plusieurs fois, avec une pause entre deux passages.
  - **Tenue** : – / + ajoute ou retire 5 s à tous les étirements, et taper une valeur (« 45 ») les met tous à cette durée. Chaque étirement se règle aussi à part.
  - **Transition** : le temps pour changer de position.
  - **Les étirements** eux-mêmes : en ajouter, en retirer, changer l'ordre.
  - Tes réglages sont retenus. « Copier dans Mes routines » et « Créer une routine » te permettent de faire les tiennes.
- **Étirements** (deuxième onglet) : les 28 positions avec leur schéma animé, filtrables par sport, mobilité ou étirements tenus. Chaque fiche donne les muscles, les étapes, le point clé et une version plus douce et plus intense.
- **Minuteur guidé** : le schéma et le chrono de chaque position, « côté gauche » puis « côté droit » avec 5 s pour changer de côté, la position suivante pendant la transition, des bips à 3-2-1 et des annonces vocales.
- **Journal** : la routine s'enregistre comme une activité « Étirements » (positions et temps de tenue), avec une charge d'entraînement très faible pour ne pas fausser ta forme et ta fatigue. Elle a son filtre dans le journal, sa ligne dans « Cette semaine » et dans le bilan. Les séances de yoga et de mobilité importées (Garmin, intervals.icu, Strava) y sont aussi rangées.

## Plan : étirements et repères

**Étirements dans le plan** (réglage « Étirements dans le plan » à la création, ou les puces Complet · Léger · Aucun sous la vue d'ensemble d'un plan déjà créé, appliquées à partir d'aujourd'hui) :
- **Complet** :
  - « Mobilité des épaules » juste avant chaque séance de natation ;
  - « Mobilité avant la course » avant les séances clés et les sorties longues de course ;
  - « Après la course » après les sorties longues et les séances dures de course ;
  - « Après le vélo » après la sortie longue de vélo, et « Dos et nuque du cycliste » après les séances dures sur le KICKR (2 par semaine au plus) ;
  - « Récupération complète » après chaque enchaînement vélo-course ;
  - sur les jours sans séance, « Détente du soir » ou « Récupération complète » (3 jours en semaine de récupération) ;
  - le jour J, la mobilité du matin, 30 à 45 minutes avant le départ.
- **Léger** : après les sorties longues et les enchaînements, plus une routine détente par semaine.
- **Hors heures d'entraînement** : ils n'entrent pas dans les heures, la répartition des sports ni la charge. Dans chaque semaine, ils apparaissent à part (« +59 min d'étirements »), juste avant ou après la séance concernée.
- **Ils suivent leur séance** : si tu la déplaces, ils se déplacent avec elle ; si tu la retires, ils sont retirés aussi. « + Étirements après » ajoute une routine à n'importe quelle séance, et « Ajouter une séance » propose aussi les routines d'étirements.
- **Sur l'accueil**, l'étirement du jour a un bouton « Commencer » qui lance le minuteur guidé. Une fois la routine faite, elle est cochée dans le plan.

**Repères ajoutés au plan** :
- **Vue d'ensemble** : le volume prévu de chaque semaine par sport, coloré par phase. Un trait blanc montre ce que tu as réellement fait, la semaine en cours est encadrée et l'épreuve est marquée d'une étoile. Touche une barre pour ouvrir la semaine.
- **Chaque semaine** : son objectif (base, développement, spécifique, affûtage, récupération), ses séances clés, et les heures faites face aux heures prévues. Les séances clés, longues et de test sont marquées.
- **Alléger cette semaine** : en cas de fatigue ou de semaine chargée, les séances qui restent sont raccourcies de 30 % et les séances dures deviennent de l'endurance. Les tests et le renfo ne changent pas.
- **Compte à rebours** (J−75…) jusqu'à l'épreuve, et à 10 jours de la course, une **check-list de la semaine de course** à cocher : vélo, natation, tenue, nutrition (avec les glucides par heure selon la durée de course), parcours, transitions, sommeil, matin de course.
- Le suivi affiche aussi le pourcentage de séances passées réalisées et le nombre d'étirements faits.

## VTT, trail et cross triathlon

**Séances** :
- **Vélo → VTT** : 6 séances pour le KICKR, construites sur ce qui fait la différence en VTT. Il y a les relances depuis une cadence basse, les montées raides à 60 tr/min, le single-track en dents de scie, une simulation de course XC, la force en côte et l'endurance avec bosses. La « Surprise » vélo propose aussi « VTT ».
- **Course → Trail** : 7 séances au cardio (en côte, l'allure ne veut rien dire) : côtes longues, côtes courtes et raides, montées-descentes techniques, fartlek nature, rando-course (marche rapide en côte), escaliers et sortie longue trail. Elles s'envoient à la montre et se font aussi sur le tapis, qui règle la vitesse au cardio. La « Surprise » course propose « Trail » et « Sortie longue trail ».
- **Journal** : à la saisie, un vélo peut être « Route », « VTT » ou « Home trainer », et une course « Route », « Trail » ou « Tapis ». Les sorties VTT, trail et tapis importées (Garmin, intervals.icu, Strava) sont reconnues.

**Plans** (onglet Plan, trois familles) :
- **Triathlon**, avec les distances classiques et trois **cross triathlons** :
  - les distances : S (500 m, 10-15 km de VTT, 3-5 km de trail), M (1 km, 20-30 km, 6-10 km) et L / XTERRA (1,5 km, 30-40 km, 10-12 km) ;
  - côté vélo : sorties longues en VTT avec du dénivelé, une sortie technique VTT par semaine (virages, descentes, franchissements) et des séances VTT sur le KICKR ;
  - côté course : sorties longues en trail, côtes et descentes ;
  - les enchaînements deviennent des enchaînements VTT-trail.
- **Vélo** :
  - **Vélo de route** : cyclosportive, course sur route, critérium, contre-la-montre, montagne, gravel, FTP, forme.
  - **VTT** : XC / course de VTT, VTT marathon / raid, enduro / descente, randonnée VTT / forme. Les séances VTT sont sur le KICKR, avec une sortie longue VTT et une sortie technique dehors.
- **Course à pied** :
  - **Route** : 5 km, 10 km, semi-marathon, marathon, forme / reprise.
  - **Trail** : trail court (moins de 30 km), trail long (30-60 km), ultra-trail (plus de 60 km), forme / découverte. Tu peux indiquer le dénivelé de la course : les sorties longues indiquent un D+ à viser.
  - Le plan prend une sortie longue (jour au choix), une ou deux séances clés espacées, des footings et du renfo en base. Pour le trail long et l'ultra, il ajoute des « week-ends chocs » (une sortie la veille de la sortie longue), et deux semaines d'affûtage avant les longues distances.
  - Tests de VMA ou de seuil, étirements et check-list de course adaptée (matériel obligatoire en trail, dossard et allure sur route).
  - Le plan course est conçu par le moteur de l'app ; l'IA reste proposée pour le triathlon et le vélo, y compris le cross triathlon et le VTT.

## 1. Mise en ligne (une seule fois)

Chrome n'autorise le Bluetooth que sur une adresse https. Le plus simple est GitHub Pages (gratuit) :

1. Crée un compte sur [github.com](https://github.com).
2. Crée un dépôt public nommé `d6tri` (bouton **New repository**).
3. Touche **uploading an existing file** et ajoute les 7 fichiers du zip : `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`, `maskable-512.png`, `LISEZ-MOI.md`. Valide avec **Commit changes**.
4. **Settings → Pages** : choisis **Branch : main**, dossier **/ (root)**, puis **Save**.
5. Une minute plus tard, l'app est en ligne sur `https://TON-PSEUDO.github.io/d6tri/`.

Pour une mise à jour, remplace les fichiers du dépôt par ceux du nouveau zip (au minimum `index.html`, `sw.js` et `manifest.webmanifest`). Chrome met à jour le nom et l'icône de l'app installée de lui-même, en général sous un ou deux jours. Si tu veux le faire tout de suite : exporte d'abord une sauvegarde (Profil → Mes données), désinstalle l'app, réinstalle-la depuis Chrome, puis réimporte la sauvegarde si tes données n'y sont plus.

## 2. Installation sur le Pixel 6a

Ouvre l'adresse dans **Chrome**, puis menu ⋮ → **Installer l'application**. Autorise Chrome à utiliser les **Appareils à proximité** (Paramètres Android → Applications → Chrome → Autorisations).

Au premier lancement, renseigne tes repères (tu pourras les affiner avec les tests) :
- **FTP** vélo (ramp test intégré) ;
- **allure seuil** course, environ ton allure sur 10 km + 5 s/km (test 30 min intégré) ;
- **CSS** natation (test 400 m + 200 m, calcul automatique dans le profil) ;
- FC max, et ton niveau dans chaque sport.

## 3. Récupérer tes activités automatiquement (Garmin Connect)

Depuis octobre 2026, Garmin donne à chaque utilisateur une **clé API personnelle** gratuite, en lecture seule. L'app s'en sert pour importer toute seule les activités de ta Forerunner, avec les courbes (FC, allure, puissance), à chaque ouverture. Garmin ne répond pas aux appels venant directement d'une page web : il faut un petit **relais** gratuit sur Cloudflare, qui ne stocke rien et ne répond qu'à ton app.

1. Sur le site Garmin Connect, ouvre [la page Clé API personnelle](https://connect.garmin.com/app/settings/personalApiToken), crée une clé (durée : 1 an) et copie-la : elle ne s'affiche qu'une fois.
2. Crée un compte gratuit sur [Cloudflare](https://dash.cloudflare.com), puis **Workers & Pages** → **Create** → Worker « Hello World » → **Deploy**.
3. Dans l'app : Profil → Montre Garmin → **Copier le code du relais**. Sur Cloudflare, **Edit code**, remplace tout par ce code, puis **Deploy**. Note l'adresse du Worker (`…workers.dev`).
4. Dans l'app, colle l'adresse du relais et la clé, puis **Tester**.

Ensuite : synchro à chaque ouverture de l'app (au plus toutes les 15 minutes, jamais pendant une séance), bouton **Synchroniser** dans le Journal, et **Récupérer les 90 derniers jours** dans Importer. Un triathlon donne une activité par sport ; une activité que tu supprimes ne revient pas. Garmin t'envoie un e-mail une semaine avant l'expiration de la clé : crée-en une nouvelle et colle-la dans le profil.

**intervals.icu** (si tu l'as configuré pour la montre, voir plus bas) : l'app y lit aussi tes activités. C'est utile pour les **lunettes FORM**, qui envoient leurs nages à intervals.icu mais pas à Garmin. Les activités qu'intervals.icu a reçues de Strava ne sont pas lisibles par son API ; celles de Garmin le sont encore, mais intervals.icu prévoit de les couper. Les doublons entre Garmin et intervals.icu sont détectés (même sport, départ à moins de 3 minutes).

**Strava** : depuis le 30 juin 2026, son API est réservée aux abonnés Strava. Avec un abonnement, la connexion (Profil → Strava) marche toujours ; sans abonnement, utilise la synchro Garmin. Sans aucune connexion, l'import de fichiers .FIT/.zip exportés de Garmin Connect reste possible.

## 4. Séances sur la Forerunner 255 (intervals.icu)

Garmin ne laisse pas une app personnelle envoyer des séances sur la montre. On passe donc par **intervals.icu**, gratuit, qui les dépose dans ton calendrier Garmin Connect :

1. Crée un compte sur [intervals.icu](https://intervals.icu). Dans ses réglages, connecte Garmin Connect et coche **Upload planned workouts**.
2. Toujours dans ses réglages, section **Developer Settings**, génère une **clé API** et note ton **identifiant d'athlète** (i123456).
3. Dans l'app : Profil → intervals.icu, colle-les, puis **Tester la connexion**.
4. Sur une séance de course ou de natation : **Envoyer à ma montre**, ou depuis le plan : **Envoyer à la montre** (4 semaines d'un coup). Synchronise l'app Garmin Connect : la séance apparaît dans Entraînement → Séances sur la montre.

Choisis dans le profil si les cibles de course sont des **allures** ou des **zones de FC**. Sans intervals.icu, le bouton **Fichier .FIT (USB)** crée une séance à copier par câble dans le dossier `GARMIN/NewFiles` de la montre.

## 5. Lunettes FORM

- Tes nages remontent dans le journal via intervals.icu : dans l'app FORM, Réglages → Services externes → Intervals.icu, et laisse « Importer aussi mes activités d'intervals.icu » activé dans le profil.
- Pour nager une séance de l'app avec les lunettes, ouvre sa **Fiche piscine**. Dans l'app FORM, crée une séance à partir d'une photo et photographie la fiche. Autre solution : **Copier le texte** et le coller dans la description d'une séance TrainingPeaks (FORM importe les séances TrainingPeaks).

## 6. IA (facultatif)

Crée une clé sur [console.anthropic.com](https://console.anthropic.com/settings/keys) et colle-la dans Profil → Intelligence artificielle. Elle sert pour les plans triathlon conçus par Claude (avec tes précisions : piscine disponible, blessures, parcours…), la séance du jour selon ta fatigue, et l'analyse de chaque activité, nutrition comprise. L'usage est facturé par Anthropic, quelques centimes par plan. Sans clé, le moteur de plans intégré fonctionne.

## 7. Écrire tes séances

- **Vélo** (% de FTP) : `10m@45-70 "Échauffement", 4x(8m@95, 4m@55), 6m@60-40`. Options : `c90` pour la cadence, `free` pour le mode libre ; `m` veut dire minutes.
- **Course** : `15min@E, 6x(800m@I, 2min@trot), 10min@E`. Cibles : `trot`, `E`, `M`, `T`, `I`, `R`, `z1` à `z5` (FC), une allure `4:30`, ou une vitesse `10.5kmh` (avec un point, pas une virgule) ; `m` veut dire mètres et `min` minutes.
- **Natation** : `400m@souple, 8x(100m@css r15s), 200m@souple`. Cibles : `educ`, `souple`, `end`, `tempo`, `css`, `css+3`, `vite`, `sprint`. `r15s` = 15 s de repos après chaque répétition.

## 8. À savoir

- Une seule application à la fois peut piloter le KICKR : ferme Zwift ou l'app Wahoo avant.
- Les valeurs des produits de nutrition sont des moyennes : adapte-les à tes marques dans le profil.
- Les repères de glucides affichés (30 à 60 g/h de 1 à 2 h d'effort, jusqu'à 60 à 90 g/h au-delà de 2 h 30) sont des recommandations générales, pas un avis médical.
- Tout est stocké sur ton téléphone. Pense à exporter une sauvegarde (Profil → Mes données).
- Le mode démo (Accueil → Home trainer) simule un KICKR et une ceinture cardio pour tout essayer.
