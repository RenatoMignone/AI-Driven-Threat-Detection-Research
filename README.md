# AI-Driven Threat Detection Research

![Polito Logo](https://github.com/RenatoMignone/attack-tactic-recognition-nlp/blob/main/resources/logo_polito.jpg?raw=true)

This repository serves as the central hub for the research and laboratory activities conducted during the **AI and Cybersecurity** course at **Politecnico di Torino**. It aggregates four distinct projects covering the intersection of Artificial Intelligence, Deep Learning, and Natural Language Processing applied to cybersecurity domains.

## Repository Structure

The projects are organized sequentially to guide the learner from foundational network flow analysis to complex malware and anomaly detection tasks.

| Order | Laboratory | Topic | Methods |
| :---: | :--- | :--- | :--- |
| **1** | **[01_Network_Flow_Analysis](01_Network_Flow_Analysis/)** | **Network Flow Classification** | Feed-Forward Neural Networks (FFNNs), Weighted Loss, Feature Bias Analysis |
| **2** | **[02_Malware_Analysis](02_Malware_Analysis/)** | **Malware Classification** | Dynamic API Analysis, RNNs (GRU/LSTM), Graph Neural Networks (GNNs) |
| **3** | **[03_Network_Anomaly_Detection](03_Network_Anomaly_Detection/)** | **Anomaly Detection (NIDS)** | One-Class SVM, Autoencoders (Reconstruction Error), Unsupervised Clustering |
| **4** | **[04_NLP_for_Cybersecurity](04_NLP_for_Cybersecurity/)** | **NLP for Cybersecurity** | Bash Command Classification, TF-IDF, Word2Vec, LSTMs for Tactics detection |

> **Note**: Each folder above is a submodule linked to its respective standalone repository. To clone them all, use `git clone --recursive`.

## Getting Started

To clone this repository along with all its submodules (laboratories), use the `--recursive` flag:

```bash
git clone --recursive https://github.com/RenatoMignone/AI-Driven-Threat-Detection-Research.git
```

If you have already cloned the repository without submodules, run:

```bash
git submodule update --init --recursive
```

## Research Overview

### 1. [Network Flow Classification](01_Network_Flow_Analysis/)
**Goal**: Classify network flows (Benign vs Malicious) using Deep Learning on the CICIDS2017 dataset.
- **Key Techniques**: Data cleaning & EDA, Handling class imbalance, deep FFNNs dynamics, and regularization (Dropout, BatchNorm, Weight Decay).

### 2. [Malware Analysis](02_Malware_Analysis/)
**Goal**: Classify malware families based on dynamic API-call traces.
- **Key Techniques**: Sequence modeling with RNNs (BiLSTM, GRU), Graph representation learning (GraphSAGE, GNNs) on API-call graphs.

### 3. [Network Anomaly Detection](03_Network_Anomaly_Detection/)
**Goal**: Detect zero-day attacks in network traffic using unsupervised approaches.
- **Key Techniques**: Semi-supervised One-Class SVM, Deep Autoencoders for anomaly scoring, Clustering (DBSCAN, K-Means) for attack patterns.

### 4. [NLP for Attack Tactic Recognition](04_NLP_for_Cybersecurity/)
**Goal**: Identify attacker intent (Tactics) from Bash command history.
- **Key Techniques**: Tokenization & Text Preprocessing, Embeddings (Word2Vec), Sequence classification with LSTMs to map commands to MITRE ATT&CK tactics.

## Authors & Contributors

This work is the result of a collaborative effort by:

| Name | GitHub | LinkedIn | Email |
| :--- | :--- | :--- | :--- |
| **Renato Mignone** | [![GitHub](https://img.shields.io/badge/GitHub-Profile-informational?logo=github)](https://github.com/RenatoMignone) | [![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?logo=linkedin)](https://www.linkedin.com/in/renato-mignone/) | [renato.mignone@studenti.polito.it](mailto:renato.mignone@studenti.polito.it) |
| **Claudia Sanna** | [![GitHub](https://img.shields.io/badge/GitHub-Profile-informational?logo=github)](https://github.com/sannaclaudia) | [![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?logo=linkedin)](https://www.linkedin.com/in/claudiasanna1/) | [claudia.sanna@studenti.polito.it](mailto:claudia.sanna@studenti.polito.it) |
| **Chiara Iorio** | [![GitHub](https://img.shields.io/badge/GitHub-Profile-informational?logo=github)](https://github.com/iochia02) | [![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?logo=linkedin)](https://www.linkedin.com/) | [chiara.iorio@studenti.polito.it](mailto:chiara.iorio@studenti.polito.it) |