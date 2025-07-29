
---

# 🔍 GraphLIME: Interpretable Explanations for Graph Neural Networks


## 🧠 Project Overview

This project implements **GraphLIME**, a **model-agnostic explanation framework** for Graph Neural Networks (GNNs) that generates **locally faithful** and **interpretable explanations** of node-level predictions in graph-structured data.

GraphLIME addresses the **black-box nature** of GNNs by selecting the most relevant node features within an N-hop neighborhood using **HSIC Lasso**, a kernel-based nonlinear feature selection technique. The method is benchmarked against other popular interpretable models such as **LIME**, **GNNExplainer**, and **Greedy selection**.

---

## 📂 Repository Contents

* `GCN_and_graphlime.ipynb` — Jupyter Notebook demonstrating:

  * Training of GNN models (GraphSAGE, GAT)
  * Implementing GraphLIME and LIME
  * Explanation results and visualizations

* `patel_shrey_presentation.pptx` — Presentation summarizing the paper, implementation, experimental results, and key observations.

---

## 📈 Key Features

* ✅ **Model-Agnostic**: Works with any GNN (e.g., GAT, GraphSAGE)
* 🔁 **N-hop Neighborhood Sampling**: Local exploration around the node of interest
* 🔍 **HSIC Lasso**: Captures nonlinear dependencies to extract top-K informative features
* 🔬 **Sparse Explanations**: Focus on the most critical features for interpretability
* 📊 **Comparison with LIME**: Highlights effectiveness in filtering noisy features

---

## 📊 Datasets Used

* **Cora**: Citation network with binary feature vectors
* **Pubmed**: Publication network with TF-IDF-based continuous features

Both datasets are commonly used benchmarks in GNN research.

---

## 🧪 Evaluation Metrics

* **Noise Distribution Analysis**: Measures how well each explainer avoids selecting irrelevant features
* **F1 Trustworthiness Score**: Validates explanations with respect to model fidelity
* **Classifier Selection Accuracy**: Whether explanations help in choosing better models

GraphLIME consistently **outperformed** baseline methods across all metrics.

---

## 📌 Observations

| Method       | Explanation Type | Noise Filtering | Local Faithfulness | Nonlinear Capture |
| ------------ | ---------------- | --------------- | ------------------ | ----------------- |
| GraphLIME    | Nonlinear        | ✅ Excellent     | ✅ Strong           | ✅ Yes             |
| LIME         | Linear           | ❌ Poor          | ❌ Weak             | ❌ No              |
| GNNExplainer | Subgraph-based   | ⚠️ Moderate     | ✅ Fair             | ⚠️ Partial        |

more:

<img width="700" height="300" alt="image" src="https://github.com/user-attachments/assets/b020debc-2da5-4784-bd4f-7d04c04b95c8" />

---

## 📚 Reference

📄 [IEEE Paper: *GraphLIME: Local Interpretable Model Explanations for Graph Neural Networks*](https://ieeexplore.ieee.org/document/9811416)
Authors: Qiang Huang, Makoto Yamada, Yuan Tian, Dinesh Singh, Yi Chang
Affiliations: Jilin University, Kyoto University, RIKEN AIP

---

## 🧭 Future Directions

* 🔄 Extend GraphLIME to **subgraph-level** explanations
* 👥 Explain predictions for **groups of nodes**
* 📈 Improve **scalability** to large, dynamic graphs

---


