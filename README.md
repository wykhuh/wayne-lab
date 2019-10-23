# Wayne Lab, UCLA

This is the repo for Wayne Lab website.

The site is created with [Academic Kickstart](https://sourcethemes.com/academic/), a static site generator written in
[Go](http://golang.org). People write the content using Markdown, and
Hugo will convert the Markdown content into HTML.

## Updating the site

1. Clone this repo.
2. Use a text editor such as Atom or VS Code to edit the files. See the
   [Add and edit](#add-and-edit-pages) section for more details.
   1. If you want to run the site on your computer to preview the changes, see the
      [Start local server](#start-local-server) section for more details.
3. Commit the changes and push them to master branch on Github.
4. The site will be automatically updated.

## Start local server

### RStudio version

1. Open RStudio and install `blogdown`

```R
install.packages("blogdown")
blogdown::install_hugo(force = TRUE)
```

2. In the RStudio menu bar, choose Addins > blogdown Serve Site (clicking this will call blogdown:::serve_site())

3. Paste the URL (e.g. http://127.0.0.1) into your web browser.

### Golang version

1. Install [Go](http://golang.org).
2. Install [Hugo](https://gohugo.io) on MacOS.

```
brew install hugo
```

3. Start server

```
hugo server
```

3. Paste the URL (e.g. http://localhost:1313) into your web browser.

## Add and edit pages

`base_templates` directory has examples files that you can copy and edit.

`config` contains configuration files for the site.

`content` directory has the content for the various pages.

- Most of your changes will go in this directory.
- The content is written in Markdown and LaTeX math. Vist
  Academic's [Writing Content](https://sourcethemes.com/academic/docs/writing-markdown-latex/) page more details.
- At the top of the page, there is some metadata between two rows of `---`.
  After the metadata (AKA Front Matter), you place the rest of the content for the page.

```
---
title: My first blog post
date: 2017-12-01
---

Esse officia voluptate excepteur ea culpa quis.
```

`static` directory is for images and files.

### 1. Contact

Edit the `/config/params.toml` file, `Contact details` section.

### 2. Donate

Edit the `content/donate.md` file.

### 3. Home page

The items on the home page are in `content/home`.

**A. Projects** (content/home/featured_projects.md)

Any project in `/content/projects/` with `featured: true` will be shown
on the home page.

**B. News** (content/home/news.md)

The latest 3 news items in `content/news` will be shown on the home page.

### 4. News

1. To add a new news item, create a directory with the item's name in `content/news`.

- Each directory must have an unique name.
- Use `-`, not spaces for the news item name.

```bash
content/news/new-news
```

2. Add a file `index.md`to the new directory. If you want the news item to have
   an image, add `featured.jpg`.

3. Copy `base_templates/news/news-name/index.md` into `index.md`, and
   edit the contents.

### 5. People

1. To add a new person, create a directory with the user's username in `content/authors`.

- Each directory have an unique username.
- Use `-`, not spaces for the username.

```bash
content/authors/new-user
```

2. Add a file `_index.md` to the new directory. If you want the person to have an
   image, add `avatar.jpg`.

3. Copy `base_templates/authors/user-name/_index.md` into `_index.md`, and edit the
   contents.

### 6. Projects

1. To add a new project, create a directory with the project's name in `content/projects`.

- Each directory must have an unique name.
- Use `-`, not spaces for the project name.

```bash
content/projects/new-project
```

2. Add a file `index.md`to the new directory. If you want the project to have
   an image, add `featured.jpg`.

3. Copy `base_templates/projects/project-name/index.md` into `index.md`, and
   edit the contents.

### 7. Publications

Edit the `content/publications.md` file.

### 8. Resources

Edit the `content/resources.md` file.
