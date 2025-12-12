# 🍽️ Feane Restaurant - Documentation

## 📋 Vue d'ensemble du projet

**Feane** est un site web de restaurant moderne et responsive, développé avec **Bootstrap 5.3.8** et **HTML/CSS**. Le projet présente une navigation intuitive, un menu de produits interactif et une mise en page fluide qui s'adapte à tous les appareils.

### 📁 Structure du projet
Feane_Restorant/
├── index.html # Page d'accueil
├── Menu.html # Page du menu avec grille de produits
├── BookTable.html # Page de réservation de table
├── About.html # Page à propos
├── style.css # Styles personnalisés
├── images/ # Dossier contenant les images
└── README.md # Ce fichier

### 📄 Pages disponibles

1. **index.html** - Page d'accueil avec présentation du restaurant
2. **Menu.html** - Affichage des plats avec système de filtrage (All, Burger, Pizza, Pasta, Fries)
3. **BookTable.html** - Formulaire pour réserver une table
4. **About.html** - Informations sur le restaurant

---

## 🎨 Technologies utilisées

- **HTML5** - Structure sémantique
- **CSS3** - Styles personnalisés
- **Bootstrap 5.3.8** - Framework CSS responsive
- **Bootstrap Icons 1.13.1** - Icônes vectorielles
- **Google Fonts** - Police "Dancing Script" pour les titres

---

## 📱 Flexbox Bootstrap - Explications

### Qu'est-ce que Flexbox ?

Flexbox est un système de disposition moderne qui permet d'organiser les éléments en ligne ou colonne avec un alignement et une répartition d'espace flexible. Bootstrap fournit des classes utilitaires pour utiliser Flexbox sans écrire de CSS personnalisé.

### Classes Flexbox Bootstrap principales

#### 1. **`d-flex`** - Activer Flexbox
Transforme un élément en conteneur flex.

```html
<div class="d-flex">
  <div>Élément 1</div>
  <div>Élément 2</div>
</div>

2. flex-row et flex-column - Direction
flex-row (défaut) : Arrange les éléments horizontalement
flex-column : Arrange les éléments verticalement
Exemple du projet (Menu.html) :
<div class="d-flex flex-column align-items-center">
  <h2 class="Style fs-1">Our Menu</h2>
  <!-- Les enfants s'empilent verticalement -->
</div>

<ul class="navbar-nav d-flex flex-row gap-3">
  <!-- Les enfants s'alignent horizontalement -->
</ul>

3. justify-content-* - Alignement horizontal
Contrôle l'alignement des éléments sur l'axe principal (horizontal en flex-row).

justify-content-start - Au début (défaut)
justify-content-center - Au centre
justify-content-end - À la fin
justify-content-between - Espacement égal entre les éléments
justify-content-around - Espacement égal avec marge sur les côtés
justify-content-evenly - Espacement égal partout

<div class="d-flex justify-content-center mt-5">
  <a class="btn btn-warning rounded-pill text-white" href="">View More</a>
</div>
<!-- Le bouton est centré horizontalement -->

<div class="d-flex align-items-center justify-content-between">
  <p class="m-0">$17</p>
  <article class="Shop_icone">...</article>
</div>
<!-- Prix à gauche, icône panier à droite -->

 6. flex-wrap - Retour à la ligne
flex-wrap - Les éléments passent à la ligne si pas assez de place
flex-nowrap (défaut) - Tous sur une ligne
Résumé des classes Flexbox les plus utilisées dans votre projet
Classe	Effet
d-flex	Active Flexbox
flex-row	Disposition horizontale
flex-column	Disposition verticale
justify-content-center	Centrer horizontalement
align-items-center	Centrer verticalement
gap-3	Espacement de 1rem entre éléments
justify-content-between	Espacement entre les extrémités

📱 Breakpoints Bootstrap - Explications
Qu'est-ce qu'un Breakpoint ?
Un breakpoint est un point de rupture où la mise en page se réajuste pour s'adapter à la taille de l'écran. Bootstrap utilise les media queries CSS pour appliquer différents styles à différentes résolutions d'écran.

Les Breakpoints Bootstrap
Bootstrap 5 définit 6 points de rupture principaux :

Breakpoint	Classe	Taille d'écran	Utilisation
Extra small	xs (défaut)	< 576px	Téléphones
Small	sm	≥ 576px	Grands téléphones
Medium	md	≥ 768px	Tablettes
Large	lg	≥ 992px	Petits ordinateurs
Extra large	xl	≥ 1200px	Ordinateurs
XXL	xxl	≥ 1400px	Grands écrans

Explication :

col-12 → Sur mobile : 100% de largeur (1 carte par ligne)
col-md-6 → Sur tablette : 50% de largeur (2 cartes par ligne)
col-lg-4 → Sur ordinateur : 33% de largeur (3 cartes par ligne)
Téléphone (< 768px)     Tablette (768px-992px)    Ordinateur (≥992px)
┌────────────────┐     ┌─────────────┬─────────┐  ┌────┬────┬────┐
│    Carte 1     │     │  Carte 1    │ Carte 2 │  │C1  │C2  │C3  │
├────────────────┤     ├─────────────┼─────────┤  ├────┼────┼────┤
│    Carte 2     │     │  Carte 3    │ Carte 4 │  │C4  │C5  │C6  │
├────────────────┤     ├─────────────┼─────────┤  ├────┼────┼────┤
│    Carte 3     │     │  Carte 5    │ Carte 6 │  │C7  │C8  │C9  │
└────────────────┘     └─────────────┴─────────┘  └────┴────┴────┘

Résumé des Breakpoints:
┌──────────────────────────────────────────────────────────────┐
│ Mobile-First Approach (xs → sm → md → lg → xl → xxl)        │
├──────────────────────────────────────────────────────────────┤
│ col-12        → 100% width (toujours)                        │
│ col-sm-6      → 50% à partir de 576px                        │
│ col-md-4      → 33% à partir de 768px                        │
│ col-lg-3      → 25% à partir de 992px                        │
│ col-xl-2      → 16.67% à partir de 1200px                   │
└──────────────────────────────────────────────────────────────┘

