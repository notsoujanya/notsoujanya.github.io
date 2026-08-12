# notsoujanya.github.io 

this repository holds the source for my technical blog that's hosted at [notsoujanya.github.io](https://notsoujanya.github.io). i cover all topics technology, science and other miscallaneous stuff. 

---
## table of contents 

- [about](#about)
- [built-with/stack](#built-with/stack)
- [project structure](#project-structure)
- [how it works](#how-it-works)
- [writing flow](#writing-flow)
- [license](#license)

---

## about
hello! this repository holds my source code for the technical blog i host using github pages. here's where i'll be jotting down my thoughts about anything in technology, science and other varied topics that i find truly interesting. 

---

## built-with/stack 

| Tool | Purpose |
|---|---|
| [Hugo](https://gohugo.io) (extended) | Static site generator |
| [PaperMod](https://github.com/adityatelange/hugo-PaperMod) | Theme |
| [GitHub Pages](https://pages.github.com) | Hosting |
| [GitHub Actions](https://github.com/features/actions) | Deploy + security pipeline |
 
---

## project structure

```
content/posts/          — blog posts, one .md file per article
static/images/          — images organised per post slug
assets/css/extended/    — custom CSS color overrides
archetypes/             — post template (auto-fills on hugo new)
.github/workflows/      — deploy pipeline + security checks
hugo.toml               — site configuration
```
 
---

## how it works 
hugo is a software which allows you to create easy posts and host it using github pages (there's other alternatives too). papermod has cool themes that you can use to supply your aesthetic for websites you create using hugo. the primary inspiration to use this software comes from me following **lilian weng** a renowned researcher, who i deeply admire, and her blogs are really invigorating. 

i store my makrdown files in `content/posts/` which hugo reads and then builds a static website with, this is in the `public/` directory. 

to make things easier for me, i wrote a github actions workflow that runs on every push i make to `main`. this then builds the site, and then deploys. 

## writing flow

the new posts always start on a separate branch just to keep things clean. 
```bash 
git checkout -b post/article-slug
hugo new content posts/article-slug.md
```

i write my content in a text editor, review. hugo has the option of toggling draft to true or false. once i'm ready to publish, i make it false, then push to my branch. the pipeline is triggered and then merged to `main`

hugo also gives you the option to preview the server, and your website locally by running 
```bash 
hugo server -D
```

---

## license

blog content and writing © soujanya bhat. all rights reserved. 

theme ([papermod](https://github.com/adityatelange/hugo-PaperMod)) is MIT licensed. 