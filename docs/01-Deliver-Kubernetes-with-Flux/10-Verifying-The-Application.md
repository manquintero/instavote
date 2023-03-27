# Verifying the Application

Now that the first third of the application is deployed we can verify its components:

Send a vote to the service and watch the `redis` container to register it

```sh
curl -sS -X POST --data "vote=a"  http://192.168.64.3:30300
```

---
Next: [Bootstrapping The Staging Cluster](../02-Kustomize/01-Bootstrapping-The-Staging-Cluster.md)
