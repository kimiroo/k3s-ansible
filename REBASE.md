## Rebase Forked Repository

### 1. Verify configured remotes
```bash
git remote -v
```

### 2. Add the upstream repository (if missing)
```bash
git remote add upstream https://github.com/k3s-io/k3s-ansible.git
```

### 3. Fetch the latest upstream changes
```bash
git fetch upstream
```

### 4. Rebase onto the upstream branch
Ensure you are on your local branch (e.g., `master`) before rebasing.
```bash
git rebase upstream/master
```

### 5. Force-push to origin
Use `--force-with-lease` to safely update your remote fork.
```bash
git push origin master --force-with-lease
```