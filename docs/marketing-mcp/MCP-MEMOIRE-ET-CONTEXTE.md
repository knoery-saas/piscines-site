# 🧠 MCP Mémoire & Compréhension

## Vos 2 besoins

1. **Mieux comprendre ce que vous dites** → Contexte persistant, projet, préférences
2. **Ne pas oublier ce qu'on se dit** → Mémoire des faits, décisions, données

---

## 📦 Les 2 MCP recommandés

### 1. 🧠 **Memory MCP** (déjà installé chez vous)

**À quoi ça sert : NE PAS OUBLIER**

- Stocke des **faits** et **informations** persistants
- Mémorise vos projets, clients, stratégies
- Persiste entre les conversations
- Pas de limite de stockage

**Exemples d'utilisation :**
```
"Mémorise que Magic Fit Auenheim a 1200 membres et 33K€ MRR"
"Rappelle-moi les infos sur le prestataire Facebook Ads"
"Stocke cette stratégie marketing pour Magic Fit"
"Qu'as-tu mémorisé sur Magic Fit ?"
```

**Ce qu'il mémorise :**
- Contexte Magic Fit (membres, MRR, concurrent Basic-Fit, etc.)
- Vos préférences (ex: répondre en français)
- Projets en cours
- Décisions prises
- Données chiffrées

**Comment l'utiliser :**
- Dites **"Mémorise..."** quand on discute d'infos importantes
- Dites **"Rappelle-moi..."** pour récupérer le contexte
- Je l'utilise aussi automatiquement quand c'est pertinent

---

### 2. 📚 **Memory Bank MCP** (nouveau - à installer)

**À quoi ça sert : MIEUX COMPRENDRE**

- Crée des **fichiers de contexte** structurés
- Contexte projet, architecture, préférences
- Fichiers Markdown dans un dossier dédié
- Contexte chargé automatiquement en début de conversation

**Exemples d'utilisation :**
```
"Crée un Memory Bank pour le projet Magic Fit"
"Documente notre stratégie marketing dans le Memory Bank"
"Met à jour le contexte avec les derniers chiffres"
```

**Ce qu'il contient :**
- Fichiers `activeContext.md` (contexte actif)
- Fichiers par projet (ex: `magic-fit-auenheim.md`)
- Résumés de conversations importantes
- Préférences utilisateur structurées

**Avantage vs Memory :**
- **Memory** = faits isolés (comme des post-its)
- **Memory Bank** = documentation structurée (comme un wiki)
- Les 2 se complètent !

**Structure typique :**
```
memory-bank/
├── activeContext.md      # Contexte actif de conversation
├── magic-fit/
│   └── contexte.md       # Tout sur Magic Fit
└── user-preferences.md   # Vos préférences
```

---

## 🔄 Comment ils travaillent ensemble

| Situation | Memory MCP | Memory Bank MCP |
|-----------|------------|-----------------|
| "Rappelle-moi le MRR de Magic Fit" | ✅ | - |
| "Quels sont nos objectifs 90 jours ?" | ✅ | ✅ |
| Nouvelle conversation, contexte projet | ✅ Rappel | ✅ Fichier chargé |
| Préférences (répondre en français) | ✅ | ✅ |
| Documentation complète stratégie | - | ✅ |
| Infos chiffrées rapides | ✅ | ✅ |

---

## 📥 Installation Memory Bank MCP

### Étape 1 : Créer le dossier

Le dossier `memory-bank` a été créé dans votre projet.

### Étape 2 : Configuration Cursor

Le Memory Bank MCP est ajouté dans votre `mcp.json` :

```json
"memory-bank": {
  "command": "npx",
  "args": ["-y", "@allpepper/memory-bank-mcp"],
  "env": {
    "MEMORY_BANK_ROOT": "/Users/knoery/Desktop/Le cerveau a skill/memory-bank"
  }
}
```

### Étape 3 : Copier dans Cursor

```bash
# Copiez la config dans Cursor
# Le fichier mcp.json du projet doit être synchronisé avec :
# ~/Library/Application Support/Cursor/mcp.json
```

### Étape 4 : Redémarrer Cursor

1. Quittez Cursor (Cmd + Q)
2. Rouvrez Cursor
3. Le Memory Bank sera actif !

---

## 🎯 Utilisation pratique

### Pour Magic Fit (exemple)

**Conversation 1 :** On discute de tout
→ Je mémorise dans **Memory** : membres, MRR, prestataire, Basic-Fit
→ Je peux créer dans **Memory Bank** : `magic-fit/strategie-90-jours.md`

**Conversation 2 (demain) :** Vous dites "On en était où ?"
→ **Memory** : Je récupère les faits (1200 membres, 33K MRR...)
→ **Memory Bank** : Je lis le fichier stratégie
→ Réponse précise sans que vous réexpliquiez !

**Conversation 3 (dans 1 semaine) :** Vous dites "Envoie le doc à mon père"
→ **Memory** + **Memory Bank** : Contexte complet
→ Je peux régénérer le document à jour

---

## ✅ Checklist utilisation

- [ ] Utiliser **"Mémorise..."** pour les infos importantes
- [ ] Demander **"Rappelle-moi..."** en début de session si besoin
- [ ] Créer des **Memory Bank** pour les gros projets
- [ ] Mettre à jour le contexte quand les chiffres changent

---

## 🔥 Commandes utiles

```
"Mémorise tout ce qu'on a dit sur Magic Fit"
"Qu'as-tu mémorisé sur [sujet] ?"
"Crée un résumé de notre conversation dans le Memory Bank"
"Met à jour le contexte Magic Fit avec les nouveaux chiffres"
"Rappelle-moi le plan d'action 90 jours"
```

---

**Avec Memory + Memory Bank = Je ne vous oublie plus ET je comprends mieux ! 🧠**
