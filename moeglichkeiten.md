
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

Possibilities for hybrids and submissions:
  - cbf_URM_estm = URM * S_cbf: we haven't tried the CBF approach yet without
    setting the diagonal to zero
  - cf_URM_estm = URM * W_cf : we haven't tried the CF approach yet with setting
    the diagonal to zero
  - Pipeline approach CBF -> CF: use cbf_URM_estm as input to CF approach,
    however according to Cremonesi you can't just take the whole URM_estm, because it will have errors, only those values with high confidence, how can we determine confidence?
    pipe_S_cf = cbf_URM_estm_norm.T * cbf_URM_estm_norm
    pipe_cf_URM_estm = URM * pipe_S_cf
  - similarity-average
    
