# 📷 Photo Club Briançonnais - Site Web

Un site web classique et simple pour le Photo Club Briançonnais, avec interface d'édition visuelle via **Pages CMS**.

---

## 🚀 Installation en 3 étapes

### Étape 1 : Créer le repository GitHub

1. Allez sur [github.com/new](https://github.com/new)
2. Nom du repository : `photoclubbrianconnais`
3. Rendez-le **Public**
4. Cochez "Add a README file"
5. Cliquez sur **Create repository**

### Étape 2 : Uploader les fichiers

#### Méthode simple (interface web) :

1. Dans votre repo GitHub, cliquez sur **"Add file"** → **"Upload files"**
2. Glissez-déposez tous les fichiers de ce dossier
3. Cliquez sur **"Commit changes"**

#### Méthode Git (ligne de commande) :

```bash
git clone https://github.com/VOTRE_USERNAME/photoclubbrianconnais.git
cd photoclubbrianconnais

# Copier tous les fichiers du site ici
cp -r /chemin/vers/photo-club-classic/* .

git add .
git commit -m "Initial commit"
git push origin main
```

### Étape 3 : Activer GitHub Pages

1. Dans votre repo, allez dans **Settings** → **Pages** (dans le menu gauche)
2. Source : sélectionnez **"GitHub Actions"**
3. Le workflow est déjà configuré dans `.github/workflows/deploy.yml`

⏳ Attendez 2-3 minutes, puis votre site sera en ligne à :
`https://VOTRE_USERNAME.github.io/photoclubbrianconnais/`

---

## 📝 Utiliser Pages CMS (Édition visuelle)

Pages CMS vous permet de modifier le contenu du site **sans toucher au code**, exactement comme sur SiteW.

### Connexion à Pages CMS

1. Allez sur [app.pagescms.org](https://app.pagescms.org/)
2. Cliquez sur **"Sign in with GitHub"**
3. Autorisez l'accès à votre repository `photoclubbrianconnais`
4. Votre projet apparaît dans la liste, cliquez sur **"Open"**

### Interface d'édition

Une fois connecté, vous verrez :

- **📄 Pages** : Liste des pages du site (Accueil, Le Club, Activités, Galerie, Contact)
- **🖼️ Media** : Gestionnaire d'images
- **⚙️ Settings** : Configuration du CMS

### Modifier une page

1. Cliquez sur la page à modifier (ex: "Page d'accueil")
2. Modifiez le texte dans l'éditeur visuel (comme Word)
3. Cliquez sur **"Save"** en haut à droite
4. Pages CMS crée automatiquement un commit GitHub
5. Le site se met à jour automatiquement en 1-2 minutes !

### Ajouter une photo dans la galerie

1. Allez dans **Media** → **images**
2. Glissez-déposez vos photos ou cliquez sur **"Upload"**
3. Les images sont automatiquement ajoutées au dossier `images/`
4. Modifiez la page "Galerie" pour ajouter le code HTML de la nouvelle photo

---

## 📁 Structure du site

```
photoclubbrianconnais/
├── index.html              # Page d'accueil
├── le-club.html           # Page Le Club
├── activites.html         # Page Activités
├── galerie.html           # Page Galerie
├── contact.html           # Page Contact
├── css/
│   └── style.css          # Styles du site
├── images/                # Dossier des images
├── .github/
│   └── workflows/
│       └── deploy.yml     # Déploiement automatique
├── .pages.yml             # Configuration Pages CMS
└── README.md              # Ce fichier
```

---

## 🎨 Personnalisation sans CMS

Si vous préférez modifier directement les fichiers :

### Modifier le contenu

Ouvrez les fichiers `.html` et modifiez le texte entre les balises. Exemple :

```html
<!-- Avant -->
<p>Notre club a vu le jour grâce à la passion...</p>

<!-- Après -->
<p>Votre nouveau texte ici...</p>
```

### Changer les couleurs

Dans `css/style.css`, modifiez les couleurs au début :

```css
.site-header {
    background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);
    /* Changez les codes couleur ici */
}
```

### Ajouter une photo

1. Placez l'image dans le dossier `images/`
2. Dans `galerie.html`, ajoutez :

```html
<div class="gallery-item">
    <img src="images/ma-photo.jpg" alt="Description">
    <p class="photo-title">Titre</p>
    <p class="photo-author">par Auteur</p>
</div>
```

---

## 🔧 Configuration du formulaire de contact

Le formulaire utilise **Formspree** (gratuit pour 50 envois/mois) :

1. Allez sur [formspree.io](https://formspree.io)
2. Créez un compte et un nouveau formulaire
3. Copiez votre ID (format : `xzbqwppg`)
4. Dans `contact.html`, remplacez :
   ```html
   action="https://formspree.io/f/YOUR_FORM_ID"
   ```
   par :
   ```html
   action="https://formspree.io/f/xzbqwppg"
   ```

---

## 📱 Caractéristiques

- ✅ **100% Gratuit** (GitHub Pages + Pages CMS)
- ✅ **Responsive** (s'adapte aux mobiles)
- ✅ **Édition visuelle** (comme SiteW)
- ✅ **Déploiement automatique** (GitHub Actions)
- ✅ **Sans base de données** (fichiers statiques)
- ✅ **SEO friendly**

---

## ❓ Support

- **Pages CMS** : [Documentation](https://pagescms.org/docs/)
- **GitHub Pages** : [Aide GitHub](https://docs.github.com/fr/pages)
- **Problèmes** : Ouvrez une issue sur votre repository GitHub

---

**© 2026 Photo Club Briançonnais**  
*Site créé avec ❤️ pour les passionnés de photographie*
