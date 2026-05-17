# CNTO — Centre National de Téléopération

> Le centre qui relie parkings, clients et assistance.
> L'expertise humaine et technologique au service d'une mobilité sans friction.

Landing page statique du **CNTO** — Centre National de Téléopération Indigo. HTML/CSS pur, mobile-first, aucune dépendance.

🌐 **En ligne :** [cnto.vercel.app](https://cnto.vercel.app)

---

## 📁 Structure du projet

```
cnto/
├── index.html         ← Page principale
├── styles.css         ← Tous les styles
├── hero.png           ← Image hero (desktop)
├── hero-mobile.png    ← Image hero (mobile)
├── favicon.svg        ← Favicon
├── vercel.json        ← Config Vercel
├── .gitignore
└── README.md
```

**Important :** tous les fichiers doivent être **à la racine** du repo, pas dans un sous-dossier. Sinon Vercel ne trouve pas `index.html` et affiche 404.

---

## 🚀 Déploiement sur Vercel

### Méthode 1 — Via GitHub (recommandé)

1. **Crée un repo GitHub** nommé `cnto`
2. **Pousse les fichiers à la racine :**
   ```bash
   git init
   git add .
   git commit -m "Initial commit — CNTO landing"
   git branch -M main
   git remote add origin https://github.com/TON-USER/cnto.git
   git push -u origin main
   ```
3. **Va sur [vercel.com/new](https://vercel.com/new)**
4. Importer le repo `cnto`
5. Framework Preset : **Other**
6. Root Directory : **laisser vide** (racine)
7. Build Command : **vide**
8. Output Directory : **vide**
9. Cliquer **Deploy**

✅ En ligne en 30 secondes.

### Méthode 2 — Drag & drop direct

1. Aller sur [vercel.com/new](https://vercel.com/new)
2. Choisir **"Deploy a template"** → **"Browse all templates"** → ou utiliser la CLI :
   ```bash
   npm i -g vercel
   cd /chemin/vers/cnto
   vercel
   ```

---

## 🛠️ Si Vercel ne détecte pas le projet

**Symptômes courants :**

| Problème | Cause | Solution |
|---|---|---|
| 404 NOT FOUND | `index.html` dans un sous-dossier | Settings → General → Root Directory → mettre le nom du sous-dossier |
| Page blanche | CSS pas trouvé | Vérifier que `styles.css` est bien à la racine |
| Images cassées | Hero PNG manquants | Vérifier que `hero.png` et `hero-mobile.png` sont push sur GitHub |
| Vercel ne redéploie pas | Cache | Deployments → `…` → Redeploy → décocher "Use existing Build Cache" |

**Forcer le redéploiement :**

1. Dashboard Vercel → projet CNTO
2. Onglet **Deployments**
3. Sur le dernier déploiement → menu `…` à droite
4. **Redeploy** → décocher "Use existing Build Cache"
5. Attendre 30s → vider cache navigateur (Ctrl+Shift+R)

---

## 🌐 Domaine personnalisé

Une fois déployé sur `cnto.vercel.app` :

1. Dashboard Vercel → **Settings** → **Domains**
2. Ajouter `cnto.fr` (ou autre)
3. Configurer le DNS chez le registrar :
   - **A record** (racine) : `76.76.21.21`
   - **CNAME** (www) : `cname.vercel-dns.com`
4. Vercel génère le certificat SSL automatiquement (5-10 min)

---

## 💻 Développement local

```bash
# Avec Node
npx serve .

# Avec Python
python3 -m http.server 3000
```

Ouvrir [localhost:3000](http://localhost:3000).

---

## 🎨 Design

- **Palette** : Crème `#F4EFE5` + Encre `#14110D` + Indigo `#1E2A52`
- **Typo** : Fraunces (titres, italiques) + Inter (corps)
- **Style** : Éditorial, sobre, premium — italiques sur les mots-clés
- **Responsive** : Mobile-first, image hero swap auto entre desktop/mobile

---

## ✏️ Modifications courantes

| Quoi changer ? | Où ? |
|---|---|
| Texte des sections | `index.html` |
| Couleurs | `:root` dans `styles.css` |
| Images du hero | `hero.png` (desktop) / `hero-mobile.png` (mobile) |
| Favicon | `favicon.svg` |
| Meta SEO | balises `<meta>` dans `<head>` de `index.html` |

---

## 📞 Contact

CNTO · Centre National de Téléopération
Indigo Group

---

© 2026 CNTO · Tous droits réservés
