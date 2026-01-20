# Multi-Layer_Heterogeneous_Network_Data
This repository provides **multi-layer heterogeneous network data sets** and example code for reproducible experiments on **key node identification** and other multi-layer network analytics.

Each data set is stored in a **two-file format** for long-term reproducibility:

- `*_network.npz` — structured network representation (matrices + metadata)
- `*_node2idx.pkl` — mapping from original node IDs to global matrix indices

This design ensures:
- deterministic, stable node ordering across experiments,
- matrix-friendly computation (NumPy/PyTorch),
- independence from NetworkX version changes.

Please note that the DBLP_2006_2008 dataset needs to be decompressed before use due to its large original file size.
---
#### loading code:
```python
import numpy as np

data = np.load("XXXXX.npz", allow_pickle=True)
node_list = data["node_list"].tolist()
layers = data["layers"].tolist()
adj_matrices = data["adj_matrices"]
inter_layers = data["inter_layers"].tolist()
inter_adj_matrices = data["inter_adj_matrices"]

with open("XXXXX_node2idx.pkl", "rb") as f:
    node2idx = pickle.load(f)
```
## 📬 Contact & Citation

If you have any questions regarding the data set or encounter any issues using it, feel free to contact us:

- 📫 **Contact**: 230239729@seu.edu.cn


