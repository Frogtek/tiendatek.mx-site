# Tiendatek.mx
[![Build Status](https://api.travis-ci.org/Frogtek/tiendatek.mx-site.svg)](https://travis-ci.org/Frogtek/tiendatek.mx-site)

This is the source code for [Tiendatek](http://tiendatek.mx) website.
It is based on [Jekyll](https://jekyllrb.com/) and deployed to [Github pages](https://pages.github.com)

## Development

### Install

You must have `ruby` and `bundler` installed

```
make install
```

### Run

To run the web locally on [http://localhost:4000](http://localhost:4000)

```
make
```

To execute all tests (or HTML tests or Css tests only):

```
make t
make t_html
make t_css
```

## Contributing

General rules:

- Run the tests (and fix it) before merge to master
- When possible, use Markdown (.md) instead of HTML (.html)

### Writing posts

1. Create a file on `_posts` folder. Follow name convention (reverse date + "slugified" title). For example: `2018-01-20-my-first-post.md`
2. Add the post header (with at least title, date, author and tags):
3. Write your post (preferably in markdown)

Note that:

- You must add `Frogtek Tiendatek` category to appear in [/revista/](http://tiendatek.mx/revista/) index
- Post images/files must be on `./assets/posts` folder
- To refer internal link you must use a liquid expression like: `{{ site.baseurl }}/relative_url`

Sample:
    
    ---
    layout: post
    title: My first post`
    date: 2018-01-20 13:13:54.000000000 +01:00
    author: guillermo
    categories:
    - Revista Tiendatek
    ---
    This is the excerpt of my first post.
    
    I can use [Markdown](https://daringfireball.net/projects/markdown)
    
    ![sample image](https://media.giphy.com/media/A49qRTnZhaZDW/giphy.gif)


### Tweak site style

Put your CSS on `_sass` folder. 

Run css tests before commit ;)

## Related documentation

- [Jekyll site](https://jekyllrb.com/docs/)
- [About Github pages and Jekyll](https://help.github.com/articles/about-github-pages-and-jekyll/)
- [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)