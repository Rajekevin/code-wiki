<p align="center">
  <img src="./static/img/code-wiki-logo.svg" width="150" alt="Code Wiki logo">
</p>

# Code Wiki

> ✨ Personal developer wiki and blog built with [Docusaurus 2](https://docusaurus.io/), with instant search, live editing, and GitHub-powered CI/CD.

---

## 🚀 Objectif

Créer un blog technique local et performant avec :

- 🔍 **Recherche instantanée avec Algolia DocSearch**
- 📝 **Édition de contenu via TinaCMS (Markdown visual editor)**
- 🛠️ **CI/CD via GitHub Actions**
- 🌐 **Hébergement via GitHub Pages**
- 🧪 **Contenu statique, rapide et modifiable**

---

## 🧰 Stack technique

| Fonctionnalité        | Technologie utilisée         |
|-----------------------|------------------------------|
| Générateur statique   | [Docusaurus 2](https://docusaurus.io/) |
| CMS headless          | [TinaCMS](https://tina.io/)            |
| Moteur de recherche   | [Algolia DocSearch](https://docsearch.algolia.com/) |
| CI/CD                 | GitHub Actions               |
| Hébergement           | GitHub Pages                 |
| Contenu               | Markdown                     |

---

## ⚙️ Démarrage rapide

### 1. Installer les dépendances

```bash
npm install
```

### 2. Lancer le site en local

```bash
npm run start
```

---

## 🔍 Scraper Algolia

Pour générer l’index de recherche Algolia, utilisez la commande suivante :

```bash
docker run -it --env-file=.env -e "CONFIG=$(cat config.json | jq -r tostring)" algolia/docsearch-scraper
```

> **Pré-requis** :
> - Un fichier `.env` contenant vos variables Algolia (APP_ID, API_KEY, etc.)
> - Un fichier `config.json` de configuration DocSearch valide ([exemple ici](https://docsearch.algolia.com/docs/config-file))

---

## 📁 Structure du projet

```
code-wiki/
├── blog/                  # Articles de blog
├── docs/                  # Documentation technique
├── static/                # Images, favicon, logo SVG
├── src/                   # Composants React (si personnalisations)
├── docusaurus.config.js   # Config Docusaurus principale
├── config.json            # Config Algolia DocSearch
├── .env                   # Variables d’environnement pour Docker
└── README.md
```

---

## ✍️ Contribuer / Modifier les contenus

1. Lancer TinaCMS :
   ```bash
   npm run dev
   ```
2. Se rendre sur `http://localhost:3000/admin`
3. Modifier les articles ou docs via l’interface graphique

---

## 🛠️ Déploiement

Déploiement automatique sur la branche `gh-pages` via GitHub Actions.

---

## 📘 Licence

MIT - libre d’utilisation et d’adaptation pour un usage personnel ou professionnel.

---

## 🧠 Auteur

**Rajekevin** — [www.rajekevin.fr](https://www.rajekevin.fr)

---