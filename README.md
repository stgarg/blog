## Minimal Collection-Based Blog

This repository hosts a very small GitHub Pages site with:

* Undated posts in a custom collection `_blog/` (free filename slugs)
* Automatic sidebar + home listing
* Light/Dark mode toggle (no build step)

### Structure
```
/_config.yml
/index.md            (home; layout: home)
/about.md            (about page; section: about)
/_blog/              (collection documents)
  first-post.md
  _template.md
/_includes/sidebar.html
/_layouts/{base,home,post,page}.html
/assets/style.css
```

### New Post
Copy `_blog/_template.md` → `_blog/my-new-note.md`, change `title:`, (optionally add `date:`), write content, commit & push.

### Ordering
If you add `date: YYYY-MM-DD`, lists sort by date (desc). Without dates, order is build order. (Add an `order:` field + adjust Liquid later if you want manual ordering.)

### Local Test (Optional)
You can run `bundle exec jekyll serve` if you add a Gemfile, but this setup is designed to work with just GitHub Pages' native build (no plugins required).

### Deploy
Repo name assumed `blog`; site will live at `https://<user>.github.io/blog/` because `_config.yml` sets `baseurl: /blog`.

### License / Attribution
All original content © You. Code for site scaffold is trivial; use freely.
