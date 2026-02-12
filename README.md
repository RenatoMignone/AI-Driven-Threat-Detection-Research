# AI-Driven Threat Detection Research

![Polito Logo](https://github.com/RenatoMignone/attack-tactic-recognition-nlp/blob/main/resources/logo_polito.jpg?raw=true)

This repository serves as the central hub for the research and laboratory activities conducted during the **AI and Cybersecurity** course at **Politecnico di Torino**. It aggregates four distinct projects covering the intersection of Artificial Intelligence, Deep Learning, and Natural Language Processing applied to cybersecurity domains.

## Repository Structure

The projects are organized sequentially to guide the learner from foundational network flow analysis to complex malware and anomaly detection tasks.

| Order | Laboratory | Topic | Methods | Repository Link |
| :---: | :--- | :--- | :--- | :--- |
| **1** | **[01_Network_Flow_Analysis](01_Network_Flow_Analysis/)** | **Network Flow Classification** | Feed-Forward Neural Networks (FFNNs), Weighted Loss, Feature Bias Analysis | [Link](https://github.com/RenatoMignone/network-flow-classification-dl) |
| **2** | **[02_Malware_Analysis](02_Malware_Analysis/)** | **Malware Classification** | Dynamic API Analysis, RNNs (GRU/LSTM), Graph Neural Networks (GNNs) | [Link](https://github.com/RenatoMignone/malware-api-classification-dl) |
| **3** | **[03_Network_Anomaly_Detection](03_Network_Anomaly_Detection/)** | **Anomaly Detection (NIDS)** | One-Class SVM, Autoencoders (Reconstruction Error), Unsupervised Clustering | [Link](https://github.com/RenatoMignone/unsupervised-network-intrusion-detection) |
| **4** | **[04_NLP_for_Cybersecurity](04_NLP_for_Cybersecurity/)** | **NLP for Cybersecurity** | Bash Command Classification, TF-IDF, Word2Vec, LSTMs for Tactics detection | [Link](https://github.com/RenatoMignone/attack-tactic-recognition-nlp) |

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

## Research Hub Overview

### 1. [Network Flow Classification](01_Network_Flow_Analysis/)
**Goal**: Classify network flows (Benign vs Malicious) using Deep Learning on the CICIDS2017 dataset.

This module focuses on the **full modelling pipeline** for tabular network data. It investigates how **Feed-Forward Neural Networks (FFNNs)** perform against baselines and explores critical real-world issues like **class imbalance** and **bias**.
- **Key Experiments**:
    - **Baseline Models**: Shallow FFNNs with varying architectures.
    - **Bias Analysis**: Investigating disparate impact of features like `Destination Port`.
    - **Deep Learning**: Deeper FFNNs (3-6 layers) with hyperparameter tuning.
    - **Regularization**: Application of Dropout, Batch Normalization, and Weight Decay.

### 2. [Malware Analysis](02_Malware_Analysis/)
**Goal**: Classify malware families based on dynamic API-call traces.

This project tackles the complexity of sequential data in malware analysis. By treating **API call traces** as sequences or graphs, we leverage advanced architectures to identify malicious behavior patterns.
- **Key Experiments**:
    - **Feature Exploration**: Frequency-based analysis of API calls.
    - **Sequence Modeling**: Using **LSTMs** and **GRUs** to capture temporal dependencies in execution traces.
    - **Graph Learning**: Representing traces as graphs and applying **GraphSAGE** and **GCNs** to learn structural features of malware execution.

### 3. [Network Anomaly Detection](03_Network_Anomaly_Detection/)
**Goal**: Detect zero-day attacks in network traffic using unsupervised approaches.

Simulating a scenario where attack labels are unavailable, this lab applies **unsupervised** and **semi-supervised** learning to detect intrusions as anomalies.
- **Key Experiments**:
    - **Shallow Anomaly Detection**: **One-Class SVM (OC-SVM)** for outlier detection.
    - **Deep Anomaly Detection**: **Autoencoders** that flag anomalies based on high reconstruction error.
    - **Clustering**: using **DBSCAN** and **K-Means** to group similar traffic patterns and isolate attacks.
    - **Visualization**: Dimensionality reduction with **t-SNE** and **PCA**.

### 4. [NLP for Attack Tactic Recognition](04_NLP_for_Cybersecurity/)
**Goal**: Identify attacker intent (Tactics) from Bash command history.

Bridging the gap between **Natural Language Processing (NLP)** and cybersecurity, this module classifies raw bash commands into **MITRE ATT&CK tactics** (e.g., *Discovery, Persistence, Execution*).
- **Key Experiments**:
    - **Text Preprocessing**: Custom tokenization for shell commands.
    - **Embeddings**: **TF-IDF** for keyword extraction and **Word2Vec** for semantic representation of commands.
    - **Sequential Classification**: **Bidirectional LSTMs** to understand the intent behind a sequence of commands.
    - **Interpretability**: Analyze confusion matrices to understand model decisions.

## Authors & Contributors

This work is the result of a collaborative effort by the following team:

| Name | GitHub | LinkedIn | Email |
| :--- | :--- | :--- | :--- |
| **Renato Mignone** | [![GitHub](https://img.shields.io/badge/GitHub-Profile-informational?logo=github)](https://github.com/RenatoMignone) | [![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?logo=linkedin)](https://www.linkedin.com/in/renato-mignone/) | [renato.mignone@studenti.polito.it](mailto:renato.mignone@studenti.polito.it) |
| **Claudia Sanna** | [![GitHub](https://img.shields.io/badge/GitHub-Profile-informational?logo=github)](https://github.com/sannaclaudia) | [![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?logo=linkedin)](https://www.linkedin.com/in/claudiasanna1/) | [claudia.sanna@studenti.polito.it](mailto:claudia.sanna@studenti.polito.it) |
| **Chiara Iorio** | [![GitHub](https://img.shields.io/badge/GitHub-Profile-informational?logo=github)](https://github.com/iochia02) | [![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-blue?logo=linkedin)](https://www.linkedin.com/) | [chiara.iorio@studenti.polito.it](mailto:chiara.iorio@studenti.polito.it) |