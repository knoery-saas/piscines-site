# 🔴 Guide Complet Reddit MCP - Configuration en 5 Minutes

**Ne trouvez pas le Client ID et Secret ? Suivez ce guide pas à pas !**

---

## 🎯 Ce que vous cherchez

Pour Reddit MCP, vous avez besoin de **2 choses** :
1. **Client ID** (une ligne de caractères)
2. **Client Secret** (une ligne "secret")

---

## 📝 ÉTAPES DÉTAILLÉES

### **Étape 1 : Allez sur Reddit Apps (2 min)**

**Option A - Lien Direct :**
```
https://www.reddit.com/prefs/apps
```

**Option B - Navigation Manuelle :**
1. Allez sur https://reddit.com
2. Connectez-vous à votre compte
3. Cliquez sur votre avatar (en haut à droite)
4. **User Settings** / **Préférences**
5. Dans le menu de gauche : **"Safety & Privacy"** ou **"Sécurité"**
6. Scrollez en bas jusqu'à **"Apps"**
7. Cliquez sur **"Apps"**

---

### **Étape 2 : Créer une Application (3 min)**

Une fois sur la page Apps :

**1. En bas de la page, cherchez :**
- **"developed applications"** ou **"applications développées"**
- Vous verrez un bouton : **"are you a developer? create an app..."**

**2. Cliquez sur ce bouton**

**3. Remplissez le formulaire :**

```
Name (Nom) :
→ "MCP Marketing Research"
   (ou n'importe quel nom)

App type (Type d'app) :
→ ⚠️ IMPORTANT : Sélectionnez "script"
   (PAS "web app", PAS "installed app")

Description :
→ "Marketing research via Model Context Protocol"
   (ou laissez vide)

About url :
→ Laissez VIDE (optionnel)

Redirect uri :
→ http://localhost:8080
   (important : exactement comme ça)
```

**4. Cochez "I'm not a robot"**

**5. Cliquez sur "create app" ou "créer l'application"**

---

### **Étape 3 : Récupérer les Credentials (1 min)**

Après avoir cliqué "create app", vous verrez une **boîte avec les détails de votre app**.

**Voici où trouver les 2 valeurs :**

```
┌─────────────────────────────────────┐
│ MCP Marketing Research              │  ← Nom de votre app
│                                     │
│ abc123def456                        │  ← CLIENT ID (sous le nom)
│ [personal use script]               │  ← Type d'app
│                                     │
│ secret: xyz789uvw012abc345          │  ← CLIENT SECRET (ligne "secret:")
│                                     │
│ [edit] [delete]                     │
└─────────────────────────────────────┘
```

**À NOTER :**
1. **Client ID** : Ligne de caractères juste en dessous du nom (ex: `abc123def456`)
2. **Client Secret** : Après le mot "secret:" (ex: `xyz789uvw012abc345`)

---

### **Étape 4 : Ajout dans mcp.json (1 min)**

**1. Notez vos 2 valeurs :**
```
Client ID : abc123def456
Client Secret : xyz789uvw012abc345
```

**2. Je vais les ajouter pour vous !**

Donnez-moi juste vos 2 valeurs en me disant :
```
"Client ID : [votre valeur]
Client Secret : [votre valeur]"
```

---

## 🔍 CAPTURE D'ÉCRAN TYPE

Quand vous êtes sur https://www.reddit.com/prefs/apps, vous devriez voir :

```
Votre page ressemble à ça :
─────────────────────────────────────────
Reddit Preferences

Safety & Privacy
├── Account
├── Profile  
├── Safety & Privacy  ← Cliquez ici
│   └── Apps          ← Puis ici
└── ...
─────────────────────────────────────────

En bas de la page Apps :
─────────────────────────────────────────
developed applications

[are you a developer? create an app...] ← Cliquez ici
─────────────────────────────────────────
```

---

## 🎯 RÉSUMÉ ULTRA-SIMPLE

1. **Allez sur :** https://www.reddit.com/prefs/apps
2. **Scrollez en bas**
3. **Cliquez :** "are you a developer? create an app..."
4. **Nom :** MCP Marketing Research
5. **Type :** script (important !)
6. **Redirect :** http://localhost:8080
7. **Créer**
8. **Notez :**
   - Client ID (sous le nom)
   - Client Secret (ligne "secret:")

---

## ❓ PROBLÈMES FRÉQUENTS

### **"Je ne vois pas le bouton create app"**
→ Scrollez complètement en bas de la page
→ Vérifiez que vous êtes bien connecté à Reddit

### **"Ça me demande de vérifier mon email"**
→ Allez vérifier votre email Reddit
→ Cliquez sur le lien de confirmation
→ Revenez sur la page

### **"Je n'ai pas de compte Reddit"**
→ Créez-en un : https://reddit.com/register (gratuit, 2 min)

### **"Le type 'script' n'existe pas"**
→ Il y a 3 types : web app, installed app, script
→ Sélectionnez "script" (le 3ème choix)

---

## 💡 ALTERNATIVE : REDDIT EN MODE LECTURE SEULE

Si vous avez des difficultés, vous pouvez aussi utiliser Reddit **sans authentification** pour la veille (lecture publique uniquement).

Je peux configurer le MCP Reddit en mode "lecture seule" :
- Pas besoin de Client ID/Secret
- Peut lire posts/discussions publics
- Ne peut pas poster/commenter

Voulez-vous cette option ?

---

## ✅ VÉRIFICATION

Une fois que vous avez vos credentials, testez avec :

```
"Recherche sur Reddit les discussions sur le marketing automation"
```

Si ça marche, vous verrez des résultats de posts Reddit !

---

## 📞 AIDE

Si vous êtes bloqué :
1. Dites-moi à quelle étape vous êtes bloqué
2. Envoyez-moi ce que vous voyez sur votre écran
3. Je vous guiderai précisément

Exemples :
- "Je suis sur reddit.com/prefs/apps mais je ne vois pas de bouton"
- "J'ai créé l'app mais je ne trouve pas le Client ID"
- "Ça me demande un truc que je ne comprends pas"

---

## 🎯 APRÈS CONFIGURATION

Une fois Reddit configuré, vous aurez :
- ✅ **12 MCP actifs** (sur 15)
- ✅ **5,000+ recherches/mois**
- ✅ **Veille communautaire illimitée**
- ✅ **Sentiment analysis Reddit**

---

**Donnez-moi vos 2 valeurs Reddit et je finalise la config ! 🚀**

**Ou dites-moi où vous êtes bloqué et je vous aide pas à pas.**
