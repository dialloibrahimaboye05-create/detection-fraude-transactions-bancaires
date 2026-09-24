# Détection de fraude - Transactions bancaires

## Contexte
Analyse d'un dataset de transactions bancaires (scénario) pour identifier 
des patterns liés aux transactions suspectes et frauduleuses.

## Données
- 5382 transactions, 9 colonnes
- Colonnes : ID Clients, Numero de compte, Identifiant operation, 
  Type de transaction, Status operation, Localisation, Date, Montant, Target
- Aucune valeur manquante

## Outils utilisés
- Python (pandas, matplotlib)
- Jupyter Notebook (VS Code)

## Résultats clés
- Répartition très déséquilibrée : environ 76% de transactions Normal, 
  20% Suspect, et seulement 4% Fraude — un déséquilibre typique des 
  problématiques réelles de détection de fraude
- Les transactions frauduleuses ont un montant moyen d'environ 1 182 637, 
  soit presque 5x plus élevé que les transactions normales (~239 140) 
  et 3.6x plus élevé que les suspectes (~324 368) — le montant semble 
  être un indicateur fort de risque
- La répartition géographique varie fortement selon la localisation 
  (ex. Ziguinchor concentre un nombre significatif de transactions 
  suspectes/frauduleuses)

## Comment lancer le projet
1. Cloner ce dépôt
2. Installer les dépendances : `pip install pandas matplotlib`
3. Ouvrir `analyse.ipynb` dans VS Code ou Jupyter

## Pistes d'amélioration
- Construire un modèle de machine learning (classification) pour prédire 
  automatiquement le statut d'une transaction, en tenant compte du 
  déséquilibre des classes (ex. rééchantillonnage, pondération)
- Analyser les corrélations entre type de transaction, heure et fraude
- Identifier un seuil de montant à partir duquel le risque de fraude augmente