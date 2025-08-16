# 🏦 Détection de Fraudes Bancaires — Challenge IA/Data IBM x Télécom Paris

Ce dépôt contient le code et la méthodologie développés dans le cadre du **challenge IA/Data IBM x Télécom Paris**, dont l’objectif était de **détecter les transactions bancaires frauduleuses** parmi un large volume d’opérations.

L'ensemble des données utilisées durant ce challenge est confidentiel et n'est donc pas mis à dispoisition sur le dépôt.

---

## 🎯 Objectif

- Identifier automatiquement les transactions frauduleuses à partir d’un dataset massif d’opérations bancaires.  
- Construire des **features numériques pertinentes** reflétant les comportements suspects.  
- Entraîner un modèle de **Random Forest** robuste au bruit généré par ces *handcrafted features*.  

---

## 🛠️ Méthodologie

### 1. Prétraitement des données
- Nettoyage des transactions (valeurs manquantes, normalisation).  
- Agrégation de signaux comportementaux (fréquence d’achat, montants moyens, variance, etc.).  
- Encodage des variables catégorielles.

### 2. Feature engineering
- Conception de **features statistiques** (moyenne, écart-type par utilisateur, historique des montants).  
- Détection de **patterns temporels** (heures inhabituelles, transactions rapides en rafale).  

### 3. Modélisation
- Utilisation d’un **Random Forest Classifier** pour sa robustesse au bruit et sa capacité à gérer des features hétérogènes.  
- Optimisation par **Grid Search** et **validation croisée**.  
- Gestion du déséquilibre de classes via :  
  - sur-échantillonnage (SMOTE),  
  - pondération des classes dans l’algorithme.  

### 4. Évaluation
- Métriques principales : **AUC-ROC**, **Precision-Recall**, **F1-score**.  
- Importance des variables pour interpréter les facteurs clés de détection.  

