# Automating Rollouts on Configuration Changes

Now the the ConfigMap information is embedded in the Deployment information every time you modify the `options.env` file a new RollOut will be triggered:

Regenerate the options file:

```sh
cat > deploy/vote/staging/options.env << EOF
OPTION_A=Thalia
OPTION_B=Paulina
EOF
```

## Commit and Promote your changes

```sh
git add deploy
git commit -m "feat: Update ConfigMap to override options in the vote site"
git push origin HEAD:refs/heads/main
```

---
Next: [Generate Worker Deployment](./12-Generate-Worker-Deployment.md)