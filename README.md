# Aterrizaje Suave — Modo Base

Minijuego educativo de física donde el estudiante debe decidir a qué altura encender el motor de una cápsula para lograr un aterrizaje seguro. Forma parte de **EulerGames**, una colección de retos interactivos donde el estudiante razona, calcula y contrasta su decisión con una simulación.

---

## Descripción del juego

En **Aterrizaje Suave — Modo Base**, una cápsula desciende verticalmente hacia una plataforma en un mundo con gravedad propia. El motor tiene una potencia fija durante toda la misión, por lo que el estudiante sólo debe decidir la altura de encendido.

La misión consiste en encender el motor con suficiente distancia de frenado para que la cápsula llegue a la plataforma con una velocidad segura, evitando un impacto destructivo, un rebote excesivo o el agotamiento prematuro del combustible.

---

## Objetivo educativo

El juego trabaja conceptos básicos de cinemática y dinámica en una dimensión:

* caída vertical;
* velocidad y aceleración;
* gravedad;
* fuerza de empuje;
* fuerza neta;
* masa;
* frenado;
* consumo de combustible;
* velocidad segura de aterrizaje;
* estimación de distancia de frenado.

---

## Mecánica principal

Cada misión presenta datos físicos del descenso, como altura inicial, velocidad inicial, gravedad, masa de la cápsula, potencia fija del motor, empuje máximo, combustible disponible y velocidad segura de contacto.

El estudiante debe tomar una sola decisión antes de iniciar:

* elegir la altura a la que se encenderá el motor.

Al presionar el botón de prueba, la cápsula ejecuta exactamente la estrategia programada. El jugador no controla el descenso en tiempo real, por lo que el reto no depende de reflejos, sino de razonar antes de actuar.

La dificultad principal está en interpretar cómo la altura de encendido modifica la distancia disponible para frenar. Si el motor se enciende demasiado tarde, la cápsula puede llegar con demasiada velocidad. Si se enciende demasiado pronto, puede gastar combustible innecesariamente o frenar en exceso.

---

## Evaluación

Cada misión permite un solo intento. Una vez iniciado el descenso, el resultado queda registrado y la misión se considera terminada.

El intento se considera exitoso si la cápsula aterriza con una velocidad final menor o igual al límite seguro indicado en los datos de misión.

Después del intento, el juego proporciona retroalimentación sobre el resultado. Puede indicar, por ejemplo, si el aterrizaje fue seguro, si el encendido ocurrió demasiado tarde, si el motor actuó demasiado pronto, si se agotó el combustible o si la cápsula llegó con una velocidad excesiva.

La retroalimentación incluye evidencia del intento, como velocidad final, límite seguro, combustible restante y comportamiento observado durante el descenso.

---

## Controles

El juego utiliza un control visual para seleccionar la altura de encendido del motor.

Controles principales:

* deslizador para ajustar la altura de encendido;
* botones visibles para disminuir o aumentar la altura;
* botón para probar el descenso;
* botón para generar una nueva misión;
* botón para activar o desactivar sonido.

Convención de teclado de EulerGames:

* `← / →` para ajuste grueso;
* `↑ / ↓` para ajuste fino;
* botones visibles equivalentes al teclado.

Después de iniciar el intento, los controles quedan bloqueados. Al finalizar, el estudiante puede revisar el resultado y pasar a una nueva misión.

---

## Visualización

El juego incluye una escena central donde se observa la cápsula descendiendo hacia la plataforma. La altura de encendido programada se muestra como una línea de referencia dentro de la simulación.

Elementos visuales principales:

* panel de datos de misión;
* simulación central en Canvas;
* indicador de tiempo;
* telemetría de altura, velocidad, combustible y estado del motor;
* barra de combustible;
* retroalimentación visual de éxito o fallo;
* panel posterior de evidencia del descenso;
* gráficas apiladas de altura vs tiempo y velocidad vs tiempo;
* línea de referencia de altura de encendido;
* línea de velocidad segura;
* efectos visuales de motor, impacto y partículas;
* sonido opcional mediante Web Audio API.

Las gráficas aparecen después del intento para que el estudiante pueda analizar la evidencia sin saturar la simulación principal.

---

## Modelo físico o matemático simplificado

El juego utiliza un modelo simplificado de movimiento vertical con fines educativos. La cápsula se mueve en una dimensión bajo la acción de la gravedad y del empuje del motor.

El modelo considera:

* gravedad constante durante cada misión;
* masa constante de la cápsula;
* velocidad inicial descendente;
* empuje vertical hacia arriba;
* potencia fija del motor;
* empuje efectivo calculado a partir de la potencia fija y el empuje máximo;
* consumo de combustible proporcional a la potencia utilizada;
* ausencia de resistencia del aire;
* simulación en tiempo físico real.

De forma general, el cálculo interno sigue estos pasos:

1. la cápsula inicia a cierta altura con una velocidad descendente;
2. antes del encendido, acelera por efecto de la gravedad;
3. cuando alcanza la altura elegida por el estudiante, el motor se activa si queda combustible;
4. el empuje reduce la aceleración descendente o puede invertirla si es excesivo;
5. la simulación actualiza posición, velocidad y combustible en cada instante;
6. al tocar la plataforma, se evalúa la velocidad final contra el límite seguro.

El modelo no pretende representar todos los detalles de un cohete real, pero mantiene una relación coherente entre gravedad, empuje, masa, aceleración, velocidad, posición y combustible.

---

## Tecnologías utilizadas

* HTML
* CSS
* JavaScript
* Canvas API
* Web Audio API

No se utilizan librerías externas.

---

## Cómo ejecutar

Sólo es necesario abrir el archivo:

```text
index.html
```

en un navegador moderno.

El juego también puede publicarse directamente mediante GitHub Pages, ya que todo el contenido está contenido en un único archivo HTML.

---

## Estructura del proyecto

```text
Aterrizaje-Suave-Modo-Base/
│
└── index.html
```

---

## Filosofía EulerGames

**EulerGames** busca crear minijuegos educativos donde el estudiante no sólo observe una simulación, sino que participe activamente en el razonamiento.

Cada juego debe proponer un reto claro:

1. leer datos;
2. razonar o calcular;
3. tomar una decisión;
4. probar la respuesta;
5. recibir retroalimentación.

El objetivo es que el juego funcione como una experiencia interactiva de aprendizaje, no como una calculadora disfrazada.

---

## Autor

Proyecto desarrollado por **Fausto** como parte de la colección **EulerGames**.
