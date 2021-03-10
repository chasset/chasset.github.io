# Utilisation de Jekyll

Pour créer un nouveau site :

```bash
export JEKYLL_VERSION=3.8; docker run --rm --volume="$PWD:/srv/jekyll" -it jekyll/jekyll:$JEKYLL_VERSION jekyll new .
```

Modifier ensuite le fichier `Gemfile` en suivant la consigne 

Pour compiler une fois :

```bash
export JEKYLL_VERSION=3.8; docker run --rm --volume="$PWD:/srv/jekyll" -it jekyll/jekyll:$JEKYLL_VERSION jekyll build
```

Pour compiler dès qu’un fichier change :

```bash
export JEKYLL_VERSION=3.8; docker run --rm --volume="$PWD:/srv/jekyll" -it jekyll/jekyll:$JEKYLL_VERSION jekyll build --watch
```

Pour servir le site internet à l’adresse http://localhost:4000 et le modifier quand un fichier change :

```bash
export JEKYLL_VERSION=3.8; docker run --rm --volume="$PWD:/srv/jekyll" -p 4000:4000 -it jekyll/jekyll:$JEKYLL_VERSION jekyll serve --watch
```
