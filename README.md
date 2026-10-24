# madanyn3.github.io

Personal website of Madan Y N, served by GitHub Pages at <https://madanyn3.github.io>.

It is a plain Jekyll site with no theme gem; the layout and styles live in this repo.

## Where things are

| What | File |
| --- | --- |
| Home page (bio, interests, outside work) | `index.html` |
| News items on the home page | `_data/news.yml` |
| Projects | `_data/projects.yml` (rendered by `projects.html`) |
| Publications | `_data/publications.yml` (rendered by `publications.html`) |
| CV page | `cv.html` |
| CV PDF | `assets/cv/Madan_YN_CV.pdf` |
| Top navigation | `_data/navigation.yml` |
| Blog posts | `_blogs/` (listed by `blogs.html`) |
| Styles, including dark mode | `assets/css/main.css` |

### Adding things

- **A publication or preprint:** copy the commented template at the top of
  `_data/publications.yml`. Set `type` to `paper`, `preprint` or `poster`;
  a section heading appears automatically once it has an entry.
- **A project:** add an item under the right group in `_data/projects.yml`.
  The `id` becomes the anchor (`/projects/#id`). To feature it on the home
  page, add the id to the `featured` list in `index.html`.
- **A news item:** add it at the top of `_data/news.yml`. The home page shows the six most recent.
- **A new CV:** replace `assets/cv/Madan_YN_CV.pdf` (keep the name) and update `cv.html`.
- **A blog post:** add a file in `_blogs/` with `layout: post`, a `permalink`,
  a `date` and `category: quick-read` (listed automatically). Long-form pieces
  are linked by hand in the "Essays & deep dives" list in `blogs.html`.
- **Math in a page:** add `math: true` to its front matter to load MathJax.

## Running locally

```sh
bundle exec jekyll serve --livereload
```

Then open <http://localhost:4000>.

## Credits

Originally built on [Lanyon](https://github.com/poole/lanyon) by Mark Otto,
via a template by [Vedang Asgaonkar](https://vedangasgaonkar.github.io/).
Released under the [MIT license](LICENSE.md).
