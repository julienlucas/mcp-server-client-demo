# Weather MCP Server

Un serveur MCP (Model Context Protocol) qui fournit des informations météorologiques via l'API National Weather Service (NWS).

## Fonctionnalités

- Récupération des alertes météorologiques par état
- Prévisions météorologiques par coordonnées géographiques
- Support des formats GeoJSON
- Interface TypeScript pour une meilleure maintenabilité

## Prérequis

- Node.js (v16 ou supérieur)
- npm ou yarn
- TypeScript
- ts-node (pour l'exécution en développement)

## Installation

1. Clonez le dépôt :
```bash
git clone [URL_DU_REPO]
cd weather
```

2. Installez les dépendances :
```bash
npm install
```

3. Compilez le projet :
```bash
npm run build
```

## Configuration

Le serveur est configuré pour se connecter à l'API NWS. Aucune configuration supplémentaire n'est nécessaire.

## Utilisation

Le serveur expose deux outils principaux :

1. `get-alerts` : Récupère les alertes météorologiques pour un état
   - Paramètre : `state` (code à deux lettres, ex: "CA", "NY")

2. `get-forecast` : Récupère les prévisions météorologiques pour une localisation
   - Paramètres :
     - `latitude` (nombre entre -90 et 90)
     - `longitude` (nombre entre -180 et 180)

## Structure du Projet

```
weather/
├── src/
│   ├── interfaces/     # Définitions des types TypeScript
│   │   └── weather.ts  # Interfaces pour les données météo
│   └── index.ts        # Point d'entrée du serveur
├── build/              # Fichiers compilés
└── package.json        # Configuration du projet
```

## Développement

Pour lancer le serveur en mode développement :
```bash
npm run dev
```

Pour compiler le projet :
```bash
npm run build
```

## Licence

MIT