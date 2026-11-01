# TP_AI_AGENTIC
# TP 5 : AI Agentique — Implémentation d'un Agent avec LangChain & LangGraph

Ce projet présente l'implémentation et l'expérimentation pratique d'un agent conversationnel et autonome utilisant les bibliothèques **LangChain** et **LangGraph**. L'objectif est de passer d'un simple modèle réactif sans état à un système agentique capable de mémoriser, d'utiliser des outils externes, d'exécuter du code, d'interroger des bases de connaissances (RAG) et d'appliquer des mécanismes de sécurité rigoureux.

---

## 👥 Auteurs & Encadrement

* **Réalisé par :** Ahlame Laquad & Nassima Doghmi
* **Filière :** Master 2 AIDC (Intelligence Artificielle et Données Connaissance)
* **Établissement :** Université Sultan Moulay Slimane — Faculté des Sciences / Département d'Informatique, Béni Mellal
* **Encadré par :** Pr. Lhoussaine Daoudi
* **Année Universitaire :** 2026 - 2027

---

## 🚀 Fonctionnalités & Notions Abordées

1. **Création d'agents conversationnels :**
   - Mise en œuvre d'un agent simple sans mémoire.
   - Gestion dynamique du contexte et sélection du modèle selon la complexité.

2. **Gestion de la mémoire et persistance :**
   - Persistance volatile en mémoire vive avec `MemorySaver`.
   - Persistance relationnelle multi-threads avec `PostgresSaver`.

3. **Utilisation d'outils (Tool Calling) :**
   - Création de fonctions personnalisées décorées avec `@tool`.
   - Recherche sur le web en temps réel avec **DuckDuckGo** et **Tavily**.
   - Exécution de code et résolution mathématique (SymPy / NumPy) via `PythonREPL`.

4. **Architecture RAG (Retrieval-Augmented Generation) :**
   - Intégration de modèles de plongement vectoriel locaux avec **Hugging Face**.
   - Recherche de similarité vectorielle avec indexation **FAISS**.

5. **Contrôle & Robustesse :**
   - Injection dynamique de *System Prompts* selon le profil de l'utilisateur.
   - Réponses structurées avec validation de types (Pydantic).
   - Middlewares personnalisés pour le tracing temporel et la gestion élégante des erreurs d'outils.

6. **Sécurité & Human-in-the-Loop (HITL) :**
   - Mise en place de garde-fous (*Guardrails*) pour bloquer les requêtes inappropriées.
   - Filtrage et protection des données personnelles sensibles (PII).
   - Validation humaine (*Human-in-the-Loop*) avant l'exécution d'actions critiques (envoi d'e-mails, paiements).

---

## 🛠️ Prérequis et Installation

Le projet utilise le gestionnaire d'environnement moderne **uv** (ou pip).

### 1. Cloner le dépôt
```bash
git clone [https://github.com/Missesqueensy/TP_AI_AGENTIC.git](https://github.com/Missesqueensy/TP_AI_AGENTIC.git)
cd TP_AI_AGENTIC
