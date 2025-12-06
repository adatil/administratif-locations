# Guide de Contribution

Merci de votre intérêt pour contribuer à **Administratif Locations** ! Ce document vous guidera dans le processus de contribution.

## 📋 Table des Matières

- [Code de Conduite](#code-de-conduite)
- [Comment Contribuer](#comment-contribuer)
- [Signaler un Bug](#signaler-un-bug)
- [Proposer une Fonctionnalité](#proposer-une-fonctionnalité)
- [Processus de Pull Request](#processus-de-pull-request)
- [Standards de Code](#standards-de-code)
- [Structure des Fichiers](#structure-des-fichiers)

## 🤝 Code de Conduite

Ce projet adhère à un code de conduite respectueux. En participant, vous vous engagez à :

- Être respectueux envers tous les contributeurs
- Accepter les critiques constructives
- Collaborer de manière positive
- Se concentrer sur ce qui est le mieux pour la communauté

## 🚀 Comment Contribuer

Il existe plusieurs façons de contribuer :

### 1. Signaler des Bugs
Trouvé un bug ? Aidez-nous à l'identifier et le corriger !

### 2. Proposer des Améliorations
Des idées pour améliorer les outils ? Partagez-les !

### 3. Améliorer la Documentation
La documentation peut toujours être améliorée, clarifiée ou traduite.

### 4. Écrire du Code
Corrigez des bugs, ajoutez des fonctionnalités, optimisez le code existant.

### 5. Tester
Testez les outils sur différents navigateurs et systèmes d'exploitation.

## 🐛 Signaler un Bug

Avant de signaler un bug :

1. **Vérifiez** que le bug n'a pas déjà été signalé dans les [Issues](https://github.com/adatil/administratif-locations/issues)
2. **Testez** avec la dernière version
3. **Reproduisez** le bug de manière cohérente

### Créer un rapport de bug

Utilisez le template suivant :

```markdown
**Description du bug**
Description claire et concise du problème.

**Comment reproduire**
1. Aller à '...'
2. Cliquer sur '...'
3. Remplir le champ '...'
4. Voir l'erreur

**Comportement attendu**
Ce qui devrait se passer normalement.

**Captures d'écran**
Si applicable, ajoutez des captures d'écran.

**Environnement**
- Navigateur : [ex. Chrome 120]
- OS : [ex. Windows 11]
- Fichier concerné : [ex. bail_mobilite_generator.html]

**Informations supplémentaires**
Tout autre contexte utile.
```

## 💡 Proposer une Fonctionnalité

Avant de proposer une fonctionnalité :

1. **Vérifiez** qu'elle n'est pas déjà proposée ou en cours
2. **Réfléchissez** à son utilité pour la majorité des utilisateurs
3. **Décrivez** clairement le cas d'usage

### Template de proposition

```markdown
**Problème résolu**
Quel problème cette fonctionnalité résout-elle ?

**Solution proposée**
Description claire de la fonctionnalité.

**Alternatives considérées**
Autres solutions envisagées.

**Informations supplémentaires**
Mockups, exemples, références...
```

## 🔄 Processus de Pull Request

### 1. Fork et Clone

```bash
# Fork via l'interface GitHub
# Puis cloner votre fork
git clone https://github.com/VOTRE-USERNAME/administratif-locations.git
cd administratif-locations
```

### 2. Créer une Branche

```bash
# Créer une branche descriptive
git checkout -b feature/nom-fonctionnalite
# ou
git checkout -b fix/nom-bug
```

### 3. Faire vos Modifications

- Respectez les [Standards de Code](#standards-de-code)
- Testez vos changements sur plusieurs navigateurs
- Documentez les nouvelles fonctionnalités

### 4. Commit

```bash
# Commits atomiques avec messages clairs
git add .
git commit -m "feat: ajout générateur de bail commercial"
# ou
git commit -m "fix: correction calcul quittance"
```

**Convention de messages de commit :**

- `feat:` Nouvelle fonctionnalité
- `fix:` Correction de bug
- `docs:` Documentation
- `style:` Formatage, style (pas de changement de code)
- `refactor:` Refactoring
- `test:` Ajout de tests
- `chore:` Maintenance

### 5. Push et Pull Request

```bash
# Push vers votre fork
git push origin feature/nom-fonctionnalite
```

Puis créez une Pull Request via l'interface GitHub.

### Checklist PR

- [ ] Le code fonctionne sur Chrome, Firefox, Safari et Edge
- [ ] Le code est commenté si nécessaire
- [ ] La documentation est mise à jour
- [ ] Les fichiers sont testés en impression/PDF
- [ ] Pas de console.log() ou code de debug
- [ ] Le style CSS est cohérent avec l'existant
- [ ] Les formulaires sont accessibles (labels, placeholders)

## 📝 Standards de Code

### HTML

```html
<!-- Utilisez une indentation de 4 espaces -->
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Titre Descriptif</title>
</head>
<body>
    <!-- Contenu bien structuré -->
</body>
</html>
```

### CSS

```css
/* Organisez par sections */
/* --- Section principale --- */
.container {
    max-width: 1200px;
    margin: 0 auto;
}

/* Classes descriptives */
.section-title {
    font-size: 18px;
    color: #2c3e50;
}

/* Media queries à la fin */
@media print {
    .no-print {
        display: none;
    }
}
```

### JavaScript

```javascript
// Utilisez des noms de variables descriptifs
function generateDocument() {
    const formData = collectFormData();
    const preview = document.getElementById('preview');

    // Commentez les sections complexes
    preview.innerHTML = generateHTML(formData);
}

// Évitez var, utilisez const/let
const API_URL = 'https://example.com';
let userInput = '';

// Fonctions pures quand possible
function calculateTotal(items) {
    return items.reduce((sum, item) => sum + item.price, 0);
}
```

### Bonnes Pratiques

1. **Accessibilité**
   - Utilisez des labels pour tous les inputs
   - Alt text pour les images
   - Contraste suffisant pour les couleurs

2. **Performance**
   - Minimisez les fichiers avant production
   - Optimisez les images
   - Évitez les bibliothèques externes si possible

3. **Compatibilité**
   - Testez sur navigateurs modernes
   - Utilisez des polyfills si nécessaire
   - Vérifiez le mode responsive

4. **Sécurité**
   - Validez les entrées utilisateur
   - Échappez les contenus HTML dynamiques
   - Pas de eval() ou innerHTML non sécurisé

## 📁 Structure des Fichiers

Chaque générateur suit cette structure :

```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <!-- Métadonnées -->
    <title>Générateur de...</title>

    <style>
        /* Styles CSS intégrés */
    </style>
</head>
<body>
    <div class="container">
        <!-- En-tête -->
        <div class="header">...</div>

        <!-- Mode édition (formulaires) -->
        <div class="edit-mode">
            <div class="section">...</div>
        </div>

        <!-- Mode aperçu -->
        <div class="preview-mode">...</div>

        <!-- Boutons d'action -->
        <div class="buttons">...</div>
    </div>

    <script>
        // JavaScript pour la logique
    </script>
</body>
</html>
```

## 🧪 Tests

Avant de soumettre :

### Tests Manuels

1. **Fonctionnalité**
   - [ ] Remplir tous les champs
   - [ ] Tester les validations
   - [ ] Générer l'aperçu
   - [ ] Sauvegarder les données
   - [ ] Charger des données sauvegardées

2. **Impression**
   - [ ] Aperçu avant impression (Ctrl+P)
   - [ ] Mise en page correcte
   - [ ] Pas d'éléments UI dans l'impression
   - [ ] Export PDF fonctionnel

3. **Navigateurs**
   - [ ] Chrome (dernière version)
   - [ ] Firefox (dernière version)
   - [ ] Safari (si disponible)
   - [ ] Edge (dernière version)

4. **Responsive**
   - [ ] Mobile (< 768px)
   - [ ] Tablette (768-1024px)
   - [ ] Desktop (> 1024px)

## 🎨 Conventions de Design

### Palette de Couleurs

Chaque type de document a sa couleur distinctive :

- **Baux** : Bleu (`#2c3e50`, `#3498db`)
- **États des lieux** : Violet (`#9b59b6`, `#8e44ad`)
- **Quittances** : Vert (`#27ae60`, `#2ecc71`)
- **Inventaires** : Violet (`#9b59b6`)
- **Documents divers** : Orange (`#e67e22`, `#d35400`)

### Typographie

- Police principale : `'Segoe UI', Tahoma, Geneva, Verdana, sans-serif`
- Titres : `28px` (H1), `20px` (H2), `18px` (H3)
- Corps de texte : `14px`
- Labels : `14px`, `font-weight: 600`

## 📞 Questions ?

- **Documentation** : Consultez le [README.md](README.md)
- **Discussions** : Utilisez les [GitHub Discussions](https://github.com/adatil/administratif-locations/discussions)
- **Issues** : Pour les bugs et fonctionnalités

## 🙏 Remerciements

Merci de contribuer à améliorer **Administratif Locations** !

Votre temps et vos efforts sont grandement appréciés.

---

**Ensemble, simplifions la gestion locative !**
