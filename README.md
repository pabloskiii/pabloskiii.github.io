# pabloskiii.github.io


docker run -it --rm -v "$PWD:/srv/jekyll" jekyll/jekyll jekyll new blog

docker run -it --rm -v "$PWD:/srv/jekyll" jekyll/jekyll jekyll build

docker run -it --rm -p 4000:4000 -v "$PWD:/srv/jekyll" jekyll/jekyll jekyll serve --force_polling
