# Eventos

## Event Propagation



Un evento de clic se propaga en 3 fases:

1. _Fase de captura_ : a partir de `window`y `document`el elemento raíz, el evento se sumerge a través de los ancestros del elemento de destino
2. _Fase de destino_ : el evento se activa en el elemento en el que el usuario ha hecho clic
3. _Fase de burbuja_ : finalmente, el evento asciende a través de los ancestros del elemento de destino hasta el elemento raíz, `document`, y `window`.



El tercer argumento `captureOrOptions`del método:

```
element.addEventListener(eventType, handler[, captureOrOptions]);
```

le permite capturar eventos de diferentes fases.

* Si `captureOrOptions`falta el argumento, `false`o `{ capture: false }`, entonces el oyente captura los eventos de _las fases objetivo y burbuja_
* Si el argumento es `true`o `{ capture: true }`, entonces el oyente escucha los eventos de _la fase de captura_ .

## Event Delegation Pattern

La delegación de eventos es básicamente un contenedor padre que le pasa el evento a todos sus hijos (en realidad no se los está pasando, sino que el contenedor padre sigue estando presente en todos los hijos, es por eso que cuando clicamos a un hijo el evento es disárado). . Entendiendo esto, cuando obtenemos el target podemos saber cuál elemento hijo del padre fue clicado, por tanto, con una simple condicional puede ver si el elemento clicado es el que yo quiero.
