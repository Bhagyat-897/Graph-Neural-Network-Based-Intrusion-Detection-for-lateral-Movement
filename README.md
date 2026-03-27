
# Graph Neural Network Based Intrusion Detection System (GNN-IDS)

**Graph Neural Network (GNN)-based Intrusion Detection System** for detecting **lateral movement attacks** in enterprise networks by modeling network activity as a graph instead of isolated events.

---

## 📖 Overview
Traditional intrusion detection systems analyze events independently, making it difficult to detect multi-step attacks. This project models network traffic as a graph:
- **Nodes** → Hosts / sessions / flows  
- **Edges** → Communication between nodes  

This enables detection of hidden attack patterns using **Graph Neural Networks (GNNs)**.

---

## 🔍 Problem
- Signature-based systems detect only known attacks  
- Anomaly-based systems produce high false positives  
- Traditional systems fail to capture relationships between entities  

### ✅ Solution
- Graph-based modeling of network activity  
- Edge-level classification (connection-based detection)  
- Context-aware detection using GNNs  

---

## 🧠 Core Idea
- Represent network as a graph  
- Learn relationships between nodes  
- Classify edges as:
  - **Benign**
  - **Malicious (Lateral Movement)**  

---

## 🏗️ System Workflow
1. Data Collection (CIC-IDS2017 / Synthetic)
2. Data Preprocessing (cleaning, normalization, feature extraction)
3. Graph Construction (nodes & edges)
4. Model Training (GCN / GraphSAGE / GAT)
5. Edge Classification
6. Evaluation (Precision, Recall, F1, AUPRC)
7. Attack Graph Visualization (MulVAL)

---


## 📊 Dataset
**CIC-IDS2017**
- Real-world dataset with attacks: DoS, DDoS, Botnet, Brute Force, Web attacks  
- Features include flow duration, packet count, bytes, TCP flags  

**Synthetic Dataset**
- Used for testing and quick experimentation  

---

## ⚙️ Technologies
Python, PyTorch, PyTorch Geometric, Pandas, NumPy, Scikit-learn, NetworkX, Matplotlib, Graphviz, MulVAL

---

## 🤖 Models
- GCN (Graph Convolutional Network)
- GraphSAGE
- GAT (Graph Attention Network)

Training:
- Loss: BCEWithLogitsLoss  
- Optimizer: Adam  
- Task: Binary edge classification  

---

## 📈 Evaluation Metrics
Precision, Recall, F1-score, ROC-AUC, AUPRC

---

## 📊 Results
- High Recall (~0.84) → detects most attacks  
- ROC-AUC (~0.85) → strong classification  
- Lower Precision → expected due to imbalance  
- Successfully detects lateral movement patterns  

---

## 🔗 Attack Graph Integration
- Uses **MulVAL** for attack path generation  
- Provides:
  - Micro-level detection (edges)
  - Macro-level attack path visualization  

---

## 🚀 Setup & Run
git clone <repo-url>  
cd project-root  

python -m venv .venv  
source .venv/bin/activate   # Windows: .venv\Scripts\activate  

pip install torch torchvision torchaudio  
pip install torch-geometric  
pip install pandas numpy scikit-learn matplotlib networkx jupyter graphviz  

jupyter notebook  

Run:
- gnn_ids_dataset1.ipynb  
- gnn_ids_dataset2.ipynb  

---

## 💡 Applications
Cybersecurity research, SOC monitoring, enterprise security, academic projects, infrastructure protection

---

## 🔮 Future Improvements
Real-time detection, SIEM integration, improved precision, additional datasets

---

## 📌 Conclusion
This project demonstrates that **Graph Neural Networks can effectively detect lateral movement attacks**, providing a **modern, scalable, and intelligent intrusion detection solution**.
```
