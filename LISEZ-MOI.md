# D Tri Training

Ton application de triathlon sur téléphone Android : journal de toutes tes activités, séances de natation, vélo et course, renfo, poids, nutrition, ressenti, plans d'entraînement et bilans mensuels. Le vélo se pilote en direct sur ton home trainer Wahoo KICKR.

## Ce que fait l'app

- **Journal** : toutes tes activités au même endroit. Tu peux les saisir à la main, les importer depuis Strava (où arrivent déjà ta Forerunner 255 et tes lunettes FORM), ou depuis des fichiers .FIT/.zip exportés de Garmin Connect. Un fichier de triathlon donne une activité par sport.
- **Vélo** : tes séances KICKR en mode ERG (l'app règle la puissance), avec 55 séances prêtes (dont des séances de cadence et de vélocité), des séances surprise et le ramp test. Envoi direct sur Strava ; fichier .FIT pour Garmin Connect.
- **Course** : 23 séances (footing, sortie longue, seuil, VMA, côtes, enchaînements, tests) et des séances surprise. Les cibles sont des allures calculées sur ton allure seuil, ou des zones de fréquence cardiaque. Chaque séance s'envoie sur ta montre.
- **Séances à la durée de ton choix** : sur chaque séance (vélo, course, natation), choisis le temps dont tu disposes (20 à 120 min). L'app recalcule la séance : nombre de répétitions, durée des blocs, échauffement et retour au calme. Une 30/30 VMA de 55 min devient ainsi 10 × 30/30 en 30 min. Dans Séances, le réglage « Temps dont je dispose » adapte toute la liste d'un coup. Les tests gardent leur durée.
- **Natation** : 15 séances (technique, endurance, CSS, vitesse, eau libre, test CSS) calculées sur ta CSS. Chaque séance a une « fiche piscine » à lire au bord du bassin ou à photographier pour les lunettes FORM.
- **Renfo** : saisie des exercices, séries, répétitions, durées et charges (pompes, tractions, dips, gainage, squats… ou tes propres exercices), avec des modèles tout prêts.
- **Ressenti et nutrition** : après chaque activité, tu notes l'effort perçu, tes sensations et des repères (fringale, crampes…), puis ce que tu as mangé et bu (gels, bidons, barres…). L'app calcule glucides par heure, liquides et sodium, compare aux repères usuels selon la durée, et fait le lien entre nutrition et sensations sur tes séances longues.
- **Poids** : suivi des pesées avec tendance sur 7 jours.
- **Plan** : plan triathlon S, M, L (70.3) ou XL (Ironman), ou vélo seul. Il tient compte de ta date de course, tes jours libres, tes heures, ton niveau dans chaque sport et ton sport faible. Au programme : périodisation, semaines allégées, enchaînements vélo-course, renfo, tests et affûtage. Tu peux déplacer, changer, ajouter ou retirer des séances, en vue semaine ou mois. Version IA (Claude) en option.
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

## 3. Récupérer toutes tes activités (Strava)

1. Sur [strava.com/settings/api](https://www.strava.com/settings/api), crée une application. Dans **Authorization Callback Domain**, mets `TON-PSEUDO.github.io`.
2. Dans l'app : Profil → Strava, colle le **Client ID** et le **Client Secret**, puis **Connecter Strava**. Accepte la lecture et l'envoi d'activités.
3. Journal → **Strava** : l'app récupère tes 90 derniers jours, puis seulement les nouveautés.

Vérifie que l'app FORM partage bien tes nages vers Strava, et que Garmin Connect est relié à Strava.

## 4. Séances sur la Forerunner 255 (intervals.icu)

Garmin ne laisse pas une app personnelle envoyer des séances sur la montre. On passe donc par **intervals.icu**, gratuit, qui les dépose dans ton calendrier Garmin Connect :

1. Crée un compte sur [intervals.icu](https://intervals.icu). Dans ses réglages, connecte Garmin Connect et coche **Upload planned workouts**.
2. Toujours dans ses réglages, section **Developer Settings**, génère une **clé API** et note ton **identifiant d'athlète** (i123456).
3. Dans l'app : Profil → Montre Garmin, colle-les, puis **Tester la connexion**.
4. Sur une séance de course ou de natation : **Envoyer à ma montre**, ou depuis le plan : **Envoyer à la montre** (4 semaines d'un coup). Synchronise l'app Garmin Connect : la séance apparaît dans Entraînement → Séances sur la montre.

Choisis dans le profil si les cibles de course sont des **allures** ou des **zones de FC**. Sans intervals.icu, le bouton **Fichier .FIT (USB)** crée une séance à copier par câble dans le dossier `GARMIN/NewFiles` de la montre.

## 5. Lunettes FORM

- Tes nages remontent dans le journal via Strava.
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
