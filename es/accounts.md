---
title: Cuentas
parent: Español
nav_order: 3
---

> {% include lang-globe.html %} Read this page in [English](../../en/accounts/)

# Cuentas

Las cuentas en savr reflejan los lugares reales donde vive tu dinero: cuentas bancarias, tarjetas de crédito, el efectivo de tu cartera, tu portafolio de inversión, el préstamo que se va achicando lentamente. Cada transacción pertenece a una cuenta y el saldo de cada cuenta se actualiza en el momento que registras actividad — así los totales en savr se mantienen en sintonía con la realidad.

Configúralas una vez. Mantenlas con dos minutos por semana.

---

## Tipos de cuenta

savr soporta seis tipos. El tipo importa porque controla cómo se agrupa la cuenta en la página, cómo se interpreta su saldo y qué funciones aparecen.

| Tipo | Úsalo para | Notas |
|---|---|---|
| **Cuenta corriente** | Gastos del día a día | Donde vive la mayoría de las transacciones |
| **Ahorro** | Dinero apartado | Se trata como Cuenta corriente para fines de presupuesto |
| **Tarjeta de Crédito** | Tarjetas de crédito | Gastar aquí no reduce una cuenta de efectivo; registra los pagos como Transferencias. Campo opcional de **límite de crédito** que aparece en la página de detalle. |
| **Efectivo** | Efectivo en mano | Dinero de bolsillo, ese sobre en el cajón |
| **Inversiones** | Brokerage, retiro, cripto | Sigue el saldo; no está pensado para detalle por operación |
| **Préstamo** | Hipotecas, créditos automotrices, créditos personales, créditos educativos | Tasa de interés, pago mensual, categoría de pago vinculada |

> Los préstamos son especiales — consulta [Cuentas de préstamo](#cuentas-de-préstamo) abajo para el tratamiento completo.

---

## Agregar una cuenta

1. Abre **Cuentas** y haz clic en **Agregar Cuenta**.
2. Ingresa:
   - **Nombre** — cómo aparece en todo savr (p. ej. "Chase Corriente")
   - **Tipo** — elige uno de los seis
   - **Saldo inicial** — lo que tiene la cuenta ahora mismo
3. Para préstamos, completa los campos específicos.
4. Haz clic en **Guardar**.

savr crea automáticamente una transacción de **Saldo Inicial** igual al monto que ingresaste. Está marcada de forma especial: establece el saldo de la cuenta pero no afecta tu presupuesto ni el gasto de las categorías.

> **Por ejemplo:** Agregaste una cuenta corriente con saldo inicial de $2,847.13. savr crea una transacción con esa fecha, marcada como Saldo Inicial, con ese monto. Tu cuenta muestra $2,847.13. Tu presupuesto no se afecta — ese dinero simplemente existe, listo para ser asignado.

---

## Cuentas de préstamo

Las cuentas de préstamo son donde savr se gana su sueldo. Te dan un lugar para llevar el control del saldo del capital, la tasa de interés y el pago para que la matemática se mantenga honesta cada mes.

Al crear o editar un préstamo, puedes configurar:

| Campo | Significado |
|---|---|
| **Tasa de interés** | Tasa anual en porcentaje. Se usa en informes y pagos recurrentes de deuda. |
| **Pago mensual** | El pago periódico esperado — se usa como valor por defecto al registrar pagos. |
| **Categoría de pago vinculada** | La categoría donde se cargan los intereses y comisiones del préstamo cuando registras un pago. |

Al crear un préstamo, puedes vincularlo a una **categoría existente** o pedir a savr que **cree una categoría nueva** (y opcionalmente la coloque en un grupo nuevo, como "Deuda"). De cualquier forma, los intereses caen en tu presupuesto como cualquier otro gasto — visibles, reales, planeados.

Para registrar pagos de préstamo con desglose de capital, intereses y comisiones, consulta [Pagos de deuda](../actividad/#pagos-de-deuda). Para pagos mensuales que se ejecutan en calendario, consulta [Pagos de deuda recurrentes](../recurring/#pagos-de-deuda-recurrentes).

> **Pro tip:** Cuando el préstamo esté pagado, [cierra la cuenta](#cerrar-una-cuenta) en lugar de eliminarla. El historial es parte de tu historia — querrás mirar atrás y ver el día que esa hipoteca llegó a cero.

---

## Tarjetas de crédito

Las tarjetas de crédito en savr funcionan distinto a la mayoría de las apps de presupuesto, y la diferencia es el punto entero: **el dinero se aparta solo para pagar la tarjeta conforme gastas, así que nunca te sorprende la cuenta.**

Esta sección explica exactamente cómo funciona.

### La categoría de pago — el superpoder silencioso de savr

Cuando creas una cuenta de tarjeta de crédito, savr crea automáticamente una **categoría de pago vinculada** para ella. Por defecto vive en un grupo llamado "Pagos de Tarjeta de Crédito" y se llama `Pago de <nombre de tu tarjeta>` (p. ej. "Pago de Chase Sapphire"). Puedes cambiar el grupo y el nombre al crear la cuenta, o vincular a una categoría existente en vez de crear una nueva.

Esa categoría de pago es el truco. Cada vez que cargas un gasto presupuestado a la tarjeta, savr mueve automáticamente ese dinero a la categoría de pago — así que los fondos para pagar la tarjeta ya están *apartados* para cuando llegue el estado de cuenta.

### Un ejemplo trabajado

Presupuestaste **$500 para Comida** en mayo. También tienes una tarjeta de crédito con su categoría vinculada **Pago de Chase Sapphire**.

5 de mayo — compras comida por **$80** en la tarjeta:

| Categoría | Antes | Después |
|---|---|---|
| Comida (Gastado) | $0 | $80 |
| Comida (Disponible) | $500 | $420 |
| Pago de Chase Sapphire (Disponible) | $0 | **$80** |
| Chase Sapphire (saldo adeudado) | $0 | $80 |

28 de mayo — pagas el estado: una **Transferencia de $80** Cuenta corriente → Chase Sapphire:

| Categoría | Antes | Después |
|---|---|---|
| Pago de Chase Sapphire (Disponible) | $80 | **$0** |
| Chase Sapphire (saldo adeudado) | $80 | $0 |
| Cuenta corriente (saldo) | … | bajó $80 |

La categoría de pago se llenó automáticamente conforme gastaste y se drenó al pagar. Nunca tuviste que acordarte de presupuestar "pago de tarjeta de crédito" — se cuidó solo.

### Qué pasa cuando te excedes en una categoría con la tarjeta

Si presupuestaste $500 para Comida y cargas $600, **solo los $500 que sí estaban presupuestados se mueven a la categoría de pago**. Los otros $100 quedan como sobregiro en Comida, lo que reduce el Por Asignar del mes siguiente — igual que cualquier sobregiro.

Esto mantiene la matemática honesta: la categoría de pago solo se autofinancia con dinero que estaba dentro de tu plan. El dinero que gastaste sin presupuestarlo es algo que tienes que abordar de verdad, no algo que la categoría de pago disimule por ti.

### Reembolsos y créditos

Una transacción tipo **Crédito** en la tarjeta (un reembolso) revierte todo limpiamente: el Gastado de la categoría baja, el saldo de la tarjeta baja, y el Disponible de la categoría de pago baja en el mismo monto. Sin importar el orden de cargos, reembolsos y pagos, los totales se mantienen balanceados.

### ¿Y si efectivo y tarjeta caen en la misma categoría?

savr camina las transacciones en orden cronológico y "cubre" el gasto con tarjeta solo hasta el punto en que el presupuesto de la categoría se acaba. Si presupuestaste $200 para Comida y gastas $100 en efectivo el día 5 y luego $150 con la tarjeta el día 10, los primeros $100 del cargo a la tarjeta caben en lo que queda del presupuesto ($100) y fluyen a la categoría de pago. Los otros $50 se convierten en sobregiro.

### Caso límite de varias tarjetas

Si usas *dos* tarjetas de crédito en la misma categoría y el reembolso de una tarjeta hace que el gasto neto vuelva a caber dentro del presupuesto, las cantidades por tarjeta en sus categorías de pago pueden no coincidir exactamente con la deuda real de cada tarjeta — una puede quedar "sobrefinanciada" en su categoría de pago y la otra "subfinanciada". El **total** siempre está bien; solo la división por tarjeta puede desfasarse. Si quieres correspondencia exacta por tarjeta, mueve dinero manualmente entre las dos categorías de pago.

### Registrar pagos

Un pago de tarjeta de crédito es una [Transferencia](../actividad/#transferencias) desde tu Cuenta corriente (o de donde salga el dinero) a la cuenta de la tarjeta. El saldo de la tarjeta baja, el saldo de la cuenta corriente baja, tu patrimonio neto general no cambia. **No registres el pago como un Gasto en la tarjeta** — eso lo contaría dos veces.

Para pagos automáticos mensuales, configura una [Transferencia recurrente](../recurring/#crear-una-transacción-recurrente) para que se ejecute el mismo día cada mes y la matemática se cuide sola para siempre.

### Límite de crédito (opcional)

Al crear o editar una cuenta de tarjeta de crédito, puedes establecer un **Límite de crédito**. Es un valor de referencia, no un tope duro — savr no bloquea transacciones cuando lo cruzas — pero el límite aparece en la página de detalle de la cuenta junto a tu saldo actual para que veas el margen de un vistazo.

Déjalo en blanco si no te interesa. Agrégalo después desde el editor de la cuenta cuando quieras.

### Consejos

- **Paga el saldo total del estado cada mes.** El sistema entero asume que lo haces. La categoría de pago tendrá exactamente el monto correcto.
- **Trata la categoría de pago como intocable.** Es el dinero que ya comprometiste a tu tarjeta. No lo muevas a otro lado a menos que de verdad no tengas saldo que pagar (lo cual sería raro).
- **Si abriste la cuenta con saldo existente**, ese saldo inicial es deuda que no estaba planeada en ningún mes de presupuesto. No se autofinancia. Asigna dinero manualmente a la categoría de pago para irla acabando.
- **Cuando cierres una tarjeta de crédito**, [cierra la cuenta](#cerrar-una-cuenta) (no la elimines). El historial de la categoría de pago sigue siendo útil.

---

## Editar, cerrar, reabrir, eliminar

### Editar una cuenta

Haz clic en la fila de la cuenta para abrir su editor. Puedes cambiar:

- El nombre
- El tipo
- (Para préstamos) la tasa de interés y el pago mensual
- (Para tarjetas de crédito) el **límite de crédito** — consulta [Tarjetas de crédito](#tarjetas-de-crédito) arriba

El saldo inicial se establece al crear. Para ajustar saldos históricos, edita o agrega una transacción directamente.

### Cerrar una cuenta

Cuando termines de usar una cuenta pero quieras conservar su historial:

1. Abre la vista de detalle de la cuenta.
2. Haz clic en **Cerrar**.

Las cuentas cerradas se ocultan de la lista principal y no aparecen en los selectores de transacción, pero todas las transacciones se conservan. Es la opción correcta para tarjetas de crédito liquidadas, inversiones vendidas y cuentas en bancos que ya no usas.

### Reabrir una cuenta

En la sección de cuentas cerradas de la página Cuentas, haz clic en **Reabrir**. Todo regresa exactamente como lo dejaste.

### Eliminar una cuenta

Solo puedes eliminar una cuenta de forma permanente si no tiene transacciones más allá del saldo inicial. Si necesitas eliminar una cuenta con actividad, tienes dos opciones:

1. Eliminar o reasignar cada transacción primero, o
2. Cerrar la cuenta — al cerrar se preserva el historial.

Cerrar es casi siempre lo que quieres. Eliminar es para cuando creaste una cuenta por error.

---

## Conciliación

La mayoría de las cuentas tienen un botón **Conciliar** que te lleva paso a paso a hacer coincidir savr con el extracto de tu banco. Es el movimiento que detecta errores de captura, transacciones perdidas y el ocasional cobro doble del banco.

Si el saldo de la cuenta en savr empieza a separarse de la realidad, corre una conciliación. Es la forma más limpia de ponerte al día.

> **Atención:** Las cuentas de préstamo no tienen botón Conciliar. Los prestamistas no emiten el tipo de extracto compensado/no compensado que asume el flujo de conciliación. Para un préstamo, lo correcto es mantener el saldo del capital al día con entradas precisas de [Pago de Deuda](../actividad/#pagos-de-deuda) y actualizar el saldo inicial una vez al año si el número del prestamista se aleja del tuyo.

→ Guía completa: [Conciliación](../reconcile/)

---

## Importación CSV

¿Tienes un año de transacciones en un CSV de tu banco? No las captures todas a mano. savr tiene un asistente de importación de tres pasos que maneja lo complicado (formatos de fecha, convenciones de signo, mapeo de columnas) por ti.

→ Guía completa: [Importar y Exportar](../import-export/)

---

## Organizar la página de cuentas

### Agrupación por tipo

Las cuentas se agrupan automáticamente por tipo. Cada grupo (Cuenta corriente, Ahorro, Tarjeta de Crédito, etc.) tiene un encabezado que muestra el saldo total del tipo — útil para "¿cuánto efectivo tengo en realidad ahora mismo?" de un vistazo.

### Colapsar y expandir

Haz clic en cualquier encabezado de grupo para colapsarlo. Úsalo para enfocarte en las cuentas con las que estás trabajando activamente. Los préstamos cerrados y las tarjetas que apenas tocas no necesitan saturar tu vista.

### Reordenar cuentas

savr permite arrastrar y soltar en dos niveles:

- **Dentro de un grupo** — arrastra cuentas individuales para cambiar su orden
- **Entre grupos** — arrastra el encabezado del grupo para cambiar el orden de los tipos

Tu orden se guarda automáticamente y persiste entre sesiones.

> **Por ejemplo:** Tienes tres cuentas corrientes y siempre piensas en "Chase Corriente" primero. Arrástrala al inicio del grupo Cuenta corriente. Ahora siempre es la primera al registrar una transacción.

---

## Vista de detalle de la cuenta

Haz clic en el nombre de una cuenta para abrir su página de detalle. Verás:

- El saldo actual y los metadatos de la cuenta (tipo, saldo inicial, fecha de creación)
- Todas las transacciones de esta cuenta, con los mismos filtros que la página principal de Transacciones
- Un botón **Nueva Transacción** para registrar actividad directamente
- Un botón **Conciliar** para coincidir con un extracto
- Una opción **Importar CSV** para agregar transacciones en bloque

Es la forma más rápida de conciliar contra un extracto físico o en línea, o de agregar varias transacciones de una sola cuenta seguidas.

---

## Saldos de cuenta explicados

Los saldos se almacenan con dos decimales de precisión. Cada vez que creas, actualizas o eliminas una transacción, el saldo de la cuenta afectada se recalcula de forma atómica — así que el número en la página de Cuentas siempre coincide con la suma de su actividad. Sin discrepancias, sin "déjame cerrar y reabrir la app para refrescar."

Las transferencias entre dos cuentas registran un par enlazado: un débito y un crédito. Ambas cuentas se actualizan juntas.

Para tarjetas de crédito, el saldo refleja lo que debes. Un saldo positivo significa que tienes un monto pendiente. Cuando registras un pago, transfiere dinero desde una cuenta corriente a la cuenta de tarjeta — el saldo de la tarjeta baja, el de cuenta corriente baja, y tu patrimonio neto general no cambia.

> **Escenario común:** Tu Chase Sapphire muestra un saldo de $843.21. La pagas transfiriendo $843.21 desde Cuenta corriente. Ahora la Sapphire muestra $0 y Cuenta corriente tiene $843.21 menos. La transferencia es una acción en savr, dos transacciones enlazadas, cero matemática de tu lado.
