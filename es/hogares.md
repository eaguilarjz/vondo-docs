---
title: Hogares
parent: Español
nav_order: 12
---

> {% include lang-globe.html %} Read this page in [English](../../en/households/)

# Hogares

Un **hogar** es donde vive un presupuesto de savr. Las cuentas, categorías, transacciones, reglas recurrentes, informes — todo está dentro de un hogar. Hasta cinco personas pueden compartir el acceso.

Si eres la única persona en la cuenta, está bien: simplemente tienes un hogar con un miembro. Pero si alguna vez has querido que tu pareja pueda ver el presupuesto del supermercado sin molestarte, o que dos adultos de la misma familia registren sus propios gastos en un mismo plan compartido, esto es lo que lo hace posible.

---

## La forma del modelo

| Cosa | Dónde vive | Qué significa |
|---|---|---|
| Cuentas, categorías, transacciones, recurrentes, objetivos, informes, vistas guardadas, el presupuesto mismo | **El hogar** | Compartido con cada miembro. Las ediciones de uno son visibles para todos. |
| Plan y suscripción, periodo de prueba | **El hogar** | El hogar paga por sí mismo. Los miembros no reciben cargos por separado. |
| **Moneda y zona horaria** | **El hogar** | Iguales para cada miembro, para que los números y las fechas signifiquen lo mismo para todos. **Sólo el Propietario puede cambiarlas.** |
| Nombre, correo, contraseña, MFA, dispositivos confiables, sesiones activas | **Tu cuenta de usuario** | Sólo tuya. Permanece igual sin importar en qué hogar estés. |
| Tema e idioma | **Tu cuenta de usuario** | Personales — cada miembro elige los suyos. Los datos del hogar se muestran con tus preferencias. |

Puedes ser **miembro de varios hogares** y cambiar entre ellos. Puedes **ser propietario de un hogar a la vez** (aquel cuya suscripción pagas).

---

## Roles

Sólo dos:

| Rol | Puede hacer |
|---|---|
| **Propietario** | Todo: editar el presupuesto, invitar miembros, eliminar miembros, revocar invitaciones pendientes, transferir la propiedad, eliminar el hogar. Paga la suscripción. |
| **Miembro** | Edita el presupuesto normalmente. Puede salir del hogar cuando quiera. No puede gestionar a otros miembros ni la facturación. |

Exactamente **un Propietario** por hogar. El Propietario no puede salir — tiene que transferir la propiedad a otro miembro o eliminar el hogar. Los demás miembros pueden entrar y salir libremente.

---

## Crear un hogar

Si acabas de registrarte, ya tienes uno — savr crea un hogar para ti en tu primer inicio de sesión, lo nombra como tú, elige una **moneda** y una **zona horaria** por defecto a partir de la configuración regional de tu navegador, y empieza la prueba de 90 días. Eres el Propietario. Puedes renombrarlo (y cambiar la moneda y la zona horaria) después.

Si eres un usuario sin hogares (por ejemplo, te eliminaron de uno y no eres propietario de ninguno), verás una pantalla de bienvenida al iniciar sesión con dos opciones:

- **Crea tu hogar** — prueba fresca de 90 días, eres el Propietario, puedes invitar a hasta cuatro personas más. Elige un nombre (p. ej. "La familia Aguilar"), confirma la moneda y la zona horaria sugeridas (o cámbialas ahora si savr adivinó mal), listo.
- **Espera una invitación** — si alguien planea agregarte, la pantalla de bienvenida te dice a qué correo esperar la invitación, y se actualiza automáticamente cuando llega una.

> **Atención:** Sólo puedes **ser propietario** de un hogar a la vez. Si ya eres propietario de uno y quieres crear otro, tendrás que salir o eliminar el primero. Pero no hay límite en cuántos hogares puedes **ser miembro**.

---

## Moneda y zona horaria

Un hogar tiene una **moneda** y una **zona horaria**, y aplican a cada miembro.

No son una preferencia personal de visualización — son parte de los datos del hogar:

- **La moneda** es la unidad en que están denominadas tus cuentas y el presupuesto. savr no hace conversión de tipo de cambio, así que sólo tiene sentido si todos los que ven el presupuesto ven la misma moneda. Una línea de supermercado de $400 que sea $400 para un miembro y €400 para otro no significaría nada.
- **La zona horaria** controla los límites del mes de presupuesto — si una transacción registrada a las 11:30 PM del 31 de enero pertenece a enero o a febrero. Dos miembros en zonas horarias distintas igualmente necesitan ponerse de acuerdo en a qué mes pertenece cada transacción, así que el hogar elige una zona y la usa para todos.

### Quién las puede cambiar

**Sólo el Propietario.** Los miembros pueden ver la moneda y la zona horaria actuales en la página del hogar pero no pueden cambiarlas. El Propietario las edita desde **Perfil → Hogares → [nombre del hogar]** en la sección de ajustes del hogar.

> **Ejemplo concreto:** Configuras "Casa Aguilar" con MXN y `America/Mexico_City` cuando la creas. Tu pareja — que tiene su teléfono en inglés y usa modo oscuro — abre el mismo hogar y ve pesos y los mismos límites de mes que tú. Sus preferencias de tema e idioma siguen siendo suyas; el dinero y el calendario del hogar son compartidos.

### Cambiarlas después

Puedes cambiar cualquiera de las dos en cualquier momento, pero piénsalo:

- **Moneda:** cambiarla no convierte los saldos existentes. Una cuenta de $1,000 se queda en "1,000" — sólo se mostrará con el nuevo símbolo. Si de verdad necesitas pasar un hogar de USD a EUR con conversión real, exporta tus datos, crea un hogar nuevo en la moneda destino y vuelve a importar. (La mayoría de la gente sólo necesita cambiar la moneda una vez, justo después de crear el hogar.)
- **Zona horaria:** cambiarla puede mover el *mes de presupuesto* de una transacción por un día en la frontera. Para la mayoría es inofensivo. Si te mudas al otro lado del mundo, ten en cuenta que un par de transacciones tarde por la noche cerca de fin de mes pueden caer al mes anterior o siguiente tras el cambio.

Si eres Miembro y quieres que la moneda o la zona horaria del hogar cambie, pídeselo al Propietario — sólo él tiene el control.

---

## Invitar a alguien

Abre **Perfil → Hogares → [nombre del hogar] → Invitar a un nuevo miembro**.

1. Escribe el correo electrónico de la persona que quieres invitar.
2. Haz clic en **Enviar invitación**.
3. savr le envía un enlace por correo. El enlace es válido por **7 días**.

La nueva invitación pendiente aparece en la lista de **Invitaciones pendientes** del hogar. Si no la aceptan a tiempo, la invitación expira — simplemente envía una nueva.

Algunas reglas:

- **Tope de 5 personas.** Miembros + invitaciones pendientes combinadas no pueden exceder 5. Si está lleno, tendrás que eliminar a alguien o revocar una invitación pendiente antes de enviar una nueva.
- **Una invitación pendiente por correo** a la vez. No puedes enviar duplicados.
- **Por correo, no por nombre de usuario.** No necesitan tener una cuenta de savr todavía — el enlace de invitación los guía por el registro si hace falta.

> **Ejemplo concreto:** Estás configurando un hogar con tu pareja. Creas el hogar ("Casa Aguilar"), luego haces clic en **Invitar a un nuevo miembro**, escribes su correo y envías. Reciben un correo titulado *"Estás invitado a Casa Aguilar."* Hacen clic en el enlace, se registran en savr (o inician sesión si ya tienen cuenta), aceptan y eligen cambiarse a Casa Aguilar inmediatamente. Ahora ambos ven el mismo presupuesto.

---

## Aceptar una invitación

Cuando haces clic en un enlace de invitación en tu correo, savr abre una página de vista previa que muestra:

- A qué hogar te han invitado
- Quién te invitó
- A qué dirección de correo se envió la invitación

Si **no has iniciado sesión**, se te pedirá iniciar sesión o crear una cuenta de savr. Puedes usar cualquier correo — el que recibió la invitación es sólo una pista de enrutamiento; tu cuenta de savr puede usar un correo diferente sin problema.

Si **ya iniciaste sesión**, dos botones:

- **Aceptar invitación** — te une al hogar. Luego eliges **Cambiar a este hogar ahora** o **Quedarme donde estoy** (en cuyo caso el nuevo hogar aparece en tu selector y puedes cambiarte más tarde).
- **Quizá después** — cierra la página sin aceptar. La invitación sigue válida durante el resto de su ventana de 7 días.

Los enlaces expirados o inválidos muestran una pantalla limpia de "esta invitación no se puede usar". Pídele al invitador que envíe una nueva.

---

## Cambiar de hogar

Si eres miembro de más de un hogar, verás un **selector** en la parte superior de la navegación (web) o bajo el menú "…" (móvil). Tócalo para ver la lista. Cada entrada muestra:

- El nombre del hogar
- Tu rol (una insignia de **Propietario** si eres el dueño)
- El conteo de miembros
- Una insignia **Activo** en el que estás usando actualmente

Toca cualquier entrada para cambiarte. El presupuesto, las cuentas y la actividad se actualizan para mostrar los datos de ese hogar. Tu perfil, preferencias y ajustes de seguridad permanecen igual.

> **Uso común:** un freelancer con un hogar personal y un hogar de "negocio" para los gastos de clientes. Cambia entre ellos dependiendo del dinero de quién esté gastando. Mismo login, dos presupuestos, sin mezcla.

---

## Gestionar miembros

Abre **Perfil → Hogares → [nombre del hogar]** para ver:

- La lista de miembros (con una insignia de Propietario en quien lo sea)
- Tus invitaciones pendientes
- Formularios para invitar nuevas personas, transferir la propiedad y (para propietarios) eliminar el hogar

### Eliminar a un miembro (sólo Propietario)

Haz clic en **Eliminar** junto al miembro que quieres quitar. Confirma. Pierden acceso al presupuesto de este hogar inmediatamente.

Su cuenta de savr no se ve afectada — conservan sus otros hogares, su perfil, sus sesiones, todo. Sólo este hogar desaparece de su vista.

El Propietario no puede eliminarse a sí mismo; para eso, usa Transferir propiedad o Eliminar hogar más abajo.

### Revocar una invitación pendiente (sólo Propietario)

En la lista de **Invitaciones pendientes**, haz clic en **Revocar** junto a la invitación. El token deja de funcionar inmediatamente — si el invitado hace clic en el enlace después de la revocación, verá la pantalla de "esta invitación no se puede usar".

### Salir de un hogar (Miembros)

Abre la página del hogar, haz clic en **Salir del hogar**, confirma. Pierdes el acceso de inmediato. El Propietario recupera el lugar para invitar a alguien más si quiere.

Si cambias de opinión, el Propietario puede volver a invitarte.

### Transferir la propiedad (sólo Propietario)

Abre la página del hogar, baja a **Transferir propiedad**, elige un miembro del desplegable, haz clic en **Transferir**. Confirma.

Después de la transferencia:

- El nuevo Propietario hereda todos los poderes (invitar, eliminar, borrar).
- Tú pasas a ser un Miembro regular. Puedes seguir viendo y editando el presupuesto; sólo ya no gestionas membresía ni facturación.

Un miembro sólo puede convertirse en Propietario si no es propietario de otro hogar. Si lo es, tendría que salir o eliminar el otro primero.

> **Cuándo importa esto:** quien paga la suscripción debe ser el Propietario. Si la cuenta debe pasar de ti a tu pareja, transfiere la propiedad y luego ella puede suscribirse (o tomar el control de la suscripción activa, según tu acuerdo de facturación).

---

## Eliminar un hogar

Esta es la opción destructiva. **Borra todo lo que hay en el hogar:** cuentas, transacciones, categorías, reglas recurrentes, informes, acceso de miembros. Es irreversible.

Pasos (sólo Propietario):

1. Abre **Perfil → Hogares → [nombre del hogar]**.
2. Baja a **Eliminar hogar**.
3. Lee la advertencia. Escribe el nombre del hogar para confirmar.
4. Haz clic en **Eliminar permanentemente**.

Algunas condiciones previas:

- **Sin suscripción activa.** Si el hogar tiene un plan de pago, cancélalo desde el portal de facturación primero. savr no eliminará un hogar de pago para prevenir cargos sorpresa.
- **Sólo Propietario.** Los miembros no pueden eliminar; sólo pueden salir.

Los demás miembros del hogar pierden el acceso inmediatamente y no se les cobrará nada.

---

## Eliminar hogar vs. eliminar cuenta

Son operaciones **distintas**:

| Acción | Qué desaparece | Dónde encontrarla |
|---|---|---|
| **Salir del hogar** | Tu acceso a este hogar específico | Página de Hogares → Salir |
| **Eliminar el hogar** | El hogar y todo lo que tiene. Tu cuenta de usuario permanece. | Página de Hogares → Eliminar (sólo Propietario) |
| **Eliminar tu cuenta de savr** | Tu cuenta de usuario misma. Pierdes acceso a todos los hogares en los que estés. Si eres propietario de un hogar, primero tienes que transferirlo o eliminarlo. | Perfil → Zona de Peligro → Eliminar mi cuenta |

---

## Hogares y facturación

La suscripción pertenece al **hogar**, no a ti.

- Cada hogar tiene su propia **prueba de 90 días**.
- Cada hogar tiene su propio **plan** (Mensual / Trimestral / Anual) y su propio portal de facturación.
- El **Propietario** paga el hogar. Los miembros no reciben cargos por separado.
- Si la suscripción del Propietario caduca o la prueba termina sin un plan, **todo el hogar pasa a sólo lectura** hasta que el Propietario vuelva a suscribirse. Los miembros no pueden arreglarlo — sólo el Propietario tiene los controles de facturación.

Un ejemplo concreto:

> Tú y tu pareja comparten "Casa Aguilar" — eres el Propietario. También perteneces a "Mamá y Papá" (el hogar familiar, donde tu mamá es la Propietaria). Tú pagas la suscripción de Casa Aguilar. Tu mamá paga Mamá y Papá. Cuando cambias a Mamá y Papá, ves el plan que tu mamá tiene. Cuando regresas a Casa Aguilar, ves el tuyo.
>
> Si tu mamá olvida renovar Mamá y Papá, ese hogar pasa a sólo lectura para todos (tú incluido) hasta que ella lo resuelva. Tu suscripción de Casa Aguilar no se ve afectada.

Mira [Plan y Facturación](../billing/) para todos los detalles de la suscripción.

---

## Escenarios comunes

| Situación | Cómo manejarla |
|---|---|
| **Compartir un presupuesto con una pareja** | Uno de ustedes se registra primero, crea el hogar e invita al otro. Ambos editan el mismo presupuesto. |
| **Presupuestos personal + trabajo** | Crea dos hogares. Cambia entre ellos con el selector. Cada uno tiene su propia suscripción. |
| **Presupuesto familiar con hijos adultos** | Los padres crean el hogar familiar e invitan a los hijos. Los hijos también pueden tener sus propios hogares personales si quieren — sin conflicto. |
| **Contador gestionando presupuestos de clientes** | Te invitan a cada hogar de cliente como Miembro. Cambias entre ellos según trabajes. El cliente conserva la Propiedad y la facturación. |
| **Pasar de solo a compartido a mitad de presupuesto** | Sólo invita a la segunda persona. Se une al hogar existente con todo su historial. Nada se migra ni se divide. |
| **Separarse cuando un presupuesto compartido ya no tiene sentido** | El Propietario puede transferir la propiedad a la otra persona si hace falta, o cada uno crea su propio hogar nuevo. Los datos del hogar original van a donde el Propietario los lleve. |

---

## Consejos

- **Elige un nombre de hogar específico.** "Presupuesto" funciona cuando tienes un hogar; en el momento que tengas dos, vas a querer "Casa Aguilar" y "Aguilar Consultoría" para distinguirlos en el selector.
- **Usa la Propiedad con moderación.** La mayoría de hogares sólo necesitan un Propietario. Si están en pareja, decidan juntos quién será el Propietario; la otra persona es Miembro con acceso completo de edición. Los mismos poderes en el día a día, menos momentos de "espera, ¿quién paga esto?".
- **El tope de 5 miembros existe por una razón.** Los hogares están diseñados para parejas, familias y configuraciones pequeñas de contabilidad — no para equipos enteros. Si intentas presupuestar entre más de 5 personas, probablemente buscas un tipo distinto de herramienta.
- **Las invitaciones son reenviables.** El enlace en el correo contiene un token de un sólo uso; cualquiera con el enlace puede aceptar. Trátalo como una contraseña. Envíalo directamente a la persona, no en un canal público.
- **Mantén sano el hogar del que eres Propietario.** Si eres Propietario, tu suscripción alimenta a todos los del hogar. Actualiza tu método de pago cuando la tarjeta caduque; renueva antes de que termine la prueba. Los miembros no pueden rescatar el hogar — sólo tú.
