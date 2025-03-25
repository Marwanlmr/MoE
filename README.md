# 🧠 Mixture of Experts (MoE) – Classification Multi-Classe avec LLMs

> Architecture basée sur des experts spécialisés, pour une classification fine et contrôlée à l’aide de modèles de langage.

---

## 🚧 État du projet

🛠️ **En cours de construction**  
Ce projet est en développement actif. Les premières briques fonctionnelles sont en place :
- ✅ Fine-tuning d'experts One-vs-All avec différents LLMs
- ✅ Système d'inférence MoE avec gating soft
- 🔜 Intégration du seuil EER et système de rejet
- 🔜 Comparaison avec un classifieur global

---

## 📌 Objectif

Construire un système de classification multi-classe en NLP en s'appuyant sur une architecture **Mixture of Experts** :
- Un modèle expert **par classe**
- Chacun entraîné en **classification binaire**
- Prise de décision via un **mécanisme de gating** inspiré des approches récentes (gating soft)

---

## 🧱 Structure du MoE

- **3 classes cibles** extraites du dataset :  
  `Food and Entertaining`, `Home and Garden`, `Personal Care and Style`
- **3 experts spécialisés** :
  - `bert-base-uncased`
  - `distilbert-base-uncased`
  - `roberta-base`
- **Entraînement individuel** via HuggingFace `Trainer`
- **Prédiction finale** basée sur pondération dynamique des scores (longueur du texte)

---

## 🗂️ Contenu du projet

