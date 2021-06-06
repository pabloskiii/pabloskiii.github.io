# pabloskiii.github.io

en esta practica desplegaremos un blog en github pages utilizando la herramienta jekyll con docker compose, para ello en el directorio del repositorio correrermos este comando para descargar las dependencias del blog
```
docker run -it --rm -v "$PWD:/srv/jekyll" jekyll/jekyll jekyll new blog
```
ahora con el siguiente comando construiremos la estructura de carpetas que tendra el sitio 
```
docker run -it --rm -v "$PWD:/srv/jekyll" jekyll/jekyll jekyll build
```

y ahora con el siguiente lanzaremos el sitio como tal y una vez lanzado podemos pararlo y subirlo a github
```
docker run -it --rm -p 4000:4000 -v "$PWD:/srv/jekyll" jekyll/jekyll jekyll serve --force_polling
```

si queremos añadir alguna pagina al blog añadiremos el archivo markdown en la carpeta post.Tendremos que activar github pages dentro de las configuraciones del repositorio
