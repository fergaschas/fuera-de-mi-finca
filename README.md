# ¡Fuera de mi Finca!

Juego de cartas para dos jugadores ambientado en el campo. Cada uno lleva una finca: compras maquinaria en la feria, levantas instalaciones y atacas la cosecha del vecino. Gana quien deja al otro sin cosecha.

Se juega en el navegador, en ordenador o en móvil. No necesita servidor propio ni cuentas.

## Cómo se juega en línea

1. Un jugador pulsa **Crear partida**. Le sale un código de 4 caracteres y un enlace.
2. Se lo pasa al otro, que abre el enlace o escribe el código en **Unirse**.
3. La partida empieza sola cuando los dos están conectados.

También hay **Practicar contra la IA** y **Aprender a jugar**, un tutorial guiado de un turno.

## Qué conviene saber

- **Conexión directa.** Los dos navegadores se conectan entre sí (WebRTC). Los dos tienen que tener la página abierta mientras juegan.
- **Servicio de emparejamiento.** Para que los navegadores se encuentren se usa el servidor público gratuito de [PeerJS](https://peerjs.com). Por él solo pasa el saludo inicial; las jugadas van de navegador a navegador. Si ese servicio está caído no se pueden crear partidas ni unirse.
- **Redes restrictivas.** Algunas redes de empresa o de datos móviles no permiten conexiones directas. Si no conecta, probad con otra red.
- **Partida guardada.** Cada navegador guarda la partida en curso. Si uno recarga o cierra, puede volver desde «Partida a medias» y sigue donde estaba cuando los dos están de nuevo dentro.
- **Sin árbitro.** No hay servidor que valide las jugadas ni oculte las manos: es un juego para echar partidas con gente de confianza.

## Archivos

| Archivo | Qué es |
|---|---|
| `index.html` | El juego completo: reglas, cartas, dibujos e interfaz. |
| `peerjs.min.js` | Biblioteca PeerJS 1.5.4 para la conexión directa (licencia MIT, ver `LICENSE-peerjs.txt`). |
| `.nojekyll` | Le dice a GitHub Pages que sirva los archivos tal cual. |

Las tipografías se cargan de Google Fonts.

## Probarlo en tu ordenador

Abrir `index.html` con doble clic sirve para la práctica y el tutorial. Para probar el modo en línea, sirve la carpeta por HTTP, por ejemplo:

```
python -m http.server 8000
```

y abre `http://localhost:8000` en dos ventanas.
