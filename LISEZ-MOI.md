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
- **Course** : `15min@E, 6x(800m@I, 2min@trot), 10min@E`. Cibles : `trot`, `E`, `M`, `T`, `I`, `R`, `z1` à `z5` (FC), ou une allure `4:30` ; `m` veut dire mètres et `min` minutes.
- **Natation** : `400m@souple, 8x(100m@css r15s), 200m@souple`. Cibles : `educ`, `souple`, `end`, `tempo`, `css`, `css+3`, `vite`, `sprint`. `r15s` = 15 s de repos après chaque répétition.

## 8. À savoir

- Une seule application à la fois peut piloter le KICKR : ferme Zwift ou l'app Wahoo avant.
- Les valeurs des produits de nutrition sont des moyennes : adapte-les à tes marques dans le profil.
- Les repères de glucides affichés (30 à 60 g/h de 1 à 2 h d'effort, jusqu'à 60 à 90 g/h au-delà de 2 h 30) sont des recommandations générales, pas un avis médical.
- Tout est stocké sur ton téléphone. Pense à exporter une sauvegarde (Profil → Mes données).
- Le mode démo (Accueil → Home trainer) simule un KICKR et une ceinture cardio pour tout essayer.
