# README

## Setup

Create a new hugo site

~~~zsh
hugo new site . --force
~~~

Add theme hugo-theme-bootstrap4-blog

~~~zsh
git submodule add https://github.com/alanorth/hugo-theme-bootstrap4-blog.git themes/hugo-theme-bootstrap4-blog
echo 'theme = "hugo-theme-bootstrap4-blog"' >> config.toml
~~~

Add theme mediumish-gohugo-theme

~~~zsh
git submodule add https://github.com/lgaida/mediumish-gohugo-theme themes/mediumish-gohugo-theme
echo 'theme = "mediumish-gohugo-theme"' >> config.toml
~~~

## Content

Add a post "helloworld" as content/posts/helloworld.md

~~~zsh
hugo new posts/helloworld.md
~~~

Review changes

~~~zsh
hugo server --buildDrafts
~~~
