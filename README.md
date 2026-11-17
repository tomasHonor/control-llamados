# Mi Cartera de Clientes

App web simple para llevar el control de llamados a clientes (gestión de cobranzas / mora temprana).

## Qué hace

- Registra cada cliente con DNI, nombre, teléfono y monto adeudado (opcionales) y la fecha en que prometió pagar.
- Calcula automáticamente la fecha para volver a llamarlo (5 días antes de la promesa, ajustable), para no perderlo de vista aunque el sistema de la empresa solo permita agendar a 5 días vista.
- Muestra alertas de "llamar hoy" (incluye vencidos), "vencidos" y "esta semana".
- Botones para llamar o escribir por WhatsApp al cliente desde su ficha.
- Los cambios de estado, llamados y borrados se pueden deshacer, y un cliente cerrado puede volver a pendiente.
- Guarda un historial de cada llamado (no contesta, nueva promesa, reagendó, agendado en el sistema, pagó, no va a pagar).
- Permite exportar/importar un backup en JSON.

## Cómo se guardan los datos

Los datos se guardan en el `localStorage` del navegador donde se abre la app (no hay backend ni base de datos). Es ideal para uso personal desde un solo navegador/dispositivo. Usar el botón de exportar backup para no perder la información si se cambia de navegador o PC.

## Uso

Abrir `index.html` en el navegador, o publicarlo con GitHub Pages.
