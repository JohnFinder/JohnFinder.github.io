# Blood Oxygen Monitor · Legal site (GitHub Pages)

Static privacy policy for App Store Connect + in-app `AppLegalURLs.privacyPolicy`.

## Expected public URL

After you create a user/org Pages site:

- User site: `https://<github-username>.github.io/privacy/`
- Or project site: `https://<github-username>.github.io/<repo-name>/privacy/`

Then set in code:

```swift
static let privacyPolicy = URL(string: "https://<github-username>.github.io/privacy/")
```

## Create & publish (recommended: GitHub CLI)

```bash
brew install gh
gh auth login   # browser / device flow — do NOT paste tokens into chat
cd legal-site
gh repo create bloodoxygen-legal --public --source=. --remote=origin --push
# In GitHub → Settings → Pages → Deploy from branch `main` / root
```

## If you prefer a token (optional)

1. GitHub → Settings → Developer settings → Personal access tokens
2. Create a **fine-grained** or classic token with `repo` (create public repo) scope
3. **Do not paste the token into Cursor chat.** Put it only in your local shell:

```bash
export GH_TOKEN='…'   # local terminal only
# or: export GITHUB_TOKEN='…'
```

Then ask the agent to create/push the repo; tools can use `$GH_TOKEN` / `$GITHUB_TOKEN` without the value appearing in chat history if you set it yourself in the terminal.

## Contact email

Replace `support@bloodoxygenmonitor.app` in `privacy/index.html` if you use a different address.
