# 🚀 GUIDE PRODUCT HUNT MCP

## ✅ **INSTALLATION COMPLÈTE**

### **1. Prérequis**
- ✅ Python 3.10+ (déjà installé sur macOS)
- ✅ pip3 (gestionnaire de packages Python)
- ⚠️ **Token API Product Hunt GRATUIT**

---

## 📦 **ÉTAPE 1 : INSTALLER LE PACKAGE**

### **Ouvrez votre Terminal et exécutez :**

```bash
pip3 install product-hunt-mcp
```

**Temps estimé :** 30 secondes

---

## 🔑 **ÉTAPE 2 : OBTENIR VOTRE TOKEN PRODUCT HUNT (GRATUIT)**

### **Instructions détaillées :**

#### **1. Créez un compte Product Hunt Developer (5 min)**

1. **Allez sur :** https://www.producthunt.com/
2. **Cliquez sur** "Sign Up" (en haut à droite)
3. **Créez votre compte** (avec Google/Email)

#### **2. Accédez à l'API Dashboard**

1. **Allez sur :** https://api.producthunt.com/v2/oauth/applications
2. **OU** : Depuis votre profil → Settings → API Dashboard
3. **Cliquez sur** "Create Application"

#### **3. Créez votre Application**

**Remplissez le formulaire :**
```
Application Name: Cursor MCP Analysis
Website URL: http://localhost:3000
Redirect URI: http://localhost:3000/callback
Description: AI analysis tool for Product Hunt data
```

#### **4. Obtenez votre Token**

Une fois l'application créée, vous verrez :
- ✅ **Client ID**
- ✅ **Client Secret**
- ✅ **Developer Token** ← **C'EST CELUI-CI QU'ON VEUT !**

**Copiez le Developer Token** (commence par `ph_`)

---

## 🔧 **ÉTAPE 3 : CONFIGURATION (DÉJÀ FAIT !)**

✅ **Product Hunt MCP est déjà ajouté à votre `mcp.json` !**

**Il suffit maintenant de :**

1. **Remplacez** `VOTRE_TOKEN_PRODUCT_HUNT_ICI`
2. **Par** votre vrai token Product Hunt

### **Où modifier ?**

**Fichier :** `~/Library/Application Support/Cursor/mcp.json`

**Ligne à modifier :**
```json
"product-hunt": {
  "command": "python3",
  "args": ["-m", "product_hunt_mcp"],
  "env": {
    "PRODUCT_HUNT_API_TOKEN": "ph_VOTRE_VRAI_TOKEN_ICI"
  }
}
```

---

## 🎯 **ÉTAPE 4 : REDÉMARRER CURSOR**

1. **Quittez Cursor** complètement
2. **Rouvrez Cursor**
3. **Product Hunt MCP** sera actif ! 🚀

---

## 🔥 **CAPACITÉS PRODUCT HUNT MCP**

### **Ce que vous pouvez faire avec :**

#### **1. 📊 Trending SaaS**
```
"Liste les 20 produits les plus populaires cette semaine sur Product Hunt
dans la catégorie SaaS"
```

#### **2. 🔍 Recherche par catégorie**
```
"Trouve tous les outils de marketing automation lancés en janvier 2026
sur Product Hunt, triés par upvotes"
```

#### **3. 💬 Analyse des commentaires**
```
"Récupère tous les commentaires sur [Nom du produit] sur Product Hunt
et analyse ce que les users aiment/n'aiment pas"
```

#### **4. 👤 Profils des makers**
```
"Analyse le profil du créateur de [Produit X] sur Product Hunt
et liste ses autres produits"
```

#### **5. 📈 Collections trending**
```
"Liste les collections les plus populaires de Product Hunt
dans la catégorie Design Tools"
```

#### **6. ⭐ Recherche avancée**
```
"Trouve les produits Product Hunt avec :
- Plus de 500 upvotes
- Lancés en 2026
- Catégorie: AI Tools
- Avec au moins 50 commentaires"
```

---

## 🎯 **WORKFLOW COMPLET : ANALYSER UN MARCHÉ SAAS**

### **Exemple : Créer un concurrent de Notion**

```
ÉTAPE 1 : DÉCOUVERTE
"Product Hunt : Liste les 50 outils de productivité les plus populaires en 2026
Filtre : Plus de 1000 upvotes
Trie par : Date de lancement (récents d'abord)"

ÉTAPE 2 : ANALYSE PROFONDE
"Pour les 10 premiers produits :
1. Récupère tous leurs commentaires
2. Identifie les features les plus demandées
3. Note les pain points mentionnés
4. Liste les alternatives suggérées"

ÉTAPE 3 : CONCURRENCE
"Analyse les produits similaires à Notion lancés en 2025-2026
Compare leurs features, pricing, et réception"

ÉTAPE 4 : MAKERS INSIGHTS
"Identifie les makers à succès dans cette catégorie
Analyse leurs patterns de lancement
Quelles features ils mettent en avant ?"

ÉTAPE 5 : SYNTHÈSE
"Sequential Thinking : Compile toutes ces données
Identifie le gap parfait dans le marché
Propose un concept de produit unique"
```

---

## 🔧 **TROUBLESHOOTING**

### **Erreur : "Module not found: product_hunt_mcp"**

**Solution :**
```bash
# Réinstallez le package
pip3 uninstall product-hunt-mcp
pip3 install product-hunt-mcp

# Vérifiez l'installation
python3 -m pip show product-hunt-mcp
```

### **Erreur : "Invalid API Token"**

**Vérifiez que :**
- ✅ Le token commence par `ph_`
- ✅ Pas d'espaces avant/après le token
- ✅ Token copié entièrement
- ✅ Application Product Hunt est active

### **Erreur : "Python version"**

**Vérifiez votre version :**
```bash
python3 --version
# Doit être 3.10 ou supérieur
```

**Si < 3.10, mettez à jour :**
```bash
brew install python@3.11
```

---

## 📊 **LIMITES API PRODUCT HUNT (GRATUIT)**

| Feature | Limite Gratuite |
|---------|----------------|
| Requêtes/heure | 50 |
| Requêtes/jour | 500 |
| Produits par requête | 50 |
| Commentaires par produit | 100 |
| Recherches/jour | 100 |

**Largement suffisant pour l'analyse et la création d'apps !**

---

## 🎯 **CAS D'USAGE RÉELS**

### **1. Veille concurrentielle**
```
"Chaque lundi, liste les nouveaux SaaS lancés dans ma catégorie
Identifie les features innovantes
Alerte-moi si un concurrent direct apparaît"
```

### **2. Inspiration features**
```
"Analyse les 100 produits les plus upvotés de 2025
Liste les features les plus demandées en commentaires
Crée un backlog de features à implémenter"
```

### **3. Market research**
```
"Quel type de SaaS marketing fonctionne le mieux en 2026 ?
Analyse les catégories, upvotes, comments
Identifie les tendances émergentes"
```

### **4. Validation d'idée**
```
"Recherche si mon idée existe déjà sur Product Hunt
Si oui : Comment a-t-elle été reçue ?
Quels retours users ? Ça marche encore ?"
```

---

## 🚀 **NEXT STEPS**

Une fois Product Hunt MCP configuré, vous aurez :

✅ **16 MCP actifs** (le plus gros setup MCP que j'ai vu !)

### **Combinaison ULTIME pour analyser les SaaS :**

```
RECHERCHE :
- Product Hunt MCP (top produits)
- Brave Search (contexte marché)
- Tavily Search (deep research)
- Exa Search (trouve articles/blogs)

ANALYSE :
- Fetch MCP (scrape leurs sites)
- Reddit MCP (opinions users)
- Wikipedia MCP (contexte tech)

INTELLIGENCE :
- Sequential Thinking (analyse patterns)
- Memory MCP (stocke insights)

CRÉATION :
- N8n MCP (automatise workflows)
- Filesystem MCP (génère code)
- Git MCP (version tout)
```

---

## 🔥 **COMMANDE COMPLÈTE POUR TESTER**

```
"Product Hunt : Liste les 10 produits les plus upvotés aujourd'hui

Pour chaque produit :
1. Récupère nom, description, upvotes, comments
2. Scrape leur site web avec Fetch MCP
3. Analyse leur landing page
4. Identifie leur value proposition principale
5. Note les patterns UI/UX communs

Mémorise tout avec Memory MCP

Puis utilise Sequential Thinking pour :
- Identifier les patterns de succès
- Trouver ce qui manque dans le marché
- Proposer 3 idées de SaaS inspirées mais uniques"
```

---

## 💡 **BESOIN D'AIDE ?**

1. **Problème d'installation ?** → Consultez la section Troubleshooting
2. **Token API ne marche pas ?** → Vérifiez sur https://api.producthunt.com/
3. **Questions ?** → Demandez-moi, je suis là ! 🚀

---

## 📝 **RÉSUMÉ INSTALLATION**

```bash
# 1. Installez le package
pip3 install product-hunt-mcp

# 2. Obtenez votre token (5 min)
# → https://api.producthunt.com/v2/oauth/applications

# 3. Ajoutez le token dans mcp.json (déjà fait !)
# → ~/Library/Application Support/Cursor/mcp.json

# 4. Redémarrez Cursor
# → C'est prêt ! 🎉
```

---

**Vous avez maintenant le MEILLEUR setup pour analyser et s'inspirer des top SaaS US ! 🔥🚀**
