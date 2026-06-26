# Opex House — Site web

Landing page statique, prête pour GitHub Pages.

## Déploiement GitHub Pages

1. Créez un repo GitHub (ex: `opexhouse-site`)
2. Déposez `index.html` à la racine
3. Settings → Pages → Source : `main` branch, dossier `/root`
4. Votre site sera accessible sur `https://votre-user.github.io/opexhouse-site`

## Brancher votre domaine

Dans Settings → Pages → Custom domain :
1. Entrez votre domaine (ex: `opexhouse.ca`)
2. Chez votre registraire DNS, ajoutez :
   - Type `A` → `185.199.108.153`
   - Type `A` → `185.199.109.153`
   - Type `A` → `185.199.110.153`
   - Type `A` → `185.199.111.153`
   - Type `CNAME` → `www` → `votre-user.github.io`
3. Attendez 10–30 min pour la propagation DNS

## Personnalisation

- **Courriel** : remplacer `bonjour@opexhouse.ca` (ligne ~400)
- **LinkedIn** : remplacer l'URL du profil LinkedIn (ligne ~430)
- **Adresse** : ajuster si vous avez une adresse précise
- **Formulaire** : le formulaire est actuellement en mode démo. Pour recevoir les soumissions, connectez un service comme [Formspree](https://formspree.io) ou [Netlify Forms](https://docs.netlify.com/forms/setup/).

## Formspree (recommandé — gratuit)

1. Créez un compte sur formspree.io
2. Créez un nouveau formulaire → copiez l'ID
3. Dans index.html, remplacez `<form ... onsubmit="handleSubmit(event)">` par :
   `<form action="https://formspree.io/f/VOTRE_ID" method="POST">`
4. Supprimez la fonction `handleSubmit` en bas du fichier

