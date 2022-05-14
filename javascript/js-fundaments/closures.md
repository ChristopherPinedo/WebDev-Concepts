# Closures

Una closure es una función que recuerda sus variables externas y puede acceder a ellas. En algunos lenguajes, eso no es posible, o una función debe escribirse de una manera especial para que suceda.

Es decir: recuerdan automáticamente dónde se crearon utilizando una propiedad oculta `[[Environment]]`, y luego su código puede acceder a las variables externas.

Cuando en una entrevista un desarrollador frontend recibe una pregunta sobre “¿qué es una clausura?”, una respuesta válida sería una definición de clausura y una explicación de que todas las funciones en JavaScript son clausuras, y tal vez algunas palabras más sobre detalles técnicos: la propiedad `[[Environment]]` y cómo funcionan los entornos léxicos.



Como se explicó anteriormente, en JavaScript todas las funciones son clausuras naturales, solo hay una excepción:

Normalmente, una función recuerda dónde nació en una propiedad especial llamada `[[Environment]]`, que hace referencia al entorno léxico desde dónde se creó.

Pero cuando una función es creada usando `new Function`, su `[[Environment]]` no hace referencia al entorno léxico actual, sino al global.

Entonces, tal función no tiene acceso a las variables externas, solo a las globales.
