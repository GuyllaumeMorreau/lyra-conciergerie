# Lyra — Conciergerie privée internationale

Site vitrine statique une page (anciennement ELYONE). Direction artistique construite autour du logo bordeaux : ivoire et bordeaux dominants, noir pour les images, or champagne réservé aux accents.

## Structure

- `index.html` — le site complet (HTML, CSS et JS inline)
- `assets/brand/` — logo détouré depuis la version bordeaux fournie :
  - `lyra-lockup.png` — logo complet (fonds sombres)
  - `lyra-lockup-bordeaux.png` — logo complet monochrome (fonds clairs)
  - `lyra-mark.png` / `lyra-mark-bordeaux.png` — constellation seule (header, fonds sombres / clairs)
- `assets/lyra/` — photos éditoriales (Unsplash, licence libre)

## Direction artistique

| Rôle | Valeur |
| --- | --- |
| Bordeaux (fond du logo) | `#43030A` |
| Ivoire | `#F5F0E8` |
| Noir | `#0D0A0A` |
| Or champagne (accent uniquement) | `#D2AD84` |

Typographies Google Fonts : **Cormorant Garamond** Light (titres, proche du « Lyra » du logo) et **Jost** (texte, proche de « CONCIERGERIE »).

## À personnaliser avant mise en ligne

1. **Email de réception** : remplacer `concierge@lyra-conciergerie.com` (constante `CONCIERGE_EMAIL` du script et lien du footer).
2. **Formulaire** : le bouton ouvre l'app mail du visiteur avec la demande pré-remplie (`mailto:`). Pour une réception sans app mail, brancher Formspree ou un petit backend dans le handler `submit`.
3. **Logo** : les PNG sont détourés depuis une capture d'écran (474 px de large). Les remplacer par le fichier source vectoriel (SVG) dès qu'il est disponible, pour une netteté parfaite.
4. **Photos** : remplacer à terme par des visuels propriétaires (mêmes noms de fichiers dans `assets/lyra/`).
5. **Domaine** : déployable tel quel sur n'importe quel hébergement statique (Nginx, Netlify, GitHub Pages…).

## Développement

```bash
python3 -m http.server 8479   # puis http://localhost:8479
```
