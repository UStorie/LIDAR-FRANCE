# LiDAR France

Application web statique de consultation du relief **LiDAR HD — MNT ombrage** de l'IGN, avec fond Esri World Imagery.

## Fonctions
- Carte plein écran (Leaflet) et relief LiDAR HD IGN (WMTS Géoplateforme)
- Recherche de localités en France (Nominatim/OpenStreetMap)
- Géolocalisation facultative (autorisation navigateur)
- Ajout/suppression de marqueurs conservés localement dans le navigateur
- Curseur d'opacité LiDAR 0 à 100 % révélant l'imagerie aérienne
- Interface adaptée aux écrans mobiles

## Mise en ligne gratuite

1. Créez un dépôt GitHub public, par exemple `lidar-france`.
2. Copiez `index.html`, `favicon.svg` et `.nojekyll` **à la racine** du dépôt.
3. Ouvrez **Settings → Pages → Build and deployment** et choisissez **Deploy from a branch**, branche `main`, dossier `/(root)`.
4. Le site sera accessible à `https://VOTRE-PSEUDO.github.io/lidar-france/`.

Aucun serveur ni compilation requis. Ouvrez également `index.html` localement dans un navigateur pour tester (certaines protections navigateur peuvent être plus strictes en `file://`).

## Services et mentions
- IGN Géoplateforme, ombrage MNT LiDAR HD : `https://data.geopf.fr/wmts`
- Fond photographique Esri World Imagery (les conditions Esri peuvent évoluer) : `https://server.arcgisonline.com/ArcGIS/rest/services/World_Imagery/MapServer/tile/`
- Géocodage : Nominatim OpenStreetMap public. L'usage est soumis à sa politique de service, notamment des limites de débit ; pour un trafic important, utiliser un service de géocodage dédié.
- Bibliothèque cartographique Leaflet chargée depuis un CDN ; fonctionnement avec accès Internet requis.
- Les marqueurs sont stockés dans `localStorage` (ils ne sont ni synchronisés ni sauvegardés sur un serveur).

Cette application est une **reconstruction indépendante à partir d'une capture de l'interface**, pas une extraction du code Base44. Les services tiers sont susceptibles d'être temporairement indisponibles et certaines zones n'ont pas encore de couverture LiDAR.