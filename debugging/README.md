# SA Notes

## Debugging konvoy deployments

Use --kubeconfig flag with admin.conf created at konvoy up time and work with cluster.

```kubectl --kubeconfig admin.conf get secret -n kubeaddons```

### Example: Check state of traefik and examine logs

1. ```kubectl --kubeconfig admin.conf get pods -A -n kubeaddons | grep traefik```
2. ```kubectl --kubeconfig admin.conf logs -n kubeaddons traefik-forward-auth-XXXXXX```

## Config options
