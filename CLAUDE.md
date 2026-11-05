# CLAUDE.md · boletas (Boletería Barakah)

Responde y comenta en español. Sé breve: muestra solo los cambios, no repitas archivos completos.

## Qué es
- Plataforma de venta de boletas de la Corporación Barakah, en producción desde el 02-nov-2026.
- Página pública: https://ovedlr.github.io/boletas/ (GitHub Pages desde `main`).
- Rutas: `#/admin` (panel, también de inscripciones) y `#/porteria` (celulares de la entrada).
- Servidor: Google Apps Script "Boletería Barakah" (cuenta infobarakah.co@gmail.com); su URL `/exec` está en `API_URL`.
- La copia de referencia del servidor es `servidor/Codigo.gs` del repo `Ovedlr/barakahco` (v11).
  No crees otra copia del servidor en este repo.

## Estructura
- `index.html`: toda la aplicación en un solo archivo (unos 400 KB).
  **No lo leas completo**: busca con grep la sección que necesitas y lee solo esas líneas.
- `logo-redondo.png` (principal) y `logo-horizontal.png` (pie, con eslogan).

## Reglas de negocio (no cambiar sin aprobación de Oved)
- Pagos solo por Nequi 314 777 9678 y Bancolombia ahorros 10537311952; confirmación manual en el panel.
  Las boletas se apartan 12 horas. Wompi desactivado (el código se conserva).
- Sin cargo por servicio ni IVA. Aforo manual por evento; la venta se cierra sola al tope.
- Boletas solo por correo, con QR, al confirmar el pago. Nunca por WhatsApp.
- Comprobantes al WhatsApp 300 322 0443 con la referencia; información general al 314 777 9678.
- Referencias: `BK-XXXXX` (boletas), `IN-` (inscripciones), `SM-` (Semillas), `SA-` (solicitudes de Sara).
  Sin caracteres confusos (0/O, 1/I/L). Las `BKH…` antiguas deben seguir funcionando.
- Estudiantes: foto del carné con el comprobante; en portería, franja "PIDE EL CARNÉ".
- Devoluciones solo si el evento se cancela.

## Datos y límites
- Base real: hoja "Boletería Barakah" en Drive. Nunca borrarla. "Reiniciar datos" pide clave y guarda respaldo.
- Gmail gratuito: unos 100 correos al día.
- Claves en Propiedades del script; nunca en el código ni en commits.

## Cambios y publicación
- Cambios en una rama `claude/<tema>`; a `main` solo con aprobación de Oved (se publica al instante).
- Servidor: pegar el nuevo `Codigo.gs`, guardar, Implementar → Gestionar implementaciones → Editar → Nueva versión.
  La URL no cambia. No volver a ejecutar "instalar".

## Identidad
`#faba2f`, `#fecb4a`, `#301638`, textos `#000`/`#fff`; Cinzel en títulos y Montserrat en el resto.
