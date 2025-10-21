# aplicandoloaprendido3
1. Generalizacion simbolica: Reglas estrictas del lenguaje
Prototipos en lugar de clases tradicionales: Aunque desde ES6 se introdujo class, JavaScript sigue funcionando internamente con prototipos. Cada objeto puede heredar directamente de otro objeto mediante Object.create() o manipulando __proto__.
Funciones como constructores: Antes de ES6, los objetos se creaban con funciones constructoras y el operador new, que asigna el prototipo de la función al nuevo objeto.
Herencia dinámica: Los objetos pueden modificar su prototipo en tiempo de ejecución, lo que permite una flexibilidad que no existe en lenguajes con herencia estática.
Encapsulamiento mediante closures: Aunque no hay modificadores de acceso como private, se puede simular encapsulamiento usando funciones y closures.
Tipado dinámico y débil: Las variables pueden cambiar de tipo en tiempo de ejecución, lo que permite una gran flexibilidad pero también introduce riesgos si no se controla bien.

2. Creencias de los profesionales: ¿Qué se considera “mejor” en JavaScript?
   Flexibilidad extrema: La herencia basada en prototipos permite estructuras más dinámicas y adaptables que las jerarquías rígidas de clases.
Funciones como ciudadanos de primera clase: Se pueden pasar, retornar y asignar funciones como cualquier otro valor, lo que potencia la programación funcional y la composición.
Closures y lexical scoping: Permiten encapsular estado sin necesidad de clases, lo que muchos consideran más elegante y funcional.
Modelo asincrónico no bloqueante: El uso de Promises, async/await y el event loop permite manejar concurrencia de forma eficiente sin hilos.
Interoperabilidad universal: JavaScript corre en navegadores, servidores (Node.js), bases de datos, y hasta microcontroladores. Su ubicuidad lo hace una herramienta versátil.
Evolución constante: La comunidad valora que el lenguaje se actualice con frecuencia (ES6, ES2020, etc.), incorporando mejoras sin perder compatibilidad.
