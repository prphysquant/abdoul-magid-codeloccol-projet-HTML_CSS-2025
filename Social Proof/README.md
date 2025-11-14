# Projet Social Proof – Témoignages Clients

## Objectif du projet
Ce projet met en avant des **témoignages clients** et des **avis utilisateurs** afin d’illustrer la satisfaction et la crédibilité d’un service.  
L’interface est **moderne, responsive et lisible** sur tous les appareils.

---

## Structure générale du projet
Le projet se compose de deux fichiers principaux :
- `index.html` → structure sémantique du contenu  
- `styles.css` → mise en forme et design responsive

---

## Commandes et fonctionnalités principales

### 🔹 HTML
| Élément / Attribut | Rôle |
|--------------------|------|
| `<!DOCTYPE html>` | Définit le type de document (HTML5). |
| `<meta charset="UTF-8">` | Assure la bonne lecture des caractères spéciaux (accents). |
| `<meta name="viewport">` | Rend le site **responsive** sur mobile. |
| `<main>` | Conteneur principal du contenu de la page. |
| `<section>` | Sert à organiser les différentes parties du site (titre, avis, témoignages). |
| `<article>` | Utilisé pour chaque **témoignage individuel**. |
| `<img>` | Affiche les photos de profil (avec `alt` pour l’accessibilité). |
| `<div>` | Sert de conteneur pour organiser les éléments (étoiles, texte, etc.). |
| `aria-label` | Améliore l’accessibilité pour les lecteurs d’écran. |

### 🔹 CSS
| Commande / Sélecteur | Fonction |
|----------------------|-----------|
| `* { box-sizing: border-box; }` | Évite les débordements en incluant les bordures dans la taille totale. |
| `.container` | Centre et limite la largeur du contenu. |
| `display: flex;` | Dispose les éléments horizontalement (titre + évaluations). |
| `justify-content` / `align-items` | Gèrent l’alignement horizontal et vertical. |
| `gap` | Crée des espaces entre les éléments sans `margin`. |
| `grid-template-columns` | Utilisé dans la section témoignages pour un affichage en colonnes automatiques. |
| `:hover` | Effet au survol pour les cartes (`transform`, `box-shadow`). |
| `@media (max-width: ...)` | Définit les **breakpoints** pour la version mobile. |
| `nth-child()` | Décale légèrement chaque carte d’évaluation pour un effet visuel élégant. |
| `border-radius` | Arrondit les bords des cartes et des images. |
| `object-fit: cover;` | Ajuste les images sans les déformer. |
| `transition` | Crée une animation fluide lors des survols. |

---

## 📱 Design Responsive
Le design s’adapte automatiquement :
- **≥ 768px** → disposition en colonnes (`flex` et `grid`)
- **< 768px** → disposition verticale (empilement)
- Ajustements précis à **425px** et **320px** pour les très petits écrans.

Les marges, largeurs et tailles de police ont été ajustées dans ces media queries pour garantir une **lecture confortable** sur mobile.

---

## Difficultés rencontrées & solutions

### 1. Alignement du texte et des cartes d’évaluation
**Problème :**  
Les cartes d’évaluation n’étaient pas bien alignées entre elles.  

**Solution :**  
Utilisation de `nth-child()` pour appliquer des `margin-left` différents à chaque carte, créant un décalage visuel équilibré.

---

### 2. Responsivité imparfaite sur mobile
**Problème :**  
Sur petits écrans, les éléments restaient collés ou sortaient du conteneur.  

**Solution :**  
Ajout de **media queries** (`@media (max-width: 768px)`, `425px`, `320px`) pour empiler les éléments verticalement et ajuster les marges/paddings.

---

### 3. Gestion des hover sur les cartes
**Problème :**  
Le changement de couleur au survol affectait toutes les cartes au lieu d’une seule.  

**Solution :**  
Remplacer `.ratings-section :hover` par `.rating-card:hover` pour cibler uniquement la carte survolée.

---

### 4. Couleur et contraste du texte
**Problème :**  
Le texte blanc sur fond violet était parfois difficile à lire.  

**Solution :**  
Utilisation d’une nuance claire (`#d9cadf`) pour les sous-textes, augmentant la lisibilité sans casser la palette de couleurs.

---

### 5. Espacement des sections
**Problème :**  
Certaines sections semblaient trop proches.  

**Solution :**  
Utilisation stratégique de `margin-bottom` et `gap` pour mieux aérer la mise en page.

