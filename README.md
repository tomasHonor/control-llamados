# Mi Cartera de Clientes

App web para llevar el control de llamados a clientes con promesa de pago (gestión de cobranzas / mora temprana).

## Cómo funciona

- **Alta de cliente:** nombre y apellido, DNI y fecha de promesa (teléfono, monto y notas son opcionales). El horario del llamado se toma de la hora en que cargás la ficha (editable).
- **Promesa normal:** se elige de un desplegable con el día de carga y los 4 días hábiles siguientes. La app agenda un llamado para **verificar el pago** el día hábil siguiente al vencimiento.
- **Promesa negociada:** si el cliente da una fecha posterior, se carga igual con "Otra fecha". La app agenda un llamado **5 días hábiles antes** para registrarla en el sistema; al marcarla como registrada, pasa a agendarse la verificación del pago.
- **Días hábiles:** se descuentan sábados, domingos y feriados nacionales de Argentina (2026–2027). Desde Opciones se pueden agregar feriados extra.
- **Hoy:** llamados del día ordenados por horario, atrasados y los del próximo día hábil.
- **Calendario:** vista mensual con la cantidad de llamados por día; al tocar un día se ve el detalle.
- **Resultado de cada llamado:** registrada, pagó, no contesta (pasa al próximo día hábil), nueva promesa o no va a pagar. Todo queda en el historial y se puede deshacer.

## Cómo se guardan los datos

Los datos se guardan en el `localStorage` del navegador donde se abre la app (no hay backend). Usá el botón de exportar backup para no perder la información si cambiás de navegador o PC.

## Uso

Abrir `index.html` en el navegador, o usar la versión publicada en GitHub Pages: https://tomashonor.github.io/control-llamados/
