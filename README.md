# MyZodia — documents légaux

Site statique contenant les documents légaux de l'application MyZodia, en français et en anglais :

| Page | Contenu |
|---|---|
| `confidentialite.html` | Politique de confidentialité (FR) |
| `conditions.html` | Conditions d'utilisation (FR) |
| `privacy.html` | Privacy Policy (EN) |
| `terms.html` | Terms of Use (EN) |
| `index.html` | Page d'accueil reliant les quatre documents |

## Avant publication

1. Compléter les zones surlignées `[…]` : nom de l'éditeur, adresse, e-mail de contact, date, droit applicable, médiateur de la consommation.
2. Faire relire les textes par un juriste : ils décrivent fidèlement le fonctionnement de l'app (aucun compte, aucun serveur, données sur l'appareil, iCloud facultatif, achats Apple) mais ne remplacent pas un avis juridique.
3. Mettre à jour ces documents si l'app évolue (compte en ligne, statistiques, serveur IA…).

## Publier gratuitement avec GitHub Pages

```bash
gh repo create myzodia-legal --public --source=. --push
gh api -X POST repos/{owner}/myzodia-legal/pages -f "source[branch]=main" -f "source[path]=/"
```

Les pages seront disponibles à `https://<compte>.github.io/myzodia-legal/`.

## Brancher l'app

Dans `MyZodia/Resources/Config.plist` de l'app :

- `PRIVACY_URL` → `https://<compte>.github.io/myzodia-legal/confidentialite.html`
- `TERMS_URL` → `https://<compte>.github.io/myzodia-legal/conditions.html`

Renseigner aussi l'URL de confidentialité dans App Store Connect (obligatoire).
