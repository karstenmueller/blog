# README

## Initial Setup

### Create a new hugo site

~~~zsh
hugo new site . --force
~~~

Add theme hugo-theme-bootstrap4-blog

~~~zsh
git submodule add -f https://github.com/alanorth/hugo-theme-bootstrap4-blog.git themes/hugo-theme-bootstrap4-blog
echo 'theme = "hugo-theme-bootstrap4-blog"' >> config.toml
~~~

### Setup git branch and worktree

Create empty branch "gh-pages"

~~~zsh
git checkout --orphan gh-pages
git reset --hard
git commit --allow-empty -m "Initializing gh-pages branch"
git push origin gh-pages
git checkout master
~~~

Add "gh-pages" to worktree

~~~zsh
git worktree add -B gh-pages public origin/gh-pages
~~~

## Create Content

Add a post "helloworld" as content/posts/helloworld.md

~~~zsh
hugo new posts/helloworld.md
~~~

Review changes

~~~zsh
hugo server --buildDrafts
~~~

## Publish Content

~~~zsh
hugo
pushd public && git add --all && git commit -m "Initial commit to gh-pages" && popd
git push origin gh-pages
~~~
