Publishing this Quarto blog and getting your R-bloggers feed
============================================================

This folder is a small Quarto blog. It already contains your stratifyR 2.0
post. When published, Quarto builds a full-content RSS feed automatically, and
that feed URL is what you paste into the R-bloggers submission form.

What you need once
------------------
1. R (you have it).
2. Quarto: download from https://quarto.org/docs/get-started/ and install.
   Check it works by running  quarto --version  in a terminal.

Preview it locally (optional)
-----------------------------
In a terminal, change into this folder and run:

    quarto preview

Your browser opens the blog. Press Ctrl+C in the terminal to stop.

EASIEST WAY TO PUBLISH: Quarto Pub (no GitHub needed)
-----------------------------------------------------
In this folder, run:

    quarto publish quarto-pub

The first time, it opens a browser to create a free Quarto Pub account and
authorise it. It then renders and uploads the site and prints your site URL,
something like:

    https://karunagreddy.quarto.pub/karuna-reddy/

Your RSS feed is that URL with index.xml on the end, for example:

    https://karunagreddy.quarto.pub/karuna-reddy/index.xml

Open the feed URL in a browser to confirm it loads, then paste it into the
R-bloggers "Blog RSS feed" field.

ALTERNATIVE: GitHub Pages
-------------------------
If you prefer GitHub, from this folder:

    git init
    git add .
    git commit -m "Add blog with stratifyR 2.0 post"
    # create an empty repo on github.com (for example: blog), then:
    git remote add origin https://github.com/<your-username>/blog.git
    git push -u origin main
    quarto publish gh-pages

Your site is then at   https://<your-username>.github.io/blog/
and the feed at        https://<your-username>.github.io/blog/index.xml

For R-bloggers
--------------
- Paste the index.xml feed URL into the "Blog RSS feed" field.
- Keep this blog R-only, so every post is R content and the feed stays clean.
  (If you later write non-R posts, we can switch to a category feed instead.)
- After R-bloggers approves the feed, this post, and any future post you add to
  the posts/ folder, is picked up automatically.

Adding a future post
--------------------
Make a new folder under posts/, for example posts/fitverse/, put an index.qmd
in it with a title, author, date and categories at the top, then run
quarto publish again. That is how FitVerse and later packages can go up too.
