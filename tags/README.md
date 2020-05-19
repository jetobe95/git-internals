## Etiquetas
Listar etiquetas `git tag`
````
$ git tag
v0.1
v1.3
````

### Etiquetas Ligeras
>  Una etiqueta ligera es muy parecido a una rama que no cambia - simplemente es un puntero a un `commit` específico.

```
$ git tag v1.4-lw
```

### Etiquetas Anotadas

> Las etiquetas anotadas se guardan en la base de datos de Git como objetos enteros.
Tienen un checksum; contienen el nombre del etiquetador, correo electrónico y fecha; tienen un
mensaje asociado; y pueden ser firmadas y verificadas con GNU Privacy Guard (GPG)

```
$ git tag -a v1.4 -m 'my version 1.4'
```

```
$ git show v1.4
tag v1.4
Tagger: Ben Straub <ben@straub.cc>
Date: Sat May 3 20:19:12 2014 -0700
my version 1.4
commit ca82a6dff817ec66f44342007202690a93763949
Author: Scott Chacon <schacon@gee-mail.com>
Date: Mon Mar 17 21:52:11 2008 -0700
  changed the version number
```


### Etiquetado Tardío
> También puedes etiquetar `commits` mucho tiempo después de haberlos hecho. Supongamos que tu
historial luce como el siguiente:

```
$ git log --pretty=oneline
15027957951b64cf874c3557a0f3547bd83b3ff6 Merge branch 'experiment'
a6b4c97498bd301d84096da251c98a07c7723e65 beginning write support
0d52aaab4479697da7686c15f77a3d64d9165190 one more thing
6d52a271eda8725415634dd79daabbc4d9b6008e Merge branch 'experiment'
0b7434d86859cc7b8c3d5e1dddfed66ff742fcbc added a commit function
4682c3261057305bdd616e23b64b0857d832627b added a todo file
166ae0c4d3f420721acbb115cc33848dfcc2121a started write support
9fceb02d0ae598e95dc970b74767f19372d61af8 updated rakefile
964f16d36dfccde844893cac5b347e7b3d44abbc commit the todo
8a5cbc430f1a9c3d00faaeffd07798508422908a updated readme
```
> Para etiquetar un `commit`, debes especificar el
checksum del commit (o parte de él) al final del comando

```
$ git tag -a v1.2 9fceb02
```


### Subir las etiquetas
`git push origin v1.5`

Subir todas las etiquetas

`$ git push origin --tags`