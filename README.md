# ⚽ PSG Hub

<div align="center">

**Application Android moderne pour suivre toutes les actualités du Paris Saint-Germain**

[![Kotlin](https://img.shields.io/badge/Kotlin-1.9.0-blue.svg)](https://kotlinlang.org)
[![Android](https://img.shields.io/badge/Android-24%2B-green.svg)](https://www.android.com)
[![Jetpack Compose](https://img.shields.io/badge/Jetpack%20Compose-Latest-orange.svg)](https://developer.android.com/jetpack/compose)
[![API](https://img.shields.io/badge/API-Football--Data.org-red.svg)](https://www.football-data.org/)

</div>

---

## 📱 À propos

PSG Hub est une application Android native développée avec **Jetpack Compose** qui permet aux fans du Paris Saint-Germain de suivre en temps réel :

- Les matchs (passés, à venir, en direct)
- L'effectif complet de l'équipe
- Les classements (Ligue 1 et Ligue des Champions)
- Les dernières actualités du club

L'application utilise l'API **Football-Data.org** pour récupérer les données en temps réel et offre une interface utilisateur moderne et intuitive.

---

## ✨ Fonctionnalités

### 🏠 Accueil
- Vue d'ensemble avec le dernier match et le prochain match
- Matchs en direct (si disponibles)
- Accès rapide aux différentes sections
- Informations clés du PSG (position en Ligue 1, meilleur buteur)

### ⚽ Matchs
- **Matchs à venir** : Liste complète des prochains matchs du PSG
- **Matchs en direct** : Suivi en temps réel des matchs en cours
- **Matchs passés** : Historique des matchs terminés avec scores
- Affichage des équipes adverses, dates, heures et résultats

### 👥 Effectif
- Liste complète des joueurs du PSG
- Informations détaillées (nom, position, numéro)
- Photos des joueurs
- Organisation par poste

### 🏆 Classement
- **Ligue 1** : Classement complet avec logos des équipes
- **Ligue des Champions** : Classement des groupes et phase finale
- Statistiques détaillées (points, matchs joués, victoires, nuls, défaites)
- Buts marqués et encaissés

### 📰 Actualités
- Fil d'actualité du PSG
- Articles récents du site officiel
- Mise à jour automatique

---

## 🛠️ Technologies utilisées

### Développement
- **Kotlin** : Langage de programmation
- **Jetpack Compose** : Framework UI moderne et déclaratif
- **Material Design 3** : Design system moderne
- **Retrofit** : Client HTTP pour les appels API REST
- **Coroutines** : Programmation asynchrone
- **ViewModel & StateFlow** : Gestion de l'état de l'application
- **Navigation Compose** : Navigation entre les écrans
- **Coil** : Chargement et mise en cache des images
- **Gson** : Sérialisation/désérialisation JSON

### Outils d'assistance
- **Perplexity AI** : Assistant IA utilisé pour l'aide au développement, la résolution de tâches complexes et le débogage d'erreurs

---

## 📋 Prérequis

- **Android Studio** : Hedgehog (2023.1.1) ou version supérieure
- **JDK** : Version 11 ou supérieure
- **Android SDK** : API 24 (Android 7.0) minimum
- **Gradle** : Version 8.0 ou supérieure

---

## 🚀 Installation

### 1. Cloner le projet

```bash
git clone https://github.com/votre-username/PSGhub.git
cd PSGhub
```

### 2. Ouvrir dans Android Studio

1. Ouvrez Android Studio
2. Sélectionnez **File → Open**
3. Choisissez le dossier du projet
4. Attendez la synchronisation Gradle

### 3. Compiler et lancer

1. Connectez un appareil Android ou lancez un émulateur
2. Cliquez sur **Run** (▶️) ou appuyez sur `Shift + F10`
3. L'application sera installée et lancée automatiquement

---

## 📁 Structure du projet

```
PSGhub/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/yanis/psghub/
│   │   │   │   ├── data/
│   │   │   │   │   ├── api/              # Services API (Retrofit)
│   │   │   │   │   │   ├── ApiConfig.kt
│   │   │   │   │   │   └── FootballApiService.kt
│   │   │   │   │   ├── model/            # Modèles de données
│   │   │   │   │   │   ├── Match.kt
│   │   │   │   │   │   ├── Player.kt
│   │   │   │   │   │   ├── TeamStatistics.kt
│   │   │   │   │   │   └── NewsItem.kt
│   │   │   │   │   └── repository/       # Repositories
│   │   │   │   │       ├── FootballRepository.kt
│   │   │   │   │       └── NewsRepository.kt
│   │   │   │   ├── ui/
│   │   │   │   │   ├── screens/          # Écrans de l'application
│   │   │   │   │   │   ├── HomeScreen.kt
│   │   │   │   │   │   ├── MatchesScreen.kt
│   │   │   │   │   │   ├── SquadScreen.kt
│   │   │   │   │   │   ├── StandingsScreen.kt
│   │   │   │   │   │   └── NewsScreen.kt
│   │   │   │   │   ├── components/       # Composants réutilisables
│   │   │   │   │   │   └── MatchCard.kt
│   │   │   │   │   ├── viewmodel/        # ViewModels
│   │   │   │   │   │   └── MainViewModel.kt
│   │   │   │   │   ├── navigation/       # Navigation
│   │   │   │   │   │   └── Screen.kt
│   │   │   │   │   ├── theme/            # Thème Material Design
│   │   │   │   │   │   └── Theme.kt
│   │   │   │   │   └── MainScreen.kt     # Navigation principale
│   │   │   │   └── MainActivity.kt       # Point d'entrée
│   │   │   └── res/                      # Ressources (images, layouts, etc.)
│   │   └── test/                         # Tests unitaires
│   └── build.gradle.kts                  # Configuration du module app
├── build.gradle.kts                      # Configuration du projet
├── gradle/
│   └── libs.versions.toml                # Catalogue des dépendances
├── settings.gradle.kts                    # Configuration Gradle
└── README.md                              # Ce fichier
```

---

## 🔧 Configuration

### API Football-Data.org

L'application utilise l'API **Football-Data.org** pour récupérer les données en temps réel. La clé API est déjà configurée dans le projet, vous n'avez rien à faire !

**Fonctionnalités de l'API :**
- ✅ **Plan gratuit** : 10 requêtes par minute
- ✅ Données en temps réel
- ✅ Classements, matchs, statistiques

**Limites du plan gratuit :**
- 10 requêtes par minute
- Données mises à jour toutes les 15 minutes
- Accès aux compétitions majeures (Ligue 1, LDC, etc.)

**Note** : L'application gère automatiquement les délais entre les requêtes pour respecter les limites de l'API.

### ⚠️ Limitations de l'API et affichage des menus

**Important** : En raison des limitations de l'API Football-Data.org (10 requêtes par minute), certains menus peuvent ne pas s'afficher immédiatement ou rester vides lors du premier lancement de l'application.

**Pourquoi certains menus sont vides ?**

L'application charge les données de manière séquentielle pour respecter les limites de l'API :
1. Les **matchs** sont chargés en premier
2. Les **classements** (Ligue 1 et LDC) sont chargés ensuite
3. L'**effectif** et les **actualités** sont chargés en arrière-plan

**Solutions :**
- ⏳ **Attendez quelques secondes** : Les données se chargent progressivement
- 🔄 **Utilisez le bouton de rafraîchissement** (🔄) dans les menus pour forcer le rechargement
- 🔁 **Fermez et rouvrez l'application** si certains menus restent vides après plusieurs secondes
- 📶 **Vérifiez votre connexion Internet** : Une connexion instable peut empêcher le chargement

**Menus prioritaires** (chargés en premier) :
- ✅ Accueil (dernier match, prochain match)
- ✅ Matchs
- ✅ Classement

**Menus secondaires** (chargés après) :
- ⏳ Effectif
- ⏳ Actualités

Si après 30 secondes certains menus sont toujours vides, cela peut indiquer :
- Une limite de l'API atteinte (attendez 1 minute avant de réessayer)
- Un problème de connexion Internet
- Une indisponibilité temporaire de l'API

---



---

## 🐛 Dépannage

### Certains menus ne s'affichent pas ou sont vides

**C'est normal !** En raison des limitations de l'API (10 requêtes par minute), les données se chargent progressivement :

1. ⏳ **Attendez 10-30 secondes** : Les menus se remplissent automatiquement
2. 🔄 **Utilisez le bouton de rafraîchissement** (🔄) dans la barre d'outils
3. 📱 **Fermez et rouvrez l'application** si certains menus restent vides
4. 🔁 **Attendez 1 minute** si vous avez atteint la limite de l'API, puis réessayez

**Ordre de chargement :**
- **Priorité 1** : Matchs et Classement (chargés immédiatement)
- **Priorité 2** : Effectif et Actualités (chargés en arrière-plan)

### L'application ne charge aucune donnée

1. Vérifiez votre connexion Internet
2. Vérifiez que vous n'avez pas dépassé la limite de 10 requêtes/minute de l'API
3. Attendez 1 minute (limite de l'API) puis réessayez
4. Consultez les logs dans Logcat (Android Studio) pour plus de détails

### Erreur de compilation

1. **Sync Gradle** : `File → Sync Project with Gradle Files`
2. **Invalidate Caches** : `File → Invalidate Caches... → Invalidate and Restart`
3. **Nettoyer le projet** : `Build → Clean Project`, puis `Build → Rebuild Project`

### L'émulateur ne répond pas

1. Fermez l'émulateur depuis le Device Manager
2. Redémarrez l'émulateur
3. Si le problème persiste, créez un nouvel AVD (Android Virtual Device)

