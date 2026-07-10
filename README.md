# blog
My personal blog

## Local Development

To run this Jekyll site locally, you will need [Ruby](https://www.ruby-lang.org/) and [Bundler](https://bundler.io/) installed. This project uses Ruby 3.3.7 (as defined in `.ruby-version` and `.tool-versions`).

1. **Install dependencies:**
   ```bash
   bundle install
   ```

2. **Start the local server:**
   ```bash
   bundle exec jekyll serve --livereload
   ```

3. Open your browser and navigate to `http://localhost:4000`. The site will automatically refresh when you save changes to the files.

## Working with Drafts

Jekyll supports a draft system for posts that you are still working on. 

### Creating a Draft
To create a draft, add a markdown file to the `_drafts` directory in the root of your project. Drafts don't need a date in the filename, just the title. 

Example: `_drafts/my-new-post.md`

### Previewing Drafts Locally
By default, drafts are not shown when you build or serve your site. To preview them locally in your browser, run the Jekyll server with the `--drafts` flag:

```bash
bundle exec jekyll serve --livereload --drafts
```
*Note: Drafts will be temporarily assigned the current date (or the file modification date) when previewed.*

### Publishing a Draft
When you are ready to publish a draft and make it a live post:

1. Move the file from the `_drafts` folder to the `_posts` folder.
2. Rename the file to include the publication date in the standard Jekyll format: `YYYY-MM-DD-title.md`.

For example, rename `_drafts/my-new-post.md` to `_posts/2026-07-10-my-new-post.md`.
