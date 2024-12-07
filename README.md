# Yet another blog!

[![Build Status](https://travis-ci.org/vipulkrsingh/vipulkrsingh.github.io.svg?branch=master)](https://travis-ci.org/vipulkrsingh/vipulkrsingh.github.io)

## Local Development

### Setup
1. Install Ruby and Jekyll dependencies:
   ```bash
   gem install jekyll bundler
   bundle install
   ```

### Running the Server
- Run with drafts visible:
  ```bash
  jekyll serve --drafts
  ```
- Run without drafts:
  ```bash
  jekyll serve
  ```
- Access the site at: `http://localhost:4000`

## Managing Posts

### Creating a Draft Post
1. Create a new markdown file in the `_drafts` folder
2. Name it using the format: `title-of-your-post.md`
3. Add the front matter at the top of the file:
   ```yaml
   ---
   layout: post
   title: "Your Post Title"
   date: YYYY-MM-DD
   categories: [category1, category2]
   ---
   ```
4. Write your post content using markdown

### Publishing a Post
1. Move the file from `_drafts` to `_posts`
2. Rename the file to include the date: `YYYY-MM-DD-title-of-your-post.md`
3. Update the date in the front matter if needed
4. Commit and push to GitHub:
   ```bash
   git add .
   git commit -m "Add new post: Your Post Title"
   git push origin master
   ```

The site will automatically deploy via Travis CI after pushing to master.

## Troubleshooting
- Clear Jekyll cache if you encounter build issues:
  ```bash
  jekyll clean
  ```
- Rebuild the site:
  ```bash
  jekyll build
  ```