# EK-Concept — Piscines du Rhin (site vitrine)

## Identite

- **Erwan Knoery**, fondateur EK-Concept
- Bas-Rhin, Alsace, France
- Directeur de creation, developpeur fullstack, producteur IA
- Solopreneur — fait tout lui-meme (dev, design, marketing, video, prospection)
- Mac 8 GB RAM — attention saturation swap

## Regles de communication — IMPORTANT

- Repondre **toujours en francais**
- UI, commentaires, messages : en francais
- Noms de variables, fonctions, classes : en anglais
- Ton direct, pas de blabla, pas de formalites excessives
- Pas d'emojis sauf demande explicite
- Pas de fichiers README/docs sauf demande explicite
- Preferer l'edition de fichiers existants a la creation de nouveaux
- Un fix a la fois, tester, valider avant de passer au suivant
- Ne jamais inventer de donnees

## Regles business — JAMAIS ENFREINDRE

1. **JAMAIS mentionner automatisation/IA/algorithme dans le marketing client** — on vend un service d'expertise realise par une "equipe d'experts"
2. **Signature emails** : "Erwan — Fondateur, [Nom du service]" (PAS "Erwan Knoery" car introuvable sur Google)
3. **Email contact** : toujours `contact@permis-piscines.fr` (jamais erwan@ek-concept.com)

---

## Ce projet : Piscines du Rhin (site vitrine)

**Piscines du Rhin** est un pisciniste fonde en 2003, Bas-Rhin (67).

- **Activite** : Construction, renovation et entretien de piscines en beton sur mesure
- **Zone** : Bas-Rhin (67) — Strasbourg, Haguenau, Saverne, Selestat et environs
- **Telephone** : +33 7 61 32 91 84
- **Email** : contact@lespiscinesdurhin.fr
- **Site** : https://piscines-site.vercel.app
- **Horaires** : Lun-Ven 08h-18h

### Services

1. Construction piscine beton sur mesure (liner ou carrelage)
2. Renovation piscine et changement de liner
3. Entretien piscine regulier
4. SAV et depannage piscine

### SEO cibles

| Requete | Priorite |
|---------|----------|
| pisciniste Bas-Rhin / pisciniste 67 | Haute |
| piscine Strasbourg | Haute (concurrence forte) |
| construction piscine beton Bas-Rhin | Moyenne |
| renovation piscine Strasbourg | Moyenne |
| devis piscine gratuit | Moyenne |

Objectif : top 3 sur "pisciniste Bas-Rhin" sous 3-6 mois.

---

## Stack technique (ce repo)

- **Type** : Site statique single-page (PAS de framework, PAS de build)
- **HTML** : Un seul fichier `index.html` (~4000 lignes)
- **CSS** : Tailwind CSS via CDN (pas de PostCSS, pas de fichier CSS separe)
- **JS** : Vanilla JavaScript inline (pas de bundler)
- **Libs CDN** : AOS (animations scroll), Font Awesome (icones), EmailJS (envoi email)
- **Deploiement** : Vercel avec Git integration (`git push origin main` = deploy)
- **Pas de tests, pas de linter, pas de CI/CD**

### Structure des fichiers

```
index.html          <- Page unique du site (tout le HTML/CSS/JS inline)
vercel.json         <- Config Vercel (rewrites, headers securite)
package.json        <- Metadonnees projet (pas de dependances ni scripts)
robots.txt          <- Regles crawlers SEO
sitemap.xml         <- Sitemap XML pour Google
assets/             <- Images (logos, temoignages, photos piscines)
docs/
  SEO-CHECKLIST.md  <- Checklist SEO du projet
  marketing-mcp/    <- 15 guides MCP et marketing
CLAUDE.md           <- Ce fichier
.claude/            <- Configuration Claude Code
.mcp.json           <- Serveurs MCP pour Claude Code (NON COMMITE — cles API)
```

### Conventions de code (ce repo)

- **Pas de build** : modifications directement dans `index.html`
- **CDN uniquement** : ne pas installer de dependances npm pour le front-end
- **Tailwind via CDN** : classes Tailwind inline, pas de fichier CSS separe
- **Images** : stocker dans `assets/`, formats WebP ou PNG optimises
- **Responsive** : toujours verifier le rendu mobile apres modification CSS
- **Securite** : ne JAMAIS commiter de cles API (EmailJS, Brave Search, etc.)
- Deploy : `git push origin main` (JAMAIS `npx vercel --prod`)

### Fonctionnalites implementees

- Formulaire de devis multi-etapes avec EmailJS
- Chatbot IA integre
- Animations scroll (AOS) + effets parallax
- Compteurs animes (statistiques entreprise)
- Notifications de preuve sociale
- Design glassmorphism avec effets 3D
- Carousel storytelling
- Section FAQ (5 questions, Schema.org FAQPage)

### SEO implemente

- Schema.org : LocalBusiness, WebSite, FAQPage, BreadcrumbList, OfferCatalog
- Open Graph + Twitter Cards
- Meta geo-ciblage (Bas-Rhin, Alsace, coordonnees GPS)
- Google Search Console + Bing Webmaster verifies
- Canonical URL + Sitemap XML + robots.txt

### Points d'attention

- `index.html` est volumineux (~4000 lignes) — naviguer avec des recherches ciblees
- `docs/marketing-mcp/mcp-config.json` est dans `.gitignore` (cles API)
- Le responsive mobile est critique pour la conversion (formulaire de devis)
- Les animations doivent rester performantes sur mobile
- Vercel deploie automatiquement a chaque push sur `main`

### Commandes

```bash
# Preview local
npx serve .

# Deploy (automatique via Vercel Git integration)
git push origin main
```

---

## Cerveau a Skill — 15 serveurs MCP (`.mcp.json`)

Configuration complete de 15 serveurs MCP pour Claude Code. Les cles API doivent etre remplies localement dans `.mcp.json` (fichier exclu du Git).

### Sans cle API (fonctionnent immediatement)

| Serveur | Fonction |
|---------|----------|
| memory | Memoire persistante entre sessions |
| sequential-thinking | Resolution problemes complexes |
| fetch | Recuperation pages web, scraping |
| filesystem | Acces systeme de fichiers |
| git | Operations git |
| time | Gestion fuseaux horaires |
| wikipedia | Recherche encyclopedique |
| n8n-mcp | Workflows automation (1084 nodes, 2709 templates) |

### Avec cle API (a configurer dans `.mcp.json`)

| Serveur | Variable d'env | Source | Limite gratuite |
|---------|---------------|--------|-----------------|
| brave-search | BRAVE_API_KEY | https://brave.com/search/api/ | 2000 req/mois |
| tavily-search | TAVILY_API_KEY | https://tavily.com | 1000 req/mois |
| exa-search | EXA_API_KEY | https://exa.ai | 1000 req/mois |
| reddit | REDDIT_CLIENT_ID + SECRET | https://reddit.com/prefs/apps | Illimite |
| notion | NOTION_API_KEY | https://notion.so/my-integrations | Illimite |
| google-sheets | GOOGLE_SHEETS_CREDENTIALS | Google Cloud Console | Illimite |
| google-search-console | GSC_CREDENTIALS | Google Cloud Console | Illimite |

Guide complet des cles : `docs/marketing-mcp/GUIDE-CLES-API-GRATUITES.md`

---

## Autres projets EK-Concept (contexte croise)

### Permis-Piscines (projet principal)

Service B2B SaaS d'automatisation de dossiers de declaration prealable de travaux pour piscines (CERFA 16702*02). Le client pro remplit un formulaire de 5 min, recoit un ZIP avec 10 PDF en ~30 secondes.

- **Site** : permis-piscines.fr
- **Stack** : Next.js 14 (Vercel) + Express v5 (Railway) + Supabase + Stripe
- **Repo** : `knoery-saas/permis-piscines`
- **Pricing** : Essentiel 179eur, Pro 199eur/mois (3 dossiers), Expert 399eur/mois (8 dossiers)
- **107 tests unitaires**, 140 adresses testees, 100% fiabilite pipeline

### WolfPack

App fitness gamifiee avec loup evolutif (React Native + Expo SDK 52 + Supabase).
- **Repo** : `knoery-saas/wolfpack`
- **Regle critique** : JAMAIS react-native-reanimated (crash SIGABRT)

### Tradex Dashboard

Dashboard trading pour comptes MT5 (Next.js 16 + Supabase).
- Design system dark/light, sparklines SVG, heatmap calendrier

---

## Stack technique globale EK-Concept

| Domaine | Technologies |
|---------|-------------|
| Frontend | Next.js 14+ (App Router), TypeScript, Tailwind CSS, Framer Motion |
| Backend | Node.js ESM, Express v5 |
| Auth + DB | Supabase (Auth + PostgreSQL + RLS) |
| Paiements | Stripe (Checkout, webhooks) |
| Emails | Resend (transactionnel), Brevo (cold email B2B) |
| Hosting | Vercel (frontend), Railway (backend) |
| IA | Gemini (Google), Claude (Anthropic) |
| Mobile | React Native + Expo SDK 52 (Animated natif, JAMAIS reanimated) |
| Icones | Lucide React |
| SEO | GA4, Clarity, Search Console, Lighthouse |

### Conventions globales

- ESM uniquement (`import`/`export`, `"type": "module"`)
- `async`/`await` partout, `const`/`let` (jamais `var`)
- camelCase variables, kebab-case fichiers
- TypeScript strict, pas de `any` sauf cas justifie
- Pas d'over-engineering, simplicite > complexite
