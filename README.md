# Site Khadija RHAOUTI-BENDUDUH — Psychologue

Site statique (HTML/CSS) remplaçant Squarespace. Hébergement gratuit sur Vercel.

---

## Structure

```
/
├── index.html       → page d'accueil
├── a-propos.html    → page à propos
├── styles.css       → styles partagés
└── images/          → à créer (voir ci-dessous)
```

---

## ⚠️ Images — ACTION REQUISE avant résiliation Squarespace

Les images actuelles pointent vers le CDN Squarespace.
**Ces URLs cesseront de fonctionner dès la résiliation du compte.**

### Télécharger les 3 images AVANT de résilier :

| Image | URL actuelle |
|-------|-------------|
| Hero accueil | `https://images.squarespace-cdn.com/.../High_Contrast_Banner_Image_Psychologist_No_Text.jpeg` |
| Photo cabinet | `https://images.squarespace-cdn.com/.../Abstract_Consultation_Space_No_Figures.jpeg` |
| Photo à propos | `https://images.squarespace-cdn.com/.../Natural_Ambiance_Consultation_Vertical.jpeg` |

### Une fois téléchargées :
1. Créer un dossier `images/` à la racine du projet
2. Renommer les fichiers : `hero.jpg`, `cabinet.jpg`, `apropos.jpg`
3. Dans `index.html`, remplacer les URLs Squarespace par :
   - `images/hero.jpg`
   - `images/cabinet.jpg`
4. Dans `a-propos.html`, remplacer par :
   - `images/apropos.jpg`

---

## Déploiement sur Vercel (gratuit)

### 1. Créer un repo GitHub

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/TON_COMPTE/khadija-site.git
git push -u origin main
```

### 2. Déployer sur Vercel

1. Aller sur [vercel.com](https://vercel.com) → Se connecter avec GitHub
2. "Add New Project" → sélectionner le repo
3. Framework Preset : **Other** (site statique)
4. Cliquer **Deploy** → c'est tout

### 3. Brancher le domaine

Dans le dashboard Vercel du projet :
1. Settings → Domains → ajouter `khadija-rhaouti-psychologue.fr`
2. Vercel affiche les DNS records à configurer

Chez le registrar (OVH ou autre), modifier la zone DNS :
- Supprimer les records A/CNAME qui pointent vers Squarespace
- Ajouter les records fournis par Vercel (généralement un CNAME + record A)

⏱ La propagation DNS prend entre 5 min et 24h.

### 4. Résilier Squarespace

**Ne résilier qu'une fois le site Vercel en ligne et le DNS propagé !**

---

## Mises à jour ultérieures

Pour modifier le site (horaires, textes…) :
1. Modifier le fichier HTML concerné
2. `git add . && git commit -m "màj" && git push`
3. Vercel redéploie automatiquement en ~30 secondes
