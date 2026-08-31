# ELYONE — Conciergerie privée internationale

Site vitrine statique une page. Identité : noir profond, ivoire, or champagne, d'après le logo ELYONE (couronne filaire + serif classique).

## Structure

- `index.html` — le site complet (HTML + CSS + JS inline, images dans `assets/img/`)
- `assets/img/` — photos (Unsplash, licence libre ; à remplacer à terme par des visuels de marque)
- `publish.html` — version générée avec images en base64 pour l'aperçu Artifact (ne pas éditer)

## Typographies

Google Fonts : **Cinzel** (titres, wordmark — proche du logo) et **Jost** (corps, labels — géométrique façon Futura).

## À personnaliser avant mise en ligne

1. **Email de réception** : remplacer `concierge@elyone.com` (2 occurrences dans `index.html` : le footer et le script du formulaire).
2. **Formulaire** : actuellement le bouton ouvre l'app mail du visiteur avec la demande pré-remplie (`mailto:`). Pour une réception serveur sans app mail, brancher Formspree/Basin ou un petit backend, et remplacer le handler `submit`.
3. **Photos** : les visuels Unsplash sont libres d'usage commercial ; remplacer par des photos propriétaires quand disponibles (mêmes noms de fichiers dans `assets/img/`).
4. **Domaine** : déployable tel quel sur n'importe quel hébergement statique (Nginx, Netlify, GitHub Pages…).

## Développement

```bash
python3 -m http.server 8479   # puis http://localhost:8479
```

Régénérer `publish.html` après modification d'`index.html` : le script inline simplement les images en data URI (voir historique de session ou refaire à la main).
