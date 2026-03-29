# Mode d’emploi – TRIAL DES PATATES

## 0. Cahier des charges

- **Objectif**  
  Créer un album souvenir web d’une journée de trial moto familiale, consultable depuis le NAS, sans backend ni base de données.

- **Contraintes techniques**  
  - Une seule page HTML autonome. 
  - Hébergement sur NAS (openmediavault) 
  - Tous les médias (images, vidéos) placés dans **le même dossier** que le fichier HTML.  
  - Fonctionne hors-ligne sur un navigateur moderne (Chrome, Edge, Firefox, Safari).  
  - Pas de dépendance externe (pas de CDN, pas de framework).
  - les photos sont renommées de F1 à F.. pour gérer l'ordre d'affichage
  - les vidéos sont renommées de v1 à v.. pour gérer l'ordre d'affichage

- **Fonctionnalités**  
  - Titre : **« TRIAL DES PATATES »**.  
  - Description : organisation d’un trial pour les cousins.  
  - Affichage du chef d’orchestre (Daniel et Alain) 
  - Affichage des participants: Agathe, Océane, Mathias, Antonin, Estabane, Côme 
  - Section **Paddock & Circuit** avec 2 vignettes (paddock + circuit).  
  - Section **Remise des trophées** avec 6 trophées illustrés.  
  - Galerie **photos** : grand format 
  - Galerie **vidéos** : idem.  
  - Section finale **vidéo Top Pilote** lue depuis un fichier local.  
  - Avatars par participant, affichés dans une popup au clic sur les badges.

- **Charte graphique**  
  - Thème moto trial, ambiance terrain / forêt.  
  - Couleurs adoucies (terracotta, ambre, bleu nuit).  
  - Animations légères (glow, bounce, slide).  
  - Motos de trial stylisées en SVG dans le header.  
  - Design responsive (mobile + desktop).

- **Trophées**  
  1. Le Plus Rapide  = Antonin
  2. Le Plus Technique = Estebane
  3. Le Plus Trial  = Côme
  4. Le Plus Casse-Cou = Mathias
  5. La Plus Enduro = Agathe
  6. La Plus Stylée = Océane

---

## 1. Préparer les fichiers

Placer dans le **même dossier** :

- `trial_des_patates.html`

**Sponsors :**

- `sponsor1.jpg` – bannière Dherbey fond bleu  
- `sponsor2.jpg` – bannière Dherbey fond blanc  

**Paddock & circuit :**

- `paddock.MOV` – vidéo du paddock  
- `circuit.jpg` – vidéo du circuit / des zones  réalisé à pied par Méline
**Galerie photos**
- les photos à utiliser sont codifiées p1.jpg à px.jpg
**galerie vidéo**
- les vidéos à utiliser sont codifiées v1.mp4 à vx.mp4

**Trophées (photos pilotes) :**

- `1.jpg` – Le Plus Rapide  
- `2.jpg` – Le Plus Technique  
- `3.jpg` – Le Plus Trial (Côme)  
- `4.jpg` – Le Plus Casse-Cou  
- `5.jpg` – Le Plus Enduro  
- `6.jpg` – La Plus Stylée  

**Avatars des participants (popups) :**

- `mathias.jpg`  
- `agathe.jpg`  
- `antonin.jpg`  
- `oceane.jpg`  
- `estebane.jpg`  
- `come.jpg`  

**Vidéo Top Pilote :**

- `toppilote.mp4`  


Les noms de fichiers doivent être **exactement identiques** (minuscules, sans accents dans les noms de fichiers).

---

## 2. Ouvrir la page

### 2.1. Sur un PC

1. Copier le dossier complet sur le PC.  
2. Double-cliquer sur `trial_des_patates.html`.  
3. Le navigateur s’ouvre et affiche la page.

### 2.2. Depuis le NAS

1. Copier le dossier dans le répertoire web du NAS (ou un partage publié via un petit serveur web).  
2. Depuis un navigateur du réseau local, ouvrir :  
   - `http://IP_DU_NAS/trial_des_patates.html`  
3. Partager cette URL à la famille.

---

## 3. Ce que contient la page

- **Header**  
  - Titre « TRIAL DES PATATES ».  
  - Sous-titre : organisation du trial pour les cousins.  
  - Deux motos de trial (SVG) animées en fond.

- **Barre sponsors**  
  - Affiche `sponsor1.jpg` et `sponsor2.jpg` si présents.

**Lieu de l'événement**
- utiliser les images zoom_1.jpeg à zoom_120.jpeg pour réaliser une animation du zoom synchronisé sur le scroll

**Section Infos**  
  - Carte « Chef d’orchestre » : Daniel et Alain.  Affiche `daniel.jpg` et `alain.jpg` si présent
  - Carte « Participants » avec les badges prénoms.Ajoute les images par exemple pour come = come.jpg etc...

- **Section Paddock & Circuit**  
  - Deux vignettes 16/9 : `paddock.MOV` (paddock) et `circuit.MOV` (circuit).  

- **Galerie Photos** 
- format grand 
- **Galerie Vidéos**  
- format grand
- **Section Remise des Trophées** 
- 2 lignes de 3 = (6 cartes)  
- **Section Vidéo Top Pilote**

---

## 4. Remise des trophées

Correspondance fichiers / trophées :  

| Fichier    | Trophée              |
|-----------|----------------------|
| `1.jpg`   | Le Plus Rapide       |
| `2.jpg`   | Le Plus Technique    |
| `3.jpg`   | Le Plus Trial        |
| `4.jpg`   | Le Plus Casse-Cou    |
| `5.jpg`   | Le Plus Enduro       |
| `6.jpg`   | La Plus Stylée       |

- Chaque carte affiche : avatar circulaire, emoji, titre du trophée, texte court.  
- Si une image manque, un **avatar moto trial** s’affiche.
- pour dévoiler l'avatar il faut cliquer sur la carte, elle tourne sur elle même deux fois avant

---

## 7. Avatars des participants (popup)

Dans la section **Participants** :

- Chaque badge de prénom est **cliquable**.  
- Clic sur un badge → ouverture d’une **fenêtre modale** avec :
  - l’avatar `prenom.jpg`,  
  - le prénom en gros,  
  - une phrase de description.

**Fermer la popup :**

- en cliquant à côté de la boîte,  
- ou sur la croix **×**,  
- ou avec la touche **Échap**.

---

## 8. Vidéo Top Pilote

En bas de page, section **« Le Top Pilote du Jour »** :

- Lecteur vidéo HTML5.  
- Lit le fichier `toppilote.mp4`  

## 9. Mise à jour suite lenteur lié au débit montant

- chargement des vidéos sur youtube en non répertoriée
`paddock` = https://youtu.be/VyqNkPWHwyM
`circuit` = https://youtu.be/Wr0XCWyB29o
`v1`= https://youtu.be/RfDTA9SbQN8
`v2`= https://youtu.be/c3tNiSCPX-8
`v3`= https://youtu.be/QFZCFVf6kyE
`v4`= https://youtu.be/cpGqTCjj35c
`v5`= à venir
`v6`= à venir
`v7`= à venir
`v8`= à venir
`v8`= à venir
`toppilote` = https://youtu.be/BHvYc0XE6uE