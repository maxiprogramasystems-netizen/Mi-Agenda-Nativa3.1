<p align="center"><img src="icon-192.png" width="120" alt="Logo Mi Agenda"></p>

# Mi Agenda

App web (PWA) para control de turnos, clientes e ingresos de manicura. Funciona sin conexión y se instala en la pantalla de inicio (Android/iPhone). No usa librerías externas: la exportación a Excel está incluida en `index.html`.

## Archivos (todos en la raíz del repositorio)
`index.html` · `manifest.json` · `sw.js` · `icon-192.png` · `icon-512.png` · `icon-maskable-512.png` · `README.md`

## Funciones
- Turnos: cliente, servicio, fecha, hora y costo (opcional, editable tocando el valor en la lista). Editar, eliminar, marcar como atendido. Se muestran siempre en estricto orden de ingreso (número de secuencia propio; editar no cambia la posición).
- Transporte por cita (opcional): medio de transporte, costo de ida y costo de regreso. El panel muestra total de transporte y ganancia neta (ingresos − transporte).
- Reloj y fecha en vivo en el encabezado; cada turno muestra su fecha (día/mes) y hora en etiquetas.
- Hora en 24 h o 12 h (AM/PM).
- Panel: clientes, pendientes, atendidos e ingresos (suma de atendidos). Recordatorios de las próximas 48 h y notificaciones.
- Exportar a Excel (.xlsx) con orden de ingreso, columnas de transporte y totales.
- Modo claro/oscuro/automático y fondos acuarela (Lila, Rosa, Durazno, Menta, Cielo).
- Seguridad opcional: PIN de 4 a 6 dígitos o contraseña alfanumérica, huella/Face ID, quitar o recuperar contraseña (no borra los turnos).

## Publicar en GitHub Pages
1. Crea un repositorio y sube todos los archivos a la raíz ("uploading an existing file").
2. Settings > Pages > rama `main`, carpeta `/ (root)`.
3. Abre el link HTTPS en el celular y usa "Agregar a pantalla de inicio" (Chrome: "Instalar aplicación"; Safari: Compartir > Agregar a pantalla de inicio).

## Actualizar la app
La app se actualiza sola: cada vez que se abre el link (o se vuelve a ella) revisa si hay versión nueva, la descarga y se recarga sin reinstalar. Los datos (turnos, ajustes, contraseña) no se pierden porque se guardan aparte del código. Si estás escribiendo un turno, muestra un aviso para actualizar cuando termines.

Para publicar un cambio: cambia también el número de versión en `sw.js` (`const V = 'mi-agenda-v3.4.0'`) para que los celulares reciban la actualización.

## Íconos
Para usar tu propia imagen, reemplaza `icon-192.png` (192×192) e `icon-512.png` (512×512) conservando los nombres.

## Datos y privacidad
Todo se guarda solo en el navegador del dispositivo (localStorage). La contraseña es un bloqueo de privacidad local, no cifra los datos.

Versión 3.4
