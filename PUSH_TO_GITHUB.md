# Instructions pour pousser vers GitHub

## État actuel
✅ Tous les fichiers sont prêts
✅ 10 commits locaux prêts à être poussés
✅ Remote GitHub configuré : `git@github.com:knoery-saas/piscines-site.git`

## Solution rapide (1 commande)

Ouvrez votre terminal dans ce dossier et exécutez :

```bash
cd "/Users/knoery/Library/Mobile Documents/com~apple~CloudDocs/piscines"
git push -u origin main
```

Si cela demande une authentification, utilisez l'une des options ci-dessous.

## Option 1 : Utiliser GitHub CLI (Recommandé)

```bash
# Installer GitHub CLI
brew install gh

# S'authentifier
gh auth login

# Pousser le code
git push -u origin main
```

## Option 2 : Utiliser un Personal Access Token

1. Allez sur https://github.com/settings/tokens
2. Cliquez sur "Generate new token" → "Generate new token (classic)"
3. Donnez un nom : "piscines-site"
4. Cochez `repo` (accès complet)
5. Cliquez "Generate token"
6. Copiez le token

Ensuite, utilisez le token comme mot de passe quand Git le demande :
```bash
git push -u origin main
# Username: knoery-saas
# Password: [collez votre token ici]
```

## Option 3 : Configurer SSH (si vous avez déjà une clé)

1. Vérifiez votre clé SSH :
```bash
cat ~/.ssh/id_ed25519.pub
```

2. Ajoutez cette clé sur GitHub :
   - Allez sur https://github.com/settings/keys
   - Cliquez "New SSH key"
   - Collez le contenu de votre clé publique
   - Cliquez "Add SSH key"

3. Poussez :
```bash
git push -u origin main
```

## Contenu qui sera poussé

- ✅ index.html (avec toutes les fonctionnalités)
- ✅ assets/ (toutes les images)
- ✅ vercel.json (configuration)
- ✅ package.json
- ✅ README.md
- ✅ 10 commits avec toutes les fonctionnalités :
  - Bulles animées, confettis
  - Validation détaillée
  - EmailJS configuré
  - Badge "+1" discret
  - Photos des projets
  - Configuration Vercel
