# Manger mieux — prototype PWA

Application web progressive en français pour iPhone :
- composition de plats et calcul automatique kcal/protéines/glucides/lipides/fibres ;
- quantités par ingrédient et portions ;
- recettes et aliments sauvegardés dans le stockage local du navigateur ;
- recherche produits et lecture de codes-barres via Open Food Facts ;
- scan caméra via html5-qrcode chargé depuis un CDN ;
- création et modification d’aliments.

## Lancer pour tester
Le plus simple est d’héberger ces fichiers sur un hébergement statique HTTPS (par exemple GitHub Pages, Netlify ou Vercel). La caméra mobile requiert HTTPS, sauf localhost. Ouvrir `index.html` directement depuis Fichiers peut ne pas autoriser la caméra ni le service worker.

## Installer sur iPhone
1. Publier le dossier sur un hébergement HTTPS.
2. Ouvrir l’adresse dans Safari sur l’iPhone.
3. Appuyer sur Partager > Sur l’écran d’accueil > Ajouter.
4. Ouvrir l’icône depuis l’écran d’accueil.

## Limites de cette première version
- Les données sont sauvegardées dans le navigateur de cet appareil ; elles ne sont pas synchronisées entre appareils.
- Les valeurs des aliments de base sont des valeurs indicatives de départ, pas une importation complète de Ciqual.
- Les produits Open Food Facts peuvent avoir des données manquantes ou erronées : vérifier l’étiquette et corriger si besoin.
- Le scan requiert une connexion pour rechercher un produit dans Open Food Facts. La saisie manuelle du code est disponible en secours.
- L’application n’est pas publiée sur l’App Store. Une publication native demanderait une étape de développement supplémentaire.

## Structure
- `index.html` : application et interface
- `manifest.webmanifest` : configuration installable
- `sw.js` : cache hors-ligne de l’interface
- `icon.svg` : icône
