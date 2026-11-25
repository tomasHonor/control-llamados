# Mi Cartera de Clientes

App web para llevar el control de llamados a clientes con promesa de pago (gestión de cobranzas / mora temprana).

## Cómo funciona

- **Buscador arriba de todo:** escribís el DNI o el nombre y la app te dice si es **Negociación** (llamar para registrar la promesa) o **Promesa** (llamar para verificar el pago), y cuándo llamarlo. Si no está cargado, te ofrece cargarlo.

- **Alta de cliente:** nombre y apellido, DNI y fecha de promesa (teléfono, monto y notas son opcionales). El horario del llamado se toma de la hora en que cargás la ficha (editable).
- **Promesa normal:** se elige de un desplegable con el día de carga y los 4 días hábiles siguientes. La app agenda un llamado para **verificar el pago** el día hábil siguiente al vencimiento.
- **Promesa negociada:** si el cliente da una fecha posterior, se carga igual con "Otra fecha". La app agenda el llamado para el **primer día hábil en que el sistema ya permite registrarla** (ese día + 4 hábiles llega a la fecha prometida); al marcarla como registrada, pasa a agendarse la verificación del pago.
- **Días hábiles:** se descuentan sábados, domingos y feriados nacionales de Argentina (2026–2027). Desde Opciones se pueden agregar feriados extra.
- **Hoy:** llamados del día ordenados por horario, atrasados y los del próximo día hábil.
- **Calendario:** vista mensual con la cantidad de llamados por día; al tocar un día se ve el detalle.
- **Resultado de cada llamado:** registrada, pagó, no contesta (pasa al próximo día hábil), nueva promesa o no va a pagar. Todo queda en el historial y se puede deshacer.

## Herramientas para el día a día

- **Botones rápidos** en la lista de Hoy: pagó, nueva promesa, no contesta, registrada y copiar, sin abrir la ficha.
- **Recordatorios** a la hora de cada llamado (notificación del navegador, mientras la app esté abierta).
- **Copiar para el sistema:** copia "DNI - nombre - promesa - monto" para pegar en el sistema de la empresa.
- **Intentos sin respuesta:** muestra cuántas veces seguidas no contestó y sugiere WhatsApp o cerrar el caso a partir de 3.
- **WhatsApp con mensaje armado** según el estado de la promesa.
- **Resumen** del día, la semana y el mes: llamados, contactados, pagos, monto recuperado y estado de la cartera.
- **Aviso de backup** si pasan 7 días sin exportar.

## Cómo se guardan los datos

Los datos se guardan en el `localStorage` del navegador donde se abre la app (no hay backend). Usá el botón de exportar backup para no perder la información si cambiás de navegador o PC.

## Uso

Abrir `index.html` en el navegador, o usar la versión publicada en GitHub Pages: https://tomashonor.github.io/control-llamados/
