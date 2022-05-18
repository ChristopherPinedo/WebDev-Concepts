# Hash Tables

Una Hash Table es similar a un objeto JSON.

La única diferencia es que, a la “key” que tu le pases se le va a aplicar una(Hash Function) función que convertirá esa key en una referencia de memoria que es en donde se guardarán los valores que tu les pases.

Para obtener de regreso tus valores, tienes que usar esa misma key, que será convertida de nuevo en un hash con la referencia de memoria en donde están guardados tus valores y te los devolverá.

## Hash table colision

En ocasiones podemos pasar un key distintito puede generar el mismo hash, colisionando con el anterior. Esto podrá depender de la cantidad de espacio disponible
