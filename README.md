# Administratif Locations

> Suite d'outils web pour la gestion administrative des locations immobilières

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![HTML](https://img.shields.io/badge/HTML-5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

## 📋 Description

**Administratif Locations** est une collection d'outils web autonomes conçus pour simplifier la gestion administrative des locations immobilières. Chaque outil est un fichier HTML standalone qui fonctionne directement dans votre navigateur, sans installation ni serveur requis.

Ces générateurs permettent de créer rapidement et facilement tous les documents administratifs nécessaires pour la gestion locative : baux, états des lieux, quittances, inventaires, etc.

## ✨ Fonctionnalités

### 📄 Générateurs de Baux

#### 🆕 Versions Améliorées (Recommandées)

- **`bail_civil_generator_v2.html`** ⭐ **NOUVEAU**
  Version améliorée du bail civil avec fonctionnalités avancées
  - ✅ Validation intelligente des formulaires
  - 💾 Sauvegarde automatique (localStorage)
  - 📊 Barre de progression
  - ⚠️ Vérification de cohérence (loyer, charges, dépôt)
  - 🌓 Mode sombre
  - 📥 Export PDF natif
  - ℹ️ Tooltips informatifs
  - 📋 Templates pré-remplis
  - ♿ Accessibilité WCAG 2.1
  - 📱 Design responsive optimisé

- **`bail_mobilite_generator_v2.html`** ⭐ **NOUVEAU**
  Version améliorée du bail mobilité avec fonctionnalités avancées
  - ✅ Bug JS corrigé (fonction dans CSS)
  - ✅ Toutes les améliorations du bail civil
  - ✍️ Signature électronique (canvas)
  - 🔢 Fonction numberToWords complète (0-999999)

- **`bail_meuble_courte_duree_v2.html`** ⭐ **NOUVEAU**
  Contrat générique de location meublée courte durée
  - 🎨 Interface bleue distinctive
  - 📝 Sans cadre légal spécifique (ni mobilité, ni civil)
  - 💰 Dépôt de garantie optionnel (non limité)
  - ⏰ Durée et conditions librement définies
  - ✅ Toutes les améliorations V2 (dark mode, auto-save, PDF)
  - 🔧 Adapté aux locations flexibles hors cadres légaux stricts

> 📖 **Voir [AMELIORATIONS.md](AMELIORATIONS.md)** pour le détail complet des améliorations

#### Versions Originales

- **`bail_civil_html_completable.html`** (44 KB)
  Générateur de bail civil pour résidence secondaire
  - Formulaire complet et guidé
  - Génération automatique du contrat
  - Impression et sauvegarde PDF

- **`bail_mobilite_generator.html`** (70 KB)
  Générateur de bail mobilité (1 à 10 mois)
  - Conforme à la loi ELAN
  - Motifs légaux prédéfinis (études, stage, mutation, etc.)
  - Durée limitée sans renouvellement tacite

### 🏠 États des Lieux

Plusieurs versions disponibles selon vos besoins :

- **`Etat-deslieux`** (60 KB)
  Générateur complet d'état des lieux d'entrée et de sortie
  - Sélection rapide des pièces courantes
  - Description détaillée par élément (sols, murs, plafond, etc.)
  - Relevés de compteurs
  - Gestion des clés
  - Mode aperçu avant impression

- **`generateur_etat_lieux.html`** (49 KB)
  Version alternative avec interface épurée

- **`etat_lieux_checkboxes.html`** (55 KB)
  Version avec cases à cocher pour remplissage rapide

- **`etatdeslieux.html`** (14 KB)
  Version légère et minimaliste

### 📦 Inventaires de Meubles

- **`inventaire-generator-fixed.html`** (51 KB)
  Générateur d'inventaire pour locations meublées
  - Organisation par pièces
  - Description, quantité et état
  - Calcul automatique des totaux
  - Export et sauvegarde

- **`inventaire_meubles_cases.html`** (59 KB)
  Version avec cases à cocher et catégories prédéfinies

### 💰 Gestion des Paiements

- **`generateur_quittance.html`** (44 KB)
  Générateur de quittances de loyer
  - Calcul automatique du total
  - Détail des charges
  - Génération mensuelle
  - Format professionnel prêt à imprimer

### 📋 Dossier de Location

- **`pieces_justificatives_locataire.html`** (47 KB)
  Liste des pièces justificatives pour dossier de location
  - Conforme à la réglementation
  - Checklist complète (locataire, garant, documents légaux)
  - Aide au montage de dossier

## 🚀 Installation et Utilisation

### Prérequis
Aucun ! Ces outils fonctionnent dans tout navigateur web moderne (Chrome, Firefox, Safari, Edge).

### Installation

**Option 1 : Téléchargement direct**
```bash
# Cloner le dépôt
git clone https://github.com/adatil/administratif-locations.git

# Accéder au dossier
cd administratif-locations
```

**Option 2 : Téléchargement ZIP**
1. Téléchargez le ZIP depuis GitHub
2. Extrayez les fichiers
3. Ouvrez les fichiers HTML directement

### Utilisation

1. **Ouvrez le fichier HTML** dans votre navigateur (double-clic ou Fichier > Ouvrir)
2. **Remplissez le formulaire** avec les informations demandées
3. **Prévisualisez** le document généré
4. **Imprimez** ou **sauvegardez en PDF** (Ctrl+P / Cmd+P)
5. **Sauvegardez vos données** (format JSON) pour réutilisation ultérieure

### Exemple : Créer un état des lieux

```bash
# 1. Ouvrir le fichier
open Etat-deslieux  # macOS
# ou
start Etat-deslieux  # Windows
# ou simplement double-cliquer sur le fichier
```

1. Sélectionnez le type (entrée ou sortie)
2. Remplissez les informations du logement et des participants
3. Cochez les pièces à inclure (Salon, Cuisine, Chambres, etc.)
4. Cliquez sur "Générer les pièces sélectionnées"
5. Complétez l'état de chaque élément
6. Cliquez sur "Aperçu" puis "Imprimer"

## 📁 Structure du Projet

```
administratif-locations/
├── README.md                              # Ce fichier
├── LICENSE                                # Licence MIT
├── CONTRIBUTING.md                        # Guide de contribution
│
├── Baux/
│   ├── bail_civil_html_completable.html  # Bail civil
│   └── bail_mobilite_generator.html      # Bail mobilité
│
├── États des lieux/
│   ├── Etat-deslieux                     # Version complète
│   ├── generateur_etat_lieux.html        # Version alternative
│   ├── etat_lieux_checkboxes.html        # Version cases à cocher
│   └── etatdeslieux.html                 # Version légère
│
├── Inventaires/
│   ├── inventaire-generator-fixed.html   # Générateur principal
│   └── inventaire_meubles_cases.html     # Version avec cases
│
├── Paiements/
│   └── generateur_quittance.html         # Quittances de loyer
│
└── Dossiers/
    └── pieces_justificatives_locataire.html  # Checklist pièces justif.
```

## 💡 Conseils d'Utilisation

### Sauvegarde des Données
- Utilisez la fonction "Sauvegarder" pour exporter vos données au format JSON
- Conservez ces fichiers pour réutilisation (comparaison état des lieux entrée/sortie)
- Nommage conseillé : `etat_lieux_entree_2024-01-15.json`

### Archivage
- Sauvegardez les documents générés en PDF
- Conservez les états des lieux pendant toute la durée du bail + 5 ans
- Stockez les quittances pendant minimum 3 ans

### Personnalisation
Les fichiers HTML peuvent être personnalisés :
- Modifier les couleurs et styles CSS
- Ajouter votre logo
- Adapter les formulaires à vos besoins

## 🔧 Compatibilité

| Navigateur | Version minimale | Support |
|------------|------------------|---------|
| Chrome     | 90+              | ✅ Complet |
| Firefox    | 88+              | ✅ Complet |
| Safari     | 14+              | ✅ Complet |
| Edge       | 90+              | ✅ Complet |
| Opera      | 76+              | ✅ Complet |

**Testé sur :**
- Windows 10/11
- macOS 11+
- Linux (Ubuntu, Debian)
- iOS 14+
- Android 10+

## 🤝 Contribution

Les contributions sont les bienvenues ! Consultez [CONTRIBUTING.md](CONTRIBUTING.md) pour plus de détails.

### Comment contribuer
1. Fork le projet
2. Créez une branche (`git checkout -b feature/amelioration`)
3. Commit vos changements (`git commit -m 'Ajout nouvelle fonctionnalité'`)
4. Push vers la branche (`git push origin feature/amelioration`)
5. Ouvrez une Pull Request

## 📝 Licence

Ce projet est sous licence MIT - voir le fichier [LICENSE](LICENSE) pour plus de détails.

## 📞 Support

- 🐛 **Bugs** : Ouvrez une [issue](https://github.com/adatil/administratif-locations/issues)
- 💡 **Suggestions** : Partagez vos idées via les [discussions](https://github.com/adatil/administratif-locations/discussions)
- 📧 **Contact** : Pour toute question spécifique

## ⚖️ Avertissement Légal

Ces outils sont fournis à titre informatif et d'aide à la gestion administrative. Les documents générés doivent être vérifiés et adaptés selon :
- La législation en vigueur dans votre pays/région
- Votre situation spécifique
- Les conseils d'un professionnel du droit si nécessaire

Les auteurs ne sauraient être tenus responsables de l'utilisation de ces outils ou des documents générés.

## 🌟 Fonctionnalités à Venir

- [ ] Export direct en PDF sans impression
- [ ] Templates personnalisables
- [ ] Mode multi-langues (EN, ES, IT)
- [ ] Application mobile
- [ ] Synchronisation cloud
- [ ] Générateur de contrat de colocation
- [ ] Calcul automatique de révision de loyer
- [ ] Générateur d'avis d'échéance

## 📊 Statistiques

- **10 outils** disponibles
- **~500 KB** au total
- **100% autonome** (pas de dépendances externes)
- **0 serveur** requis
- **Gratuit** et open-source

## 🙏 Remerciements

Merci à tous les contributeurs qui rendent ce projet possible !

---

**Fait avec ❤️ pour simplifier la gestion locative**

*Dernière mise à jour : Décembre 2024*
