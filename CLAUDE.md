# Piscines du Rhin - Site Web

## Entreprise

**Piscines du Rhin** est un pisciniste basé dans le Bas-Rhin (67), Alsace, France, fondé en 2003.

- **Activité** : Construction, rénovation et entretien de piscines en béton sur mesure
- **Zone** : Bas-Rhin (67) — Strasbourg, Haguenau, Saverne, Sélestat et environs
- **Téléphone** : +33 7 61 32 91 84
- **Email** : contact@lespiscinesdurhin.fr
- **Site actuel** : https://piscines-site.vercel.app
- **Horaires** : Lun-Ven 08h-18h
- **Gamme de prix** : €€ (moyen-haut de gamme)

### Services proposés

1. **Construction piscine béton** sur mesure (liner ou carrelage)
2. **Rénovation piscine** et changement de liner
3. **Entretien piscine** régulier
4. **SAV et dépannage** piscine

### Positionnement SEO

Mots-clés cibles principaux :
- "pisciniste Bas-Rhin" / "pisciniste 67" (priorité haute)
- "piscine Strasbourg" (haute concurrence)
- "construction piscine béton Bas-Rhin"
- "rénovation piscine Strasbourg"
- "devis piscine gratuit"

Objectif : top 3 sur "pisciniste Bas-Rhin" sous 3-6 mois.

### Propriétaire

Utilisateur macOS, username `knoery`. Utilise Cursor comme IDE principal avec des MCP servers configurés (Brave Search, Memory, Filesystem, Fetch, Git, N8n). Parle français.

---

## Projet technique

### Stack

- **Type** : Site statique single-page (pas de framework, pas de build)
- **HTML** : Un seul fichier `index.html` (~4000 lignes)
- **CSS** : Tailwind CSS via CDN (pas de PostCSS, pas de fichier CSS séparé)
- **JS** : Vanilla JavaScript inline (pas de bundler)
- **Libs CDN** : AOS (animations scroll), Font Awesome (icônes), EmailJS (formulaire email)
- **Déploiement** : Vercel avec Git integration (push = deploy)
- **Pas de tests, pas de linter, pas de CI/CD**

### Structure des fichiers

```
index.html          ← Page unique (tout le HTML/CSS/JS inline)
vercel.json         ← Config Vercel (rewrites, headers sécurité)
package.json        ← Métadonnées (pas de dépendances ni scripts)
robots.txt          ← Règles crawlers SEO
sitemap.xml         ← Sitemap XML pour Google
assets/             ← Images (32 fichiers : logos, témoignages, photos piscines)
docs/
  SEO-CHECKLIST.md  ← Checklist SEO du projet
  marketing-mcp/    ← 15 guides MCP et marketing (Brave Search, Memory, N8n, etc.)
CLAUDE.md           ← Ce fichier (contexte pour Claude Code)
.claude/            ← Configuration Claude Code
.mcp.json           ← Serveurs MCP pour Claude Code
```

### Fonctionnalités implémentées

- Formulaire de devis multi-étapes (EmailJS pour l'envoi)
- Chatbot IA intégré
- Animations scroll (AOS) + effets parallax
- Compteurs animés (statistiques entreprise)
- Notifications de preuve sociale
- Design glassmorphism avec effets 3D
- Carousel storytelling
- Section FAQ (5 questions, Schema.org FAQPage)
- SEO complet (LocalBusiness, Open Graph, Twitter Cards, géo-ciblage)

### SEO implémenté

- Schema.org : LocalBusiness, WebSite, FAQPage, BreadcrumbList, OfferCatalog
- Open Graph + Twitter Cards
- Méta géo-ciblage (Bas-Rhin, Alsace, coordonnées GPS)
- Google Search Console vérifié
- Bing Webmaster Tools vérifié
- Canonical URL configurée
- Sitemap XML + robots.txt

---

## Conventions de développement

- **Langue** : Tout le contenu, les commentaires et les noms de classes sont en français
- **Pas de build** : Toutes les modifications sont directement dans `index.html`
- **CDN uniquement** : Ne pas installer de dépendances npm pour le front-end
- **Tailwind via CDN** : Utiliser les classes Tailwind inline, pas de fichier CSS séparé
- **Images** : Stocker dans `assets/`, formats WebP ou PNG optimisés
- **Responsive** : Toujours vérifier le rendu mobile après modification CSS
- **Sécurité** : Ne jamais commiter de clés API (EmailJS, Brave Search, etc.)

## Points d'attention critiques

- `index.html` est un fichier volumineux (~4000 lignes) — naviguer avec des recherches ciblées
- Le fichier `docs/marketing-mcp/mcp-config.json` est exclu du Git (contient des clés API)
- Le responsive mobile est critique pour la conversion (formulaire de devis)
- Les animations (AOS, parallax) doivent rester performantes sur mobile
- Vercel déploie automatiquement à chaque push sur `main`

## Commandes utiles

```bash
# Prévisualiser localement
npx serve .
# ou
python3 -m http.server 8000

# Déployer (automatique via Vercel Git integration)
git push origin main
```

---

## Contexte MCP et outils

Le propriétaire utilise un écosystème de 16 MCP servers pour le marketing digital, documenté dans `docs/marketing-mcp/`. Les principaux :

- **Brave Search** : Veille concurrentielle, recherche de mots-clés (2000 req/mois)
- **Memory** : Mémoire persistante (personas, stratégies, données chiffrées)
- **N8n-MCP** : Workflows d'automation marketing
- **Fetch** : Scraping web
- **Sequential Thinking** : Résolution de problèmes complexes

La documentation complète des MCP est dans `docs/marketing-mcp/README.md`.
