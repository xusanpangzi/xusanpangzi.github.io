<<<<<<< HEAD
=======
<<<<<<< HEAD
Solana – a Wholesome, Flat, Sunshiny Jekyll Theme
===============================================

**Solana** is a theme for the [Jekyll][jk] static site generator. [View the demo][demo].

### Features

* Compatible with GitHub Pages
* Supports categories & tags
* Responsive design
* Lightweight (no jQuery, Bootstrap, etc.) 
* Obfuscates email addresses for protection against email harvesting bots
* Comments via outbound links to Reddit

![](https://raw.githubusercontent.com/rlue/i/master/solana/responsive.gif)

![](https://raw.githubusercontent.com/rlue/i/master/solana/device_mockup.png)

Installation
------------

### Cloning Solana to your GitHub Pages

1. Prepare a [new GitHub repository][new] named after your GitHub Pages address (`<username>.github.io`). Do not initialize with a `README`, `.gitignore`, or license.
2. Clone this repository:

        $ git clone https://github.com/rlue/jekyll-solana.git

3. Associate your local copy with the GitHub Pages repo you just created:

        $ cd solana
        $ git remote rm origin
        $ git remote add origin https://github.com/<username>/<username>.github.io

4. In `_config.yml`, replace the `baseurl` site variable (`/jekyll-solana`) with an empty string (`''`):

        $ sed -i "s/\/jekyll-solana/''            /" _config.yml     # on UNIX
        $ sed -i '' "s/\/jekyll-solana/''            /" _config.yml  # on Mac

5. And push:

        $ git push -u origin master

In just a few minutes, your site should be live at https://\<username\>.github.io/!

### Previewing the site on your machine

1. Ensure that you have a Ruby development environment installed on your machine, including [Bundler][bun].
2. Install the dependencies:

        $ bundle install

3. Start the server: 

        $ bundle exec jekyll serve

You should now have a development preview of your site at http://localhost:4000/.

Usage
-----

### Customizing the theme

Edit the data in `_config.yml` as appropriate. You’ll also want to rewrite the `README` and replace identifying graphics (`/i/avatar.png`, `/favicon.ico`) with your own.

### Creating new posts

As with any Jekyll site, posts are generated from Markdown files placed in the `_posts` directory, and must be named according to the following format: `<year>-<month>-<day>-<url_slug>.md`. See the sample posts for examples of how to format rich text in Markdown.

Post content must be preceded by [YAML frontmatter][doc-fm] describing, at a minimum, the title of the post. Keep titles under 60 characters, and teasers under 160.

### Categories & Tags

This repository automatically generates “category” and “tag” archive pages based on labels provided by you in each post’s aforementioned YAML frontmatter. This feature is not available through Jekyll itself or the plugins approved for use on GitHub Pages, so it has been implemented using [git hooks][ghk].

To enable this feature, run the following command from the project root:

```
$ ln -s ../../.scripts/pre-commit.rb .git/hooks/pre-commit
```

Now, these scripts will run every time you `git commit`, ensuring that your categories and tags pages always stay up-to-date.

#### Explanation

Solana implements categories and tags as [‘collections’][doc-col], meaning each has its own top-level directory in the project root (`/_category` & `/_tag`). Inside these directories, there is a file representing each category or tag.

These files are generated by `/.scripts/spawn_labels.rb`, based on the `category:` and `tags:` attributes listed at the top of each post. The wrapper script `/.scripts/pre-commit.rb` calls this first script, then adds the newly created files to the git repo.

### Comments

As a static site generator, Jekyll has no means to provide a commenting system. For this theme, discussion is outsourced to Reddit, and requires some manual intervention. The process is as follows:

1. Publish a post.
2. Post it to Reddit.
3. Include the resulting Reddit URL in the post’s YAML frontmatter:

        reddit_post: 'https://www.reddit.com/r/Jekyll/comments/6258ln/welcome_to_solana/'

   Now, a link to the Reddit discussion will appear at the end of the post content, before the footnotes (if any).

   ![](https://raw.githubusercontent.com/rlue/i/master/solana/comments-1.png)
4. If the post receives noteworthy comments that you would like to embed directly on the page, add their permalinks to the YAML frontmatter as well:

        featured_comments:
          - url: 'https://www.reddit.com/r/Jekyll/comments/6258ln/welcome_to_solana/dfjtxba/'
            context: false
            freeze: false

   The `context` flag tells the embed script to include the target comment’s parent. The `freeze` flag prevents live updating in the event that a comment is edited after the fact. Both default to `false`.

   ![](https://raw.githubusercontent.com/rlue/i/master/solana/comments-2.png)

Modifying
---------

See the official documentation for an overview of [how Jekyll sites are organized][doc-dirs] or [how to get started][doc-qs].

The CSS for this theme was organized following Harry Roberts’ [Inverted Triangle CSS architecture][itcss].

License
-------

© 2017 Ryan Lue. This project is licensed under the terms of the MIT license.

[jk]: http://jekyllrb.com/
[demo]: https://solana.ryanlue.com/
[new]: https://github.com/new
[bun]: https://github.com/bundler/bundler#installation-and-usage
[doc-fm]: https://jekyllrb.com/docs/frontmatter/
[ghk]: http://githooks.com/
[doc-col]: https://jekyllrb.com/docs/collections/
[doc-dirs]: https://jekyllrb.com/docs/structure/
[doc-qs]: https://jekyllrb.com/docs/quickstart/
[itcss]: https://www.xfive.co/blog/itcss-scalable-maintainable-css-architecture/
=======
>>>>>>> 修改
## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/xusanpangzi/xusanpangzi.github.io/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/xusanpangzi/xusanpangzi.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
<<<<<<< HEAD
=======
>>>>>>> 5f771a9be556cd50c0557df77a89abf4173265bf
>>>>>>> 修改
