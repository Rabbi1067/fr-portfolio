# Fazley Rabbi — Portfolio

A personal portfolio website with a built-in **dark / light theme toggle** (dark mode by default).

---

## 📁 File Structure

```
fazleyrabbi-portfolio/
├── index.html        ← Main HTML (all sections + theme toggle button)
├── css/
│   └── styles.css    ← All CSS styles (theme variables at the top)
├── js/
│   └── main.js       ← All JavaScript (theme toggle logic at the top)
└── README.md         ← This file
```

---

## 🎨 Dark / Light Mode

- The site opens in **dark mode by default**.
- Click the sun/moon button in the navbar to switch themes.
- The chosen theme is saved in the browser's `localStorage`, so it is
  remembered the next time the visitor opens the site.
- All theme colors are defined as CSS variables in `css/styles.css`
  (`:root` = dark theme, `[data-theme="light"]` = light theme override).

---

## 🚀 Deploy to GitHub Pages (Free, Step by Step)

### Step 1 — Create a GitHub repository

1. Go to **github.com** → Sign in (or create an account)
2. Click **New repository**
3. Name it `portfolio` (or any name you like) → set it to **Public** → **Create repository**

### Step 2 — Upload your files

1. On your new repository page, click **Add file → Upload files**
2. Drag and drop these files/folders:
   ```
   index.html
   css/styles.css
   js/main.js
   README.md
   ```
3. Click **Commit changes**

### Step 3 — Enable GitHub Pages

1. In your repository, go to **Settings → Pages**
2. Under **Build and deployment → Source**, select **Deploy from a branch**
3. Under **Branch**, select `main` and folder `/ (root)` → click **Save**
4. Wait 1–2 minutes. GitHub will show your live URL, something like:
   ```
   https://<your-github-username>.github.io/portfolio/
   ```

That's it — your site is live for free, with no extra configuration needed!

### Step 4 (Optional) — Use a custom domain

If you own a custom domain (e.g. `fazleyrabbi.dev`) and want to use it with
GitHub Pages instead of the default `github.io` URL:

1. In your domain registrar's DNS settings, add a **CNAME** record:
   ```
   Type    Host    Value
   CNAME   www     <your-github-username>.github.io
   ```
   (For an apex/root domain like `fazleyrabbi.dev` without `www`, add 4 **A** records pointing to GitHub Pages' IP addresses: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`)
2. In your repository, go to **Settings → Pages → Custom domain**, enter your
   domain, and click **Save**
3. Check **Enforce HTTPS** once it becomes available (GitHub provides a free
   SSL certificate automatically)
4. Wait for DNS to propagate (can take a few minutes up to 24 hours)

---

## ✅ W3C Validation

Validate your HTML at: **https://validator.w3.org**
- Method: **File Upload** → upload `index.html`
- Or after deploying: use **Direct Input** with your live URL

Validate your CSS at: **https://jigsaw.w3.org/css-validator**
- File Upload → `css/styles.css`

---

## 📝 Adding Your Photo

In `index.html`, find this section:
```html
<div class="photo-avatar-inner">FR</div>
```

Replace it with an image inside the `.photo-card` block:
```html
<img src="photo.jpg" alt="Fazley Rabbi"
  style="width:100%;height:100%;object-fit:cover;object-position:top center;" />
```

Place the photo file in the project's root folder.

---

## 🔧 How to Update the Site

After making any changes, push/upload the updated files to your GitHub
repository. GitHub Pages will automatically redeploy the site within a
minute or two.
