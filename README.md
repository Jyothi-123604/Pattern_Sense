
### ✅ Steps to Remove a Contributor (Advanced)

If you really want to remove `Jyothi-123604` or any contributor:

#### 1. Clone the repository

```bash
git clone --mirror https://github.com/your-username/your-repo.git
cd your-repo.git
```

#### 2. Use [`git filter-repo`](https://github.com/newren/git-filter-repo) to remove a contributor

Install `git-filter-repo` (recommended over `filter-branch`):

```bash
pip install git-filter-repo
```

Then run:

```bash
git filter-repo --commit-callback '
    if commit.author_name == "Gundra Jyothika sri":
        commit.author_name = "Your Name"
        commit.author_email = "your@email.com"
'
```

This rewrites the commit history to replace her name and email.

> Replace `"Gundra Jyothika sri"` and email with exact match from her commits.

#### 3. Push the cleaned repo (⚠️ force push!)

```bash
git push --force --mirror
```

---

### 🟡 Alternative (Do Nothing or Archive)

If this is only cosmetic and doesn't affect your project:

* Just ignore the contributor section.
* You can mention contributors explicitly in the `README.md` instead.
