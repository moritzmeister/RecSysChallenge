
### Methods and Matrices:

General:
  - URM
  - ICM

MF:
  - URM_estm (product of X*Y)

CF:
  - URM_norm : URM normalized per column with l2 norm
  - S_cf = URM_norm.T * URM_norm : Cosine similarity between items (Step 1)
  - W_cf = S_cf, just with diagonal all zeros
  - cf_URM_estm = URM * S_cf : yields score 0.06864

CBF:
  - ICM_norm : ICM normalized per column with l2 norm
  - S_cbf = ICM_norm * ICM_norm.T
  - W_cbf = S_cbf , with diagonal all zeros
  - cbf_URM_estm = URM * W_cbf : yields score 0.07951


Hybrid-Erweiterung:
- ALS
- SVD
- gewichtet nur wenn anderer Wert
- normalisierung pro playlist vor Gewichtung

Einzelne Methoden verbessern:
- Bias
- CBF Tag-Gewichtung
- Shrinkage bei Collaborative Filter

Neue Methoden:
- Factorization Machines
- SLIM BPR
- Stochastic gradient descent

Sonstiges:
- Validierung
