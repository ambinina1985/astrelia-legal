# Astrelia — documents légaux

Site statique contenant les documents légaux de l'application Astrelia, en français et en anglais :

| Page | Contenu |
|---|---|
| `confidentialite.html` | Politique de confidentialité (FR) |
| `conditions.html` | Conditions d'utilisation (FR) |
| `privacy.html` | Privacy Policy (EN) |
| `terms.html` | Terms of Use (EN) |
| `assistance.html` | Assistance et questions fréquentes (FR) |
| `support.html` | Support & FAQ (EN) |
| `index.html` | Page d'accueil reliant les documents |

## Avant publication

1. Éditeur et contact renseignés comme pour Atlas (Ambinina Andriamboavonjy, ambinina@gmail.com) ; à adapter si besoin. Si vous exercez à titre professionnel, nommer votre médiateur de la consommation dans `conditions.html`.
2. Faire relire les textes par un juriste : ils décrivent fidèlement le fonctionnement de l'app (aucun compte, aucun serveur, données sur l'appareil, iCloud facultatif, achats Apple) mais ne remplacent pas un avis juridique.
3. Mettre à jour ces documents si l'app évolue (compte en ligne, statistiques, serveur IA…).

## Publier gratuitement avec GitHub Pages

```bash
gh repo create astrelia-legal --public --source=. --push
gh api -X POST repos/{owner}/astrelia-legal/pages -f "source[branch]=main" -f "source[path]=/"
```

Les pages seront disponibles à `https://<compte>.github.io/astrelia-legal/`.

## Brancher l'app

Dans `Astrelia/Resources/Config.plist` de l'app :

- `PRIVACY_URL` → `https://<compte>.github.io/astrelia-legal/confidentialite.html`
- `TERMS_URL` → `https://<compte>.github.io/astrelia-legal/conditions.html`

Renseigner aussi l'URL de confidentialité dans App Store Connect (obligatoire).
