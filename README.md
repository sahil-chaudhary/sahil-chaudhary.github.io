# sahil-chaudhary.github.io

Personal academic website — built with plain HTML & CSS.

---

## Folder Structure

```
sahil-website/
├── index.html          ← About + News (home page)
├── publications.html   ← Research papers
├── blogs.html          ← Blog post index
├── notes.html          ← Lecture notes index
├── style.css           ← All shared styles
├── photo.jpg           ← Your profile photo (replace this)
├── blogs/
│   ├── example-post.html   ← Template; copy for new posts
│   └── your-post.html
└── notes/
    ├── ml-theory-lec1.pdf
    └── (drop PDFs here)
```

---

## Deploying to GitHub Pages

### Step 1 — Create your repo

1. Go to https://github.com/new
2. Name it exactly: `<your-github-username>.github.io`
   (e.g. `sahilchaudhary.github.io`)
3. Set it to **Public**
4. Click **Create repository**

### Step 2 — Push the files

```bash
# In this folder:
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/<username>/<username>.github.io.git
git push -u origin main
```

### Step 3 — Enable Pages

1. Go to your repo → **Settings** → **Pages**
2. Under "Source", select **Deploy from a branch**
3. Branch: `main`, folder: `/ (root)`
4. Click **Save**

Your site will be live at `https://<username>.github.io` within ~2 minutes.

---

## How to Update

### Add a news item
Open `index.html`, find the `<!-- ADD NEWS BELOW -->` section,
copy an existing `<div class="news-item">` block and fill in your text.

### Add a publication
Open `publications.html`, copy the `<div class="pub-item">` block,
fill in venue, title, authors, and link to the paper.

### Write a blog post
1. Copy `blogs/example-post.html` → `blogs/your-post-name.html`
2. Edit the content in the new file
3. Open `blogs.html` and add a new `<a class="blog-card">` pointing to it

### Add lecture notes
1. Drop your PDF into the `notes/` folder
2. Open `notes.html`, copy a `<div class="note-item">` block,
   update the `href` and title

### Add your profile photo
Replace `photo.jpg` in the root folder with your actual photo.
The `<img src="photo.jpg">` in `index.html` will pick it up automatically.
Keep the filename as `photo.jpg`, or update the `src` attribute.

---

## Math in Blog Posts

Each blog post template has MathJax commented out at the bottom.
To enable LaTeX rendering in a post, just uncomment those lines.

---

## Custom Domain (optional)

1. Buy a domain (e.g. `sahilchaudhary.com`)
2. In your repo root, create a file called `CNAME` with one line: `sahilchaudhary.com`
3. Point your domain's DNS to GitHub Pages (see GitHub docs for exact records)
