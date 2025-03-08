# 🏠 [HomeIO](https://realgames.co/home-io) WebServer

Simple panneau de contrôle web pour le simulateur Home IO de RealGames, offrant une interface propre et intuitive pour gérer divers systèmes d'automatisation domestique, notamment les lumières, les volets et la porte de garage.

## 🎮 À propos du Simulateur Home IO

Ce projet est conçu pour fonctionner avec le [simulateur Home IO](https://realgames.co/home-io) de RealGames, un logiciel professionnel de simulation d'automatisation domestique. Le simulateur fournit un environnement réaliste pour tester et développer des solutions d'automatisation domestique.

> 📚 Une documentation officielle complète est disponible en anglais : [Documentation Home IO Web Server](https://docs.realgames.co/homeio/en/downloads/homeio-web-server_en.pdf)

## ✨ Fonctionnalités

- **💡 Contrôle des Lumières**
  - Contrôle individuel des lumières par pièce (Piscine, Entrée)
  - Contrôle groupé des lumières pour plusieurs pièces (Salon, WC, Cuisine, Couloir)
  - Retour visuel avec indicateurs d'état allumé/éteint

- **🪟 Contrôle des Volets**
  - Contrôle des volets pour plusieurs pièces
  - Trois modes : Monter, Descendre et Arrêter
  - Sélection des pièces via menus déroulants

- **🚗 Contrôle de la Porte de Garage**
  - Fonctionnalité d'ouverture/fermeture de la porte de garage
  - Fonction d'arrêt

## 🛠️ Technologies Utilisées

- HTML5
- CSS3
- JavaScript (Vanilla)
- Intégration API du Simulateur Home IO

## 📁 Structure du Projet

```
HomeIO WebServer/
├── assets/
│   ├── fonts/
│   │   └── roboto_mono.css
│   └── icons/
│       ├── logo.png
│       ├── light_icon_on.png
│       ├── light_icon_off.png
│       ├── volets_icon.png
│       ├── garage_icon.png
│       └── en-arriere.png
├── css/
│   └── style.css
├── index.html
├── lumieres.html
├── volets.html
└── garage.html
```

## 🔌 Points d'Accès API du Simulateur Home IO

L'application communique avec le simulateur Home IO fonctionnant sur le port 9797 :

### 💡 Contrôle des Lumières
- `http://localhost:9797/stsw/allumer/{target}` - Allumer une lumière spécifique
  - Exemple : `lumière_piscine`, `lumière_entrée`
- `http://localhost:9797/stsw/eteindre/{target}` - Éteindre une lumière spécifique
- `http://localhost:9797/swl/{command}/{number}/{room}` - Contrôler les lumières groupées
  - Exemple : `allumer/1/A` pour la pièce A, lumière 1

### 🪟 Contrôle des Volets
- `http://localhost:9797/strs/{command}/{number}/{room}` - Contrôler les volets
  - Commandes : monter, descendre, stopper
  - Numéro : 1-5 (numéro du volet)
  - Pièce : A-M (identifiant de la pièce)

### 🚗 Contrôle de la Porte de Garage
- `http://localhost:9797/cgate/ouvrir/porte_garage` - Ouvrir la porte de garage
- `http://localhost:9797/cgate/fermer/porte_garage` - Fermer la porte de garage
- `http://localhost:9797/cgate/stopper/porte_garage` - Arrêter la porte de garage

## 🚀 Installation

1. Installez le [simulateur Home IO](https://www.realgames.pt/software/home-io/) de RealGames

2. Clonez ce dépôt :
```bash
git clone https://github.com/1Developpeur/HomeIO-WebServer.git
```

3. Accédez au répertoire du projet :
```bash
cd HomeIO-WebServer
```

4. Ouvrez `index.html` dans votre navigateur web ou servez-le à l'aide d'un serveur web local.

## 🤝 Contribution

Les contributions sont les bienvenues !

## 📄 Licence

Ce projet est sous licence MIT
