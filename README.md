# Mixture of Experts (MoE) – Classification Multi-Classe avec LLMs

![Project Status](https://img.shields.io/badge/status-en%20construction-yellow)
![LLM](https://img.shields.io/badge/model-BERT%2C%20DistilBERT%2C%20RoBERTa-purple)
![HuggingFace](https://img.shields.io/badge/framework-HuggingFace%20Transformers%20Pytorch-blue)

> Système de classification multi-classe basé sur une architecture Mixture of Experts (MoE), combinant plusieurs modèles de langage spécialisés.

---

## État du projet

Ce projet est **en cours de développement**. Il repose sur une approche One-vs-All avec un expert (LLM) par classe.

Fonctionnalités mises en place :
- Entraînement d'experts binaires (un par classe)
- Fonction d'inférence MoE avec gating soft basé sur la longueur du texte

Fonctionnalités prévues :
- Calcul du seuil optimal par expert (EER)
- Mécanisme de rejet si aucune classe n'est suffisamment probable
- Comparaison avec un classifieur multitâche unique

---

## Objectif

L'objectif est de construire un classifieur multi-classe composé de plusieurs experts indépendants.  
Chaque expert est un modèle de langage pré-entraîné, fine-tuné sur la détection d'une classe spécifique (One-vs-All).  
L’inférence finale repose sur la combinaison pondérée des sorties des experts.

---

## Détails des experts

| Classe                    | Modèle utilisé           |
|---------------------------|---------------------------|
| Food and Entertaining     | `bert-base-uncased`       |
| Home and Garden           | `distilbert-base-uncased` |
| Personal Care and Style   | `roberta-base`            |

---

## Contenu du projet

