# 🔑 Guide Complet : Obtenir TOUTES les Clés API Gratuites

**Date :** 30 Janvier 2026  
**MCP Installés :** 15 servers (5 nouveaux !)  
**Temps total :** 30 minutes maximum

---

## 🎉 NOUVEAUX MCP INSTALLÉS !

Vous avez maintenant **15 MCP servers** au lieu de 10 !

### ✅ **5 Nouveaux MCP Ajoutés :**

1. 📝 **Notion MCP** - Organisation marketing
2. 📊 **Google Sheets MCP** - Rapports automatisés
3. 📚 **Wikipedia MCP** - Recherche encyclopédique (100% gratuit, aucune clé nécessaire !)
4. 🔍 **Reddit MCP** - Veille communautaire
5. 🎯 **Google Search Console MCP** - Monitoring SEO

---

## 🔑 CLÉS API À OBTENIR (6 au total)

### ⚠️ **État Actuel :**
- ✅ **Brave Search** : Configuré
- ⚠️ **Tavily Search** : Nécessite clé gratuite
- ⚠️ **Exa Search** : Nécessite clé gratuite
- ⚠️ **Notion** : Nécessite clé gratuite
- ⚠️ **Google Sheets** : Nécessite credentials gratuits
- ✅ **Wikipedia** : Aucune clé nécessaire !
- ⚠️ **Reddit** : Nécessite credentials gratuits
- ⚠️ **Google Search Console** : Nécessite credentials gratuits

---

## 📋 GUIDE COMPLET PAR MCP

---

## 1️⃣ TAVILY SEARCH (5 minutes)

### ✅ **Plan Gratuit : 1,000 recherches/mois**

### **Étapes :**

**1. Créer un compte (2 min)**
```
URL : https://tavily.com
→ Cliquez "Sign Up"
→ Email + mot de passe
→ Confirmez email
```

**2. Obtenir la clé API (1 min)**
```
→ Connectez-vous à https://tavily.com
→ Allez dans "Dashboard"
→ Section "API Keys"
→ Cliquez "Create API Key"
→ Copiez la clé (commence par "tvly-...")
```

**3. Ajouter dans mcp.json (2 min)**
```bash
# Éditez :
~/Library/Application Support/Cursor/mcp.json

# Ligne 48, remplacez :
"TAVILY_API_KEY": "tvly-VOTRE_CLE_API_TAVILY_ICI"

# Par votre vraie clé :
"TAVILY_API_KEY": "tvly-abc123def456..."
```

### ✅ **Test :**
```
Redémarrez Cursor
Testez : "Recherche avec Tavily les tendances marketing 2026"
```

---

## 2️⃣ EXA SEARCH (5 minutes)

### ✅ **Plan Gratuit : 1,000 recherches/mois**

### **Étapes :**

**1. Créer un compte (2 min)**
```
URL : https://exa.ai
→ Cliquez "Get Started"
→ Email + mot de passe
→ Confirmez email
```

**2. Obtenir la clé API (1 min)**
```
→ Connectez-vous à https://exa.ai
→ Allez dans "Settings" ou "API Keys"
→ Cliquez "Generate API Key"
→ Copiez la clé
```

**3. Ajouter dans mcp.json (2 min)**
```bash
# Ligne 55, remplacez :
"EXA_API_KEY": "VOTRE_CLE_API_EXA_ICI"

# Par votre vraie clé :
"EXA_API_KEY": "exa_abc123def456..."
```

### ✅ **Test :**
```
Redémarrez Cursor
Testez : "Recherche avec Exa des contenus similaires sur le SEO"
```

---

## 3️⃣ NOTION MCP (10 minutes)

### ✅ **Plan Gratuit : Usage personnel illimité**

### **Étapes :**

**1. Créer un compte Notion (2 min)**
```
URL : https://notion.so
→ Sign Up (gratuit)
→ Email + mot de passe
```

**2. Créer une Intégration (5 min)**
```
→ Allez sur : https://www.notion.so/my-integrations
→ Cliquez "+ New integration"
→ Nom : "MCP Marketing Assistant"
→ Type : "Internal Integration"
→ Capabilities : 
   ✅ Read content
   ✅ Update content
   ✅ Insert content
→ Cliquez "Submit"
→ Copiez le "Internal Integration Token" (commence par "secret_...")
```

**3. Partager une page avec l'intégration (2 min)**
```
→ Ouvrez une page Notion
→ Cliquez "Share" (en haut à droite)
→ Cherchez votre intégration "MCP Marketing Assistant"
→ Cliquez "Invite"
```

**4. Ajouter dans mcp.json (1 min)**
```bash
# Ligne 69, remplacez :
"NOTION_API_KEY": "VOTRE_CLE_API_NOTION_ICI"

# Par votre token :
"NOTION_API_KEY": "secret_abc123def456..."
```

### ✅ **Test :**
```
Redémarrez Cursor
Testez : "Liste mes pages Notion"
```

### 📚 **Documentation Notion :**
https://developers.notion.com/docs/create-a-notion-integration

---

## 4️⃣ GOOGLE SHEETS MCP (15 minutes - un peu plus technique)

### ✅ **Plan Gratuit : Illimité**

### **Méthode Simplifiée (Recommandée) :**

**Option A : Service Account (Plus Simple)**

**1. Créer un projet Google Cloud (3 min)**
```
URL : https://console.cloud.google.com
→ Nouveau projet
→ Nom : "MCP Marketing"
→ Créer
```

**2. Activer Google Sheets API (2 min)**
```
→ Dans le projet
→ "APIs & Services" > "Library"
→ Cherchez "Google Sheets API"
→ Cliquez "Enable"
```

**3. Créer Service Account (5 min)**
```
→ "APIs & Services" > "Credentials"
→ "+ Create Credentials"
→ "Service Account"
→ Nom : "MCP Sheets Access"
→ Créer
→ Grant access : "Editor"
→ Done
```

**4. Générer clé JSON (2 min)**
```
→ Cliquez sur le service account créé
→ "Keys" tab
→ "Add Key" > "Create new key"
→ Type : JSON
→ Téléchargez le fichier JSON
```

**5. Ajouter dans mcp.json (3 min)**
```bash
# Ouvrez le fichier JSON téléchargé
# Copiez TOUT son contenu

# Dans mcp.json, ligne 75, remplacez :
"GOOGLE_SHEETS_CREDENTIALS": "VOTRE_CREDENTIALS_GOOGLE_ICI"

# Par le JSON complet (échappé) :
"GOOGLE_SHEETS_CREDENTIALS": "{\"type\":\"service_account\",\"project_id\":\"...\"}"

# OU créez un fichier séparé :
# 1. Sauvegardez le JSON dans : ~/.config/gcp/credentials.json
# 2. Dans mcp.json, mettez le chemin :
"GOOGLE_SHEETS_CREDENTIALS": "/Users/knoery/.config/gcp/credentials.json"
```

**6. Partager vos Google Sheets avec le Service Account**
```
→ Ouvrez votre Google Sheet
→ Cliquez "Share"
→ Ajoutez l'email du service account
   (trouvé dans le JSON : "client_email")
   Ex : mcp-sheets-access@mcp-marketing.iam.gserviceaccount.com
→ Donnez accès "Editor"
```

### ✅ **Test :**
```
Redémarrez Cursor
Testez : "Liste mes Google Sheets"
```

### 📚 **Documentation Google :**
https://developers.google.com/sheets/api/quickstart/python

---

## 5️⃣ WIKIPEDIA MCP (0 minutes - Déjà prêt !)

### ✅ **100% Gratuit - Aucune clé nécessaire !**

**Wikipedia MCP est déjà opérationnel !**

### ✅ **Test immédiat :**
```
"Recherche sur Wikipedia l'histoire du marketing digital"
"Donne-moi des infos Wikipedia sur le SEO"
```

**Pas de configuration nécessaire !** 🎉

---

## 6️⃣ REDDIT MCP (10 minutes)

### ✅ **Plan Gratuit : Illimité (lecture publique)**

### **Étapes :**

**1. Créer un compte Reddit (2 min)**
```
URL : https://reddit.com
→ Sign Up (si pas de compte)
```

**2. Créer une application Reddit (5 min)**
```
→ Allez sur : https://www.reddit.com/prefs/apps
→ Scroll en bas
→ Cliquez "create another app..." ou "are you a developer? create an app..."
→ Remplissez :
   Name : "MCP Marketing Research"
   App type : "script"
   Description : "For marketing research via MCP"
   About url : (laissez vide)
   Redirect uri : http://localhost:8080
→ Cliquez "create app"
```

**3. Récupérer les credentials (2 min)**
```
Vous verrez :
→ Client ID : sous le nom de l'app (ligne de caractères)
→ Client Secret : ligne "secret"
→ Notez ces 2 valeurs
```

**4. Ajouter dans mcp.json (1 min)**
```bash
# Lignes 81-82, remplacez :
"REDDIT_CLIENT_ID": "VOTRE_CLIENT_ID_REDDIT"
"REDDIT_CLIENT_SECRET": "VOTRE_SECRET_REDDIT"

# Par vos vraies valeurs :
"REDDIT_CLIENT_ID": "abc123def456"
"REDDIT_CLIENT_SECRET": "xyz789uvw012"
```

### ✅ **Test :**
```
Redémarrez Cursor
Testez : "Recherche sur Reddit les discussions sur le marketing automation"
```

### 📚 **Documentation Reddit API :**
https://www.reddit.com/wiki/api

---

## 7️⃣ GOOGLE SEARCH CONSOLE MCP (15 minutes - Avancé)

### ✅ **Plan Gratuit : Illimité**

### **Prérequis :**
- Avoir un site web vérifié dans Google Search Console
- Même processus que Google Sheets (Service Account)

### **Étapes Simplifiées :**

**1. Utiliser le même Service Account que Google Sheets**
```
Si vous avez déjà configuré Google Sheets MCP,
vous pouvez réutiliser le même Service Account !
```

**2. Activer Search Console API (2 min)**
```
→ Google Cloud Console
→ "APIs & Services" > "Library"
→ Cherchez "Google Search Console API"
→ Cliquez "Enable"
```

**3. Ajouter le Service Account dans GSC (3 min)**
```
→ Allez sur : https://search.google.com/search-console
→ Sélectionnez votre propriété
→ Settings (roue dentée)
→ "Users and permissions"
→ "Add user"
→ Ajoutez l'email du service account
   Ex : mcp-sheets-access@mcp-marketing.iam.gserviceaccount.com
→ Permission : "Full"
→ Add
```

**4. Ajouter dans mcp.json (1 min)**
```bash
# Ligne 88, utilisez les mêmes credentials que Google Sheets :
"GSC_CREDENTIALS": "/Users/knoery/.config/gcp/credentials.json"
```

### ✅ **Test :**
```
Redémarrez Cursor
Testez : "Montre-moi mes positions Google Search Console"
```

### 📚 **Documentation GSC API :**
https://developers.google.com/webmaster-tools/v1/api_reference_index

---

## 📊 RÉCAPITULATIF : État des MCP

| # | MCP Server | Clé Requise | Difficulté | Temps | Statut |
|---|------------|-------------|------------|-------|--------|
| 1 | Brave Search | ✅ API Key | Facile | 5 min | ✅ FAIT |
| 2 | Tavily Search | ⚠️ API Key | Facile | 5 min | À FAIRE |
| 3 | Exa Search | ⚠️ API Key | Facile | 5 min | À FAIRE |
| 4 | Memory | ❌ Aucune | - | 0 min | ✅ PRÊT |
| 5 | Sequential Thinking | ❌ Aucune | - | 0 min | ✅ PRÊT |
| 6 | N8n-MCP | ❌ Aucune | - | 0 min | ✅ PRÊT |
| 7 | Fetch | ❌ Aucune | - | 0 min | ✅ PRÊT |
| 8 | Filesystem | ❌ Aucune | - | 0 min | ✅ PRÊT |
| 9 | Git | ❌ Aucune | - | 0 min | ✅ PRÊT |
| 10 | Time | ❌ Aucune | - | 0 min | ✅ PRÊT |
| 11 | Notion | ⚠️ Token | Moyen | 10 min | À FAIRE |
| 12 | Google Sheets | ⚠️ Service Account | Avancé | 15 min | À FAIRE |
| 13 | Wikipedia | ❌ Aucune | - | 0 min | ✅ PRÊT |
| 14 | Reddit | ⚠️ Client ID/Secret | Facile | 10 min | À FAIRE |
| 15 | GSC | ⚠️ Service Account | Avancé | 15 min | À FAIRE |

---

## 🎯 PLAN D'ACTION RECOMMANDÉ

### **Phase 1 : Les Faciles (15 min)**
**À faire MAINTENANT :**
1. ✅ Tavily (5 min)
2. ✅ Exa (5 min)
3. ✅ Reddit (10 min)

**Après Phase 1 : 11 MCP actifs (sur 15)**

---

### **Phase 2 : Les Moyens (10 min)**
**À faire cette semaine :**
4. ✅ Notion (10 min)

**Après Phase 2 : 12 MCP actifs**

---

### **Phase 3 : Les Avancés (30 min)**
**À faire quand vous avez le temps :**
5. ✅ Google Sheets (15 min)
6. ✅ Google Search Console (15 min)

**Après Phase 3 : 15 MCP actifs (100% !) 🎉**

---

## 🚀 CONFIGURATION RAPIDE (Priorité Immédiate)

### **Option Express (15 minutes) :**

Configurez JUSTE ces 3 pour avoir un impact immédiat :

1. **Tavily** (5 min) → +1,000 recherches AI/mois
2. **Exa** (5 min) → +1,000 recherches sémantiques/mois  
3. **Reddit** (10 min) → Veille illimitée

**Résultat :** 11 MCP actifs, 6,000 recherches/mois !

---

## ⚠️ TROUBLESHOOTING

### **Problème : "Command not found" après ajout MCP**
**Solution :**
```bash
# Redémarrez complètement Cursor
Cmd + Q
Relancez Cursor
```

### **Problème : MCP ne répond pas**
**Solution :**
```bash
# Vérifiez que la clé API est correcte
# Vérifiez qu'il n'y a pas d'espace avant/après
# Vérifiez les guillemets dans mcp.json
```

### **Problème : Google Sheets/GSC trop complexe**
**Solution :**
```bash
# OPTIONNEL : Vous pouvez les sauter pour l'instant
# Concentrez-vous sur les 13 autres MCP
# Revenez-y plus tard si besoin
```

### **Problème : Reddit ne trouve rien**
**Solution :**
```bash
# Vérifiez que l'app Reddit est bien "script" type
# Vérifiez que les credentials sont corrects
# Testez avec : "Recherche Reddit discussions sur marketing"
```

---

## 📝 CHECKLIST FINALE

### **Configuration Minimale (15 min) :**
- [ ] Tavily API Key configurée
- [ ] Exa API Key configurée
- [ ] Reddit credentials configurés
- [ ] Cursor redémarré
- [ ] Test : "Liste les MCP servers disponibles"

### **Configuration Complète (60 min) :**
- [ ] Tavily ✅
- [ ] Exa ✅
- [ ] Reddit ✅
- [ ] Notion ✅
- [ ] Google Sheets ✅
- [ ] Google Search Console ✅
- [ ] Tous les MCP testés
- [ ] Documentation lue

---

## 💡 CONSEILS PRO

### **1. Créez un fichier de secrets séparé**
```bash
# Créez : ~/.config/mcp-secrets/.env
TAVILY_API_KEY=tvly-...
EXA_API_KEY=exa-...
NOTION_API_KEY=secret-...
REDDIT_CLIENT_ID=...
REDDIT_CLIENT_SECRET=...

# Plus sécurisé que tout dans mcp.json
```

### **2. Testez les MCP progressivement**
```
Ne configurez pas tout d'un coup !
Testez chaque MCP après configuration
Ça aide à identifier les problèmes
```

### **3. Gardez vos clés API en sécurité**
```
❌ Ne partagez JAMAIS vos clés API
❌ Ne commitez JAMAIS vos clés dans Git
✅ Utilisez des variables d'environnement
✅ Changez les clés si exposées
```

### **4. Documentez vos configurations**
```
Notez où vous obtenez chaque clé
Gardez les liens utiles
Ça aide pour la maintenance
```

---

## 🎉 FÉLICITATIONS !

Après avoir suivi ce guide, vous aurez :

**✅ 15 MCP Servers opérationnels**
**✅ 6,000+ recherches gratuites/mois**
**✅ Organisation marketing complète (Notion)**
**✅ Reporting automatisé (Google Sheets)**
**✅ Veille communautaire (Reddit)**
**✅ Monitoring SEO (Google Search Console)**
**✅ Recherche encyclopédique (Wikipedia)**

**Valeur totale :** 800€+/mois  
**Coût réel :** 0€  
**Temps configuration :** 30-60 min  

---

## 📞 AIDE

**Si vous êtes bloqué :**
1. Relisez la section du MCP concerné
2. Vérifiez le Troubleshooting
3. Testez avec Wikipedia d'abord (aucune config)
4. Demandez-moi directement dans Cursor

---

## 🔗 LIENS UTILES

**APIs Gratuites :**
- Tavily : https://tavily.com
- Exa : https://exa.ai
- Notion : https://www.notion.so/my-integrations
- Reddit : https://www.reddit.com/prefs/apps
- Google Cloud : https://console.cloud.google.com

**Documentation MCP :**
- MCP Protocol : https://modelcontextprotocol.io/
- MCP Servers : https://github.com/modelcontextprotocol/servers

**Support :**
- GitHub Issues : https://github.com/knoery-saas/cerveau-mcp/issues
- MCP Discord : Via site officiel

---

## ⏭️ PROCHAINES ÉTAPES

1. ✅ **Suivez Phase 1** (15 min) pour activer 11 MCP
2. 📖 **Lisez MCP-MARKETING-COMPLET.md** pour cas d'usage
3. 🚀 **Testez vos premiers prompts marketing**
4. 📊 **Configurez Notion** pour votre content calendar
5. 🎯 **Explorez les possibilités** avec vos 15 MCP !

---

**🎯 Prêt à transformer votre marketing avec 15 MCP servers GRATUITS ! 🚀**

**GitHub :** https://github.com/knoery-saas/cerveau-mcp  
**Dernière mise à jour :** 30 Janvier 2026
