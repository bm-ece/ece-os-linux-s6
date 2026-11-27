# ECE — Operating Systems: Linux

Site pédagogique ING3, semestre 6 (2026–2027).

## Contenu

- Accueil (`public/index.html`)
- Syllabus A4 (`public/syllabus.html`)
- Poster A3 (`public/poster.html`)
- Planning A3 (`public/planning.html`)
- Simulateur exploratoire (`public/simulateur.html`)

Les fichiers HTML/CSS/JS sont statiques ; aucun build n'est nécessaire.

## Déploiement automatique sur Cloudflare Workers

Ce dépôt est destiné au Worker existant **ece-os-linux-s6** :
https://ece-os-linux-s6.baligh-mn.workers.dev

1. Cloudflare > Workers & Pages > **ece-os-linux-s6**.
2. **Settings > Builds > Connect** puis autoriser le dépôt `bm-ece/ece-os-linux-s6`.
3. Branche de production : **main**.
4. Répertoire racine : `/`.
5. Build command : **aucune**.
6. Deploy command : **`npx wrangler deploy`**.

La configuration `wrangler.jsonc` pointe vers `./public`.
Les push sur `main` déclenchent un déploiement après connexion dans Cloudflare.

## Mise à jour

Modifier les fichiers dans `public/`, tester, puis intégrer les changements dans `main`.
Les branches de préparation peuvent servir aux relectures avant publication.
Le simulateur et son option de plafonnement sont exploratoires et ne font pas
partie des modalités officielles d'évaluation.

> Attention : le site publié est public. Vérifier les droits de diffusion des images et documents.
