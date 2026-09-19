# Operación A2 — V1

App privada para ejecutar en móvil los simulacros PDF con el formato de `Simulacro 08`.

## Qué hace
- Importa un PDF con preguntas A/B/C/D y plantilla final.
- Ejecuta el examen pregunta a pregunta.
- Permite avanzar, retroceder y dejar en blanco.
- Corrige al final.
- Guarda resultados e histórico en el propio navegador.
- No usa IA y no envía el contenido del test a ningún modelo.

## Arranque
Para que el navegador permita leer PDFs y usar el modo instalable, sirve esta carpeta con un servidor web.
En un PC con Python:
`python -m http.server 8000`
Después abre `http://IP_DEL_PC:8000` desde el móvil estando en la misma red.

La lectura PDF usa PDF.js desde CDN la primera vez. Una evolución posterior puede incluir PDF.js dentro del paquete para hacerlo 100% autónomo.

## Nota
La V1 calcula la nota como: (aciertos - fallos/3) / nº de preguntas * 10.
