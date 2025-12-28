```bash 
kubeseal \
--fetch-cert \
--controller-namespace sealed-secrets \
--controller-name sealed-secrets \
> sealed-secrets-cert.pem
```

```bash
kubeseal \
  --format yaml \
  --namespace ceph-block-storage \
  --scope namespace-wide \
  --cert sealed-secrets-cert.pem \
  < valid-secret.yaml \
  > ceph-csi-block-storage-sealed-secret.yaml     
```


