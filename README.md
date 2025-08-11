# Calculateur d'Eutectiques n-aires

Une application web interactive pour le calcul thermodynamique de mélanges eutectiques multi-composants, avec visualisation par diagramme circulaire.

![Version](https://img.shields.io/badge/version-1.0-blue.svg)
![Status](https://img.shields.io/badge/status-experimental-orange.svg)
![Generated](https://img.shields.io/badge/generated-Claude_Code-purple.svg)

## 📖 À propos

Cette application implémente les équations thermodynamiques pour calculer la composition et la température des points eutectiques dans des systèmes n-aires (binaires, ternaires, quaternaires, etc.).

### 🔬 Bases scientifiques

L'application est basée sur la publication scientifique originale :

**Brunet, L., Caillard, J. & André, P.** *Thermodynamic calculation of n-component eutectic mixtures*. **International Journal of Modern Physics C** 15, 675–687 (2004).

Le script original était écrit en **ADA95**. Cette version web utilise les mêmes algorithmes thermodynamiques mais avec une interface moderne et interactive.

### ⚗️ Méthode

L'application utilise la **méthode de Newton-Raphson** pour résoudre le système d'équations non-linéaires basé sur :

- **Équilibre thermodynamique** : μᵢ = μᵢ°
- **Équation d'équilibre** : ln(xᵢ) + Hᵢ/R × (1/T - 1/Tᵢ°) = 0
- **Approximations** : 
  - Liquides miscibles
  - Enthalpie de fusion constante
  - Pas de composés intermédiaires
  - Activité ≈ concentration

## ✨ Fonctionnalités

### 🧪 Sélection des matériaux
- **115+ composés** dans la base de données
- **Recherche filtrée** par nom ou formule
- **Catégories variées** : métaux, sels, organiques, etc.
- **Sélection illimitée** de composants

### 🧪 Cas de test
- **3 systèmes de référence** de la publication originale
- **Ag-Si** : système binaire métal-semi-conducteur
- **KCl-LiCl-NaCl** : système ternaire de chlorures alcalins
- **KNO₃-LiNO₃-NaNO₃** : système ternaire de nitrates alcalins

### 🧠 Optimisation par algorithme génétique
- **Recherche inverse** : spécifier une température cible
- **Systèmes variables** : 2 à 7 composants
- **Population de 50 individus** sur 100 générations
- **Opérateurs évolutionnaires** : sélection par tournoi, croisement uniforme, mutation adaptative
- **5 meilleures solutions** avec écart à la cible

### 🍰 Visualisation
- **Diagramme circulaire** interactif
- **Couleurs uniques** par composant
- **Température eutectique** au centre
- **Légende dynamique** avec pourcentages
- **Tooltips** informatifs

### 📱 Interface
- **Design responsive** (desktop, tablette, smartphone)
- **Animations fluides** CSS3 + jQuery
- **Police scientifique** Lexend Deca
- **Thème professionnel** bleu marine

## 🚀 Utilisation

### 🌐 Démo en ligne
**Essayez l'application directement :** [https://l0d0v1c.github.io/eutecJS/](https://l0d0v1c.github.io/eutecJS/)

### Installation locale
```bash
git clone https://github.com/votre-repo/eutec.git
cd eutec
# Ouvrir index.html dans un navigateur
```

### Utilisation
1. **Sélectionner** 2+ matériaux dans les menus déroulants
2. **Configurer** ou utiliser la sélection aléatoire
3. **Calculer** l'eutectique avec le bouton bleu
4. **Visualiser** les résultats dans le diagramme circulaire

## 📊 Base de données

### Composés inorganiques
- **Métaux** : Ag, Al, Cu, Zn, Pb, Sn
- **Semi-conducteurs** : Si, Ge
- **Sels halogénés** : KCl, NaCl, LiF, etc.
- **Nitrates** : KNO₃, AgNO₃, etc.
- **Hydroxydes, sulfates**

### Composés organiques
- **Alcanes** : C₆H₁₄ à C₂₀H₄₂
- **Acides carboxyliques** : acétique, stéarique, benzoïque
- **Alcools** : méthanol à décanol, glycols
- **Aromatiques** : benzène, toluène, naphtalène
- **Liquides ioniques** : chlorure de choline, urée

## 🔧 Technologies

- **HTML5/CSS3** avec Flexbox et Grid
- **JavaScript ES6** avec jQuery 3.6
- **SVG** pour le diagramme circulaire
- **Responsive Design** avec media queries
- **Lexend Deca** font family

## ⚠️ Avertissements

### 🧪 Nature expérimentale
Cette application est **EXPÉRIMENTALE** et a été **générée par Claude Code**. 

### 📝 Limitations
- **Approximations thermodynamiques** simplifiées
- **Validation expérimentale** recommandée
- **Écart moyen ~60°C** avec valeurs expérimentales (publication originale)
- **Pas de garantie** de précision pour applications critiques

### 🎯 Usage recommandé
- **Recherche pédagogique**
- **Estimation préliminaire**
- **Exploration de systèmes**
- **Démonstrations scientifiques**

## 📚 Références

1. **Brunet, L., Caillard, J. & André, P.** *Thermodynamic calculation of n-component eutectic mixtures*. International Journal of Modern Physics C 15, 675–687 (2004).

2. **Newton-Raphson method** pour systèmes non-linéaires

3. **Thermodynamique des mélanges** - Équilibres liquide-solide

## 🛠️ Développement

### Structure du projet
```
eutec/
├── index.html          # Application principale
├── README.md          # Documentation
└── [autres fichiers]
```

### Algorithme principal
```javascript
// Newton-Raphson avec sous-relaxation (10%)
// Matrice jacobienne pour système n×n
// Convergence: résidu < 0.00001
// Maximum 100 itérations
```

## 📄 Licence

Cette application est fournie "en l'état" à des fins éducatives et de recherche. 

**Aucune garantie** n'est fournie quant à l'exactitude des résultats. **Validation expérimentale recommandée** pour tout usage scientifique ou industriel.

---

*🤖 Généré avec [Claude Code](https://claude.ai/code) - Assistant IA pour le développement*