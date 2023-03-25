---
nav:
  - 
---
# Reformed Perspective Website

---

The rp.ca website is created using Wordpress (PHP) and an extensive, custom PHP theme called **Benchpress**. It is hosted on Dreamhost and uses Cloudflare as a caching proxy.

## Website Details

The Benchpress theme, stored at `wp-content/themes/benchpress` is a complex, custom theme that does almost all of the heavy lifting for the RP website. It handles:

- ...
- ...
- ...

### staging

Changes are made on the [staging site](staging.md) before being copied to the main site. This allows us to see, test, and evaluate the changes before they go live. Only the `benchpress` folder and select plugins from `wp-content/plugins/?` are tracked by git. New content can be added to tracking, but only as necessary.

### github

Changes to the website are [tracked using git](git.md) and are pushed to the RP [GitHub organization and repository](https://github.com/ReformedPerspective/reformedperspective.ca). Changes are pushed from staging and then pulled to the main rp.ca site using git.

---

## Page Links

---

### PHP

[See PHP](php.md)

### Git

[See Git](git.md)

### Dreamhost

[See Dreamhost](dreamhost.md)

### Cloudflare

[See Cloudflare](cloudflare.md)
