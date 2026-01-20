# Multi-Layer_Heterogeneous_Network_Data
This repository provides **multi-layer heterogeneous network data sets** and example code for reproducible experiments on **key node identification** and other multi-layer network analytics.

Each data set is stored in a **two-file format** for long-term reproducibility:

- `*_network.npz` — structured network representation (matrices + metadata)
- `*_node2idx.pkl` — mapping from original node IDs to global matrix indices

This design ensures:
- deterministic, stable node ordering across experiments,
- matrix-friendly computation (NumPy/PyTorch),
- independence from NetworkX version changes.

---
