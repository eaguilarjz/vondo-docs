---
title: App Móvil
parent: Español
nav_order: 13
---

> {% include lang-globe.html %} Read this page in [English](../../en/mobile/)

# App Móvil

vondo está disponible en iOS y Android como una app nativa multiplataforma. Misma cuenta, mismos datos, mismo presupuesto — solo optimizada para un teléfono en tu bolsillo mientras estás formado en la fila del super decidiendo si la bolsa de granola de $7 es "Comida" o "Restaurantes."

Esta página cubre todo lo que es específico de la app móvil: cómo está organizada, cómo se mantiene sincronizada con la web, y el puñado de cosas que la móvil aún no hace.

---

## Instalación

Busca **Vondo** en la App Store (iOS) o Play Store (Android), instala y entra con la misma cuenta que usas en la web. Todo lo que ya configuraste — cuentas, categorías, presupuestos, reglas recurrentes, vistas guardadas, todo — aparece en el teléfono de inmediato.

Si aún no te has registrado, también puedes crear tu cuenta desde la pantalla de inicio de sesión móvil. Consulta [Primeros pasos → Crea tu cuenta](../getting-started/#crea-tu-cuenta-y-empieza-tu-prueba-gratuita) para el flujo (los pasos son los mismos en móvil).

---

## Pestañas

La parte inferior de la pantalla tiene cinco pestañas:

| Pestaña | Qué encuentras |
|---|---|
| **Inicio** | Un resumen del mes actual — Por asignar arriba, categorías sobregiradas que necesitan atención, actividad reciente. |
| **Presupuesto** | El presupuesto completo del mes actual: grupos, categorías, Asignado / Gastado / Disponible por categoría. Toca una categoría para abrir la hoja de detalle (asignar dinero, fijar un objetivo, ver historial). |
| **Actividad** | Cada transacción de todas tus cuentas, con pills de filtro y búsqueda. |
| **Cuentas** | Todas tus cuentas agrupadas por tipo. Toca una para ver su pantalla de detalle con transacciones y el botón de conciliar. |
| **Informes** | Los mismos cuatro informes que la web — Ingresos vs Gastos, Ahorro Neto, Gasto por Categoría, Beneficiarios Principales. |

### El menú "…"

Las cosas que no viven en una pestaña — Categorías, Beneficiarios, Recurrentes, Perfil, Hogares, Seguridad, Plan y Facturación, Sesiones Activas, Cambios Pendientes — se abren desde un botón **…** en las pantallas de Inicio, Presupuesto y Actividad. Tócalo y se abre una hoja con todos los destinos secundarios agrupados por tema.

Tomamos este enfoque porque la barra de pestañas inferior se llena rápido, y las guías de Apple recomiendan máximo cinco. El resultado: las cinco cosas que haces todos los días están a un toque; el resto, a dos.

### Selector de hogar

Si eres miembro de más de un [hogar](../hogares/), el menú "…" también muestra un **selector de hogar**. Tócalo y se abre una hoja que lista cada hogar al que perteneces, con tu insignia de rol, el conteo de miembros y una marca de **Activo** junto al que estás usando. Toca cualquier entrada para cambiarte — el presupuesto, las cuentas y la actividad se recargan para mostrar los datos de ese hogar. Tu sesión, tema e idioma permanecen igual.

---

## Funciona offline: cómo la móvil se mantiene útil con mala conexión

La mayor diferencia con la web es que **la app móvil sigue funcionando cuando se cae tu conexión**. Puedes registrar transacciones, asignar dinero, mover dinero entre categorías y editar casi cualquier cosa mientras estás en el metro, en un avión o en ese café del fondo con Wi-Fi terrible.

### Qué pasa cuando estás sin conexión

1. **La app muestra un banner arriba** — *Estás sin conexión — los cambios se sincronizarán cuando vuelvas a conectarte*.
2. **Las lecturas vienen del almacenamiento local.** Tus cuentas, categorías, presupuesto y actividad reciente están en caché en el dispositivo, así que la app carga al instante incluso sin señal.
3. **Las escrituras entran a una cola.** Cuando creas una transacción, editas una categoría o mueves dinero, el cambio aplica localmente de inmediato — ves los números nuevos al momento — y se agrega a una cola de **escrituras pendientes**.
4. **Cuando vuelves a conectarte**, la cola se reproduce automáticamente. Sin botón que presionar. El banner desaparece cuando todo está sincronizado.

> **Ejemplo trabajado — un vuelo de CDMX a Nueva York:**
>
> 1. Despegas. El teléfono entra en modo avión. Aparece el banner de offline de vondo arriba.
> 2. A media altura recuerdas que le debes $40 a tu roomie por los servicios. Lo registras como una Transferencia de tu Cuenta corriente a "Préstamos a roomie" — aparece en tu Actividad al instante y **Cambios pendientes** sube a "1 cambio sin sincronizar."
> 3. Subiéndote a un vuelo de conexión te compras un sándwich y un café. Dos transacciones más entran. Ahora "3 cambios sin sincronizar."
> 4. Aterrizas en NY y apagas el modo avión. En unos segundos el banner desaparece, el contador de Cambios pendientes baja a cero, y las tres transacciones ya están en el servidor. Abres la app web en el Uber y ahí están.
>
> No hiciste nada especial. Sin botón de "sincronizar ahora", sin reintentos, sin volver a correr nada. La app simplemente se puso al día.

### La pantalla de Cambios Pendientes

Abre **… → Cambios pendientes** para ver exactamente qué hay en cola. Cada fila muestra:

- Una descripción del cambio ("Agregar transacción en Costco", "Editar categoría Renta", etc.)
- Su estado actual — **Esperando sincronizar**, **Enviando…**, o **Falló**
- Una marca de tiempo

Si un cambio falla (típicamente porque el servidor lo rechaza — p. ej. editaste una categoría en web que ya habías eliminado en el teléfono), verás un botón **Reintentar** o **Descartar** en la fila que falló. Reintentar la manda de nuevo; Descartar tira el cambio y lo saca de la cola.

> **Atención:** Si una escritura falla varias veces, es señal de que la copia local se separó del servidor. Lo más seguro es descartar la escritura fallida, hacer pull-to-refresh en la pantalla afectada para obtener una copia fresca del servidor, y rehacer el cambio con los datos actualizados enfrente.

---

## Inicio de sesión y seguridad en móvil

La app móvil usa el mismo sistema de autenticación que la web: correo + contraseña, Continuar con Google, y Continuar con Microsoft. Después de iniciar sesión, aplican los mismos flujos de [autenticación de dos factores](../security/#autenticación-de-dos-factores-mfa) y [dispositivos de confianza](../security/#dispositivos-de-confianza).

Un par de notas específicas de móvil:

- **Cerrar sesión borra los datos locales.** Cerrar sesión en un teléfono limpia el caché local del dispositivo, la cola de escrituras pendientes y el cursor de sincronización — así que la siguiente persona que inicie sesión (tú u otra) empieza limpia. El cierre de sesión en web solo limpia los tokens; el móvil limpia tokens *y* la base de datos en el dispositivo.
- **Las sesiones activas muestran tus teléfonos.** Tus dispositivos móviles aparecen en **Seguridad → Sesiones activas** junto con los navegadores web. Revoca una sesión de teléfono desde la web si pierdes un dispositivo.

## Cuando termina la prueba (o se pausa una suscripción)

Si tu prueba expira o tu suscripción queda en pausa sin un plan activo, la app móvil muestra una pantalla de **bloqueo de suscripción** al abrirla — una señal de alto amigable que:

- Te dice que la prueba terminó (o que la suscripción está en pausa), con la fecha.
- Tiene un único botón **Administrar suscripción** que abre el portal de facturación en tu navegador.
- Se queda al frente de la app hasta que arregles la facturación — aún puedes cerrar sesión, pero no llegas a Presupuesto / Actividad / etc.

Tus datos están completamente a salvo. El bloqueo es una pausa de acceso; en cuanto te suscribas o reanudes desde el portal, la próxima vez que abras la app móvil te deja pasar directo a donde te quedaste.

---

## Lo que es igual

Casi todo. Para ahorrarte leer las demás páginas de ayuda otra vez, esto es lo que funciona idéntico:

- Los cuatro tipos de transacción (Ingreso, Gasto, Transferencia, Crédito) más Pago de Deuda, con divisiones
- Las seis [estrategias de llenado rápido](../budget/#estrategias-de-llenado-rápido)
- El modal de [Cambios Recientes](../budget/#cambios-recientes)
- [Mover dinero](../budget/#mover-dinero-entre-categorías) entre categorías
- Los cuatro [tipos de objetivo](../budget/#objetivos-también-llamados-metas) (Mensual, Semanal, Anual, Personalizado) con arrastre
- Las cinco [frecuencias recurrentes](../recurring/#frecuencias), el modal de previsualización al aplicar vencidos, y pagos de deuda recurrentes
- Los seis [tipos de cuenta](../accounts/#tipos-de-cuenta) incluyendo tarjetas de crédito con límite opcional y la categoría de pago vinculada que se autofinancia conforme gastas
- [Conciliación](../reconcile/)
- [Informes](../reports/) — las cinco gráficas (Ingresos vs Gastos, Ahorro Neto, Patrimonio Neto, Gastos por Categoría, Beneficiarios Principales) con los mismos preajustes de rango de tiempo y filtros de Cuenta y Categoría que la web
- Deshacer / Rehacer (toca las flechas curvas en la barra superior)
- Todas tus [vistas guardadas](../actividad/#vistas-guardadas), filtros y el cuadro de búsqueda
- Tema **Sistema / Claro / Oscuro** e idioma

### Detalles de móvil

Un puñado de pequeños toques que móvil tiene además de la paridad:

- **Crear en línea desde el formulario de transacción.** Cuando estás capturando una transacción y necesitas una categoría o beneficiario que aún no existe, escribe un nombre que no coincida con nada y aparece una opción **"Crear *<nombre>*"** al final de las sugerencias. Tócala y la entidad se crea ahí mismo — sin tener que salir del formulario, ir a la pantalla de Categorías o Beneficiarios, y regresar.
- **Crear en línea desde el formulario recurrente también.** Mismo atajo cuando configuras una cuenta recurrente.
- **Pull-to-refresh** en cualquier pantalla de lista fuerza una sincronización fresca con el servidor.

---

## Lo que es solo web (por ahora)

Algunas cosas viven solo en la app web. Ninguna te impide el día a día; son tareas administrativas de borde o flujos que necesitan una pantalla más grande:

- **Importación CSV.** Importar un año de transacciones bancarias desde un CSV es una tarea de escritorio — los selectores de archivos y el mapeo de columnas funcionan mucho mejor en una laptop. Usa la página web de [Importar y Exportar](../import-export/).
- **Tokens de búsqueda avanzados.** La búsqueda móvil soporta el cuadro de búsqueda y los pills de filtro, pero la sintaxis abreviada `category:Comida`, `>100`, `since:YYYY-MM-DD` es solo web.
- **Reordenar categorías arrastrando.** En móvil, reordenas categorías desde la pantalla de edición con controles arriba/abajo. La web tiene drag-and-drop real.
- **Cambios de plan.** Suscribirse, cancelar y actualizar métodos de pago corre todo por el portal de facturación, que se abre en tu navegador — incluso desde la app móvil. La app móvil te lleva al portal automáticamente.
- **Asistente de configuración.** La web tiene el asistente completo de configuración; la móvil muestra una pantalla breve de bienvenida y asume que harás la configuración inicial desde una laptop.

---

## Notificaciones push, desbloqueo biométrico, sincronización en segundo plano

No están en esta versión:

- **Sin notificaciones push.** La app móvil no te avisa sobre nada — sin resúmenes diarios, sin recordatorios, sin alertas de saldo. Podríamos agregar algunas opcionales más adelante.
- **Sin desbloqueo FaceID / TouchID.** El inicio de sesión es el flujo estándar de correo/contraseña (u OAuth) más MFA. La cookie de dispositivo de confianza te mantiene con sesión iniciada por 30 días, así que en la práctica raramente vuelves a autenticarte.
- **Sin sincronización en segundo plano.** La cola se sincroniza cuando la app está abierta y conectada (al instante al reconectar, y al enfocar la pantalla). Cerrar la app no drena los cambios pendientes — esperan a que vuelvas a abrirla.

---

## Consejos

- **Usa el teléfono para capturar, la laptop para configurar.** La mayoría de la gente termina usando la móvil para registrar transacciones durante el día y la web los domingos en la noche para la revisión mensual.
- **Pull-to-refresh en cualquier pantalla de lista.** Si crees que el servidor tiene datos más nuevos, desliza hacia abajo — vondo trae una foto fresca y la reconcilia con lo que tengas en la cola de pendientes.
- **No te preocupes por el banner de offline.** No es un error; es un estado. La app sigue funcionando. Tus cambios están seguros localmente y se sincronizarán cuando vuelvas a estar en línea.
- **Cierra sesión antes de prestar el dispositivo.** Si alguien te pide tu teléfono para un vuelo, cierra sesión primero. Volver a entrar es rápido (un toque con Google/Microsoft, o tu contraseña + un código MFA si lo tienes activado).
