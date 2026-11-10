# Juego de mesa de cartas

Juego de cartas para el navegador, para una ronda en grupo frente a la misma pantalla. Al abrir, el menú dice **Elige un mazo** y ofrece tres: **Reto**, **Adivinanza** y **Categoría**. Cada mazo saca una carta al azar.

**Demostración:** [https://scorpwik.github.io/juego-de-mesa-cartas/](https://scorpwik.github.io/juego-de-mesa-cartas/)

## Cómo jugar

1. Elige un mazo. La carta gira un momento, poco más de un segundo, y después muestra el texto.
2. Esa carta sale del mazo y no vuelve a aparecer hasta que se acaben las demás. Cuando el mazo queda vacío, se llena otra vez con todas sus cartas y el sorteo sigue al azar.
3. Dale clic a la carta, o tócala, para voltearla y leer el reverso. Mientras gira al salir, todavía no se voltea. En **Adivinanza**, tampoco se voltea hasta tocar **Iniciar participación**.
4. **Volver a los mazos** cierra la carta y regresa al menú.
5. Si recargas la página, los tres mazos vuelven a estar completos. Nada queda guardado.

### Reto

Son 25 cartas. La cara trae una pregunta: datos del Ecuador, cultura general o un dicho para completar. En las que piden varios nombres, el reverso muestra ejemplos.

Cuando aparece el texto, la cuenta regresiva arranca sola en **00:30**.

- **+30seg** suma 30 segundos. El tope es 60.
- **-30seg** resta 30 segundos. En 0 se acaba la ronda.
- Al voltear la carta, el tiempo se detiene y se ve la respuesta.
- Si el tiempo llega a 0, la carta se cierra sin mostrar la respuesta y aparece **¡Se acabó el tiempo!** durante unos tres segundos.

### Adivinanza

Son 20 cartas. La cara muestra la adivinanza, la línea **Respuesta:** con la solución y el botón **Iniciar participación**. Quien lleva la pantalla puede leer la respuesta antes de que empiece la ronda.

Al tocar **Iniciar participación**, esa respuesta se oculta y arranca la misma cuenta regresiva de 30 segundos, con **-30seg** y **+30seg**. Voltear la carta detiene el tiempo y muestra la respuesta al reverso.

### Categoría

Son 32 cartas. La cara propone un tema, por ejemplo objetos de un color, comidas que empiezan con una letra o animales. No hay cuenta regresiva. Al voltear la carta se ven ejemplos de respuestas.

## Características

- Tres mazos incluidos: 25 retos, 20 adivinanzas y 32 categorías.
- Sorteo al azar, sin repetir carta hasta agotar el mazo.
- Animación al sacar la carta y volteo para ver el reverso.
- Cuenta regresiva de 30 segundos en Reto y en Adivinanza, ajustable de 30 en 30 segundos, entre 0 y 60.
- Aviso **¡Se acabó el tiempo!** si la cuenta llega a cero. En ese caso la respuesta no se revela.
- En Adivinanza, la respuesta queda a la vista solo hasta **Iniciar participación**.
- Categoría sin tiempo, con ejemplos al reverso.
- Fondo oscuro, detalles en dorado y cartas en tono de papel. El tamaño se acomoda al alto y al ancho de la pantalla, en el celular o en la computadora.

## Tecnologías

- HTML
- CSS, con animaciones y medidas que siguen el alto y el ancho de la ventana
- JavaScript en un solo archivo, sin librerías

Para jugar bastan el navegador y los archivos `index.html`, `style.css` y `script.js`. Los estilos y el código se enlazan con rutas relativas, así que la demostración los carga bajo el nombre actual del repositorio, `juego-de-mesa-cartas`.

## Cómo ejecutarlo en local

```bash
git clone https://github.com/Scorpwik/juego-de-mesa-cartas.git
cd juego-de-mesa-cartas
```

Abre `index.html` en el navegador.

Si prefieres servirlo en local:

```bash
python3 -m http.server 8000
```

Entra a [http://localhost:8000](http://localhost:8000).

## Autor

Joshua Lozada — [Scorpwik](https://github.com/Scorpwik)
