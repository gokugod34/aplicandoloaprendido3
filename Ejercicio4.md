1. Encapsulamiento
   Cada módulo define una función constructora que encapsula su estado interno (por ejemplo, tareas en TaskManager) y expone métodos públicos mediante el prototype. Esto permite proteger la lógica interna y evitar que otras partes del programa manipulen directamente los datos sin pasar por los métodos definidos.
2. Abstracción
   Se abstraen responsabilidades específicas en objetos dedicados: InputHandler para entrada, TaskManager para gestión de tareas, TaskSearcher para búsqueda, MenuHandler para navegación, y Application como punto de entrada. Esta separación permite que cada módulo se enfoque en una sola responsabilidad, facilitando el mantenimiento y la comprensión del código.
3. Modularidad y reutilizacion
   Al definir métodos en el prototype, se evita duplicar lógica entre instancias y se promueve la reutilización. Además, los módulos están organizados en archivos separados, lo que permite importar y usar funcionalidades de forma clara y ordenada.

No use Polimorfismo y herencia porque el problema no lo requeria. Y el sistema no requeria de jerarquias de clases ni especializacion de comportamientos.

No se como queria los ejemplos pero le pongo uno de cada codigo usado para realizar el ejercicio
1. io.js:
   Encapsula la lógica de entrada en un objeto reutilizable, ocultando detalles de implementación.
   
   function InputHandler() {
  this.rl = readline.createInterface({
    input: process.stdin,
    output: process.stdout,
  });
}

InputHandler.prototype.input = function (question) {
  return new Promise((resolve) => {
    this.rl.question(question, (answer) => resolve(answer));
  });
};

2. main.js: 
Define una abstracción del ciclo de vida de la aplicación, separando la inicialización del resto del sistema.

   function Application() {}

Application.prototype.run = function () {
  menu();
};

3. menu.js:
Organiza la interacción del usuario en un objeto dedicado, manteniendo el flujo de control encapsulado.

function MenuHandler() {}

MenuHandler.prototype.menu = async function () {
  // lógica de menú interactivo
};

4. buscarTarea.js:
Encapsula la lógica de búsqueda en un objeto especializado, promoviendo la modularidad.

function TaskSearcher() {}

TaskSearcher.prototype.buscarTarea = async function () {
  // muestra tareas y permite seleccionar una
};

5. agregarTarea.js:
Este módulo encapsula estado (tareas) y expone métodos para manipularlo, cumpliendo con los principios de OOP.

function TaskManager() {
  this.tareas = [];
}

TaskManager.prototype.agregarTarea = async function () {
  // crea tareas y las guarda en this.tareas
};

TaskManager.prototype.getTareas = function () {
  return this.tareas;
};
