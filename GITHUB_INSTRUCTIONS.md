
# GitHub + Custom Domain Setup Guide

GitHub username: **jbass121212**
Repository name: **krystal-date-night**
Custom domain: **KrystalDateNight.com**

---
## 1. Upload the site to GitHub

1. Go to https://github.com and log in.
2. Click the **+** in the top-right → **New repository**.
3. Name it: `krystal-date-night`
4. Leave it **Public**.
5. **Do NOT** initialize with a README (leave that unchecked).
6. Click **Create repository**.

Then:

1. On the new repo page, click **"Add file" → "Upload files"**.
2. From this ZIP, upload:
   - `index.html`
   - `BestPart - Daniel Caesar ft. H.E.R. (sax cover Graziatto).mp3`
   - `README.md` (optional)
3. Scroll down and click **Commit changes**.

Your code is now on GitHub.

---
## 2. Turn on GitHub Pages

1. In your repository, click **Settings** (top bar).
2. In the left sidebar, click **Pages**.
3. Under **"Build and deployment"**:
   - Source: **Deploy from a branch**
   - Branch: choose **`main`**, folder **`/ (root)`**
4. Click **Save**.

After a minute or two, GitHub will give you a URL like:

`https://jbass121212.github.io/krystal-date-night/`

This is your GitHub Pages site.

---
## 3. Connect KrystalDateNight.com to GitHub Pages

Log in to the website where you bought **KrystalDateNight.com** and go to the **DNS / Domain / Advanced DNS** settings.

Add these records:

### A Records (IPv4)

Add **four** A records pointing your root domain (`@`) to GitHub Pages IPs:

- Type: **A**, Host: **@**, Value: **185.199.108.153**
- Type: **A**, Host: **@**, Value: **185.199.109.153**
- Type: **A**, Host: **@**, Value: **185.199.110.153**
- Type: **A**, Host: **@**, Value: **185.199.111.153**

TTL can be left at the default (e.g., Automatic).

### CNAME Record (for www)

- Type: **CNAME**
- Host: **www**
- Value: **jbass121212.github.io**
- TTL: default

Save all DNS changes.

---
## 4. Set the Custom Domain in GitHub

1. Go back to your repo on GitHub: `krystal-date-night`.
2. Go to **Settings → Pages**.
3. In the **Custom domain** box, type:

   `KrystalDateNight.com`

4. Click **Save**.

GitHub may show a message about DNS not being configured yet. That’s okay—it can take a few minutes to an hour for DNS to update.

After some time, refresh the Pages settings. Once GitHub verifies the DNS, enable:

- **Enforce HTTPS**

Now your site should be available at:

- `https://KrystalDateNight.com`
- `https://www.KrystalDateNight.com`

---
## 5. Test Everything

1. Visit: `https://KrystalDateNight.com`
2. You should see the **Private Invitation** password screen.
3. Enter the password: `IMCHECKn4krys`
4. The page should unlock, music should start, and the invitation should appear.

If something doesn’t work:
- Make sure both `index.html` and the `.mp3` file are uploaded to the **same repository and root folder**.
- Double-check the DNS records match exactly.
- Wait 10–30 minutes for DNS to fully propagate.
