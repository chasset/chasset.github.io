# Utilissation de Jekyll

Pour créer un nouveau site :

```bash
export JEKYLL_VERSION=3.8; docker run --rm --volume="$PWD:/srv/jekyll" -it jekyll/jekyll:$JEKYLL_VERSION jekyll new .
```

Pour compiler une fois :

```bash
export JEKYLL_VERSION=3.8; docker run --rm --volume="$PWD:/srv/jekyll" -it jekyll/jekyll:$JEKYLL_VERSION jekyll build
```

Pour compiler dès qu’un fichier change :

```bash
export JEKYLL_VERSION=3.8; docker run --rm --volume="$PWD:/srv/jekyll" -it jekyll/jekyll:$JEKYLL_VERSION jekyll build --watch
```
