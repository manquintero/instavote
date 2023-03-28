# Expoting Sync Manifests

-----

Clone the `flux-infra` repository

```sh
git clone https://github.com/${GITHUB_USER}/flux-infra.git
cd flux-infra
```

Export the Source Controller

```sh
# See the contents
flux export source git instavote

# Save the contents
flux export source git instavote >> clusters/dev/instavote-gitrepository.yaml
```

Export the Kustomizations

```sh
# See the contents
flux export kustomization vote-dev
# Save the contents
flux export kustomization vote-dev >> clusters/dev/vote-dev-kustomization.yaml
```

Save the Resources

```sh
git add -Av
git commit -am "chore: save cluster dev configuration"
git push origin HEAD:refs/heads/main
```

-----
Next: [Adding Health Checks](./07-Adding-Health-Checks.md)
