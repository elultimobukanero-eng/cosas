ESTO PARA LO DE LA PROFESIOENS EXCLUISDA
PASO 1 DE 10 – DATOS DEL SEGURO (ASEGURADO)
a. Se visualiza el formulario con los datos del asegurado.
b. Se completan los campos obligatorios:

Documento del asegurado

Profesión

Pregunta de invalidez

Importe de deuda (sin mínimo ni máximo; valor permitido ≥ 0 €)

Fecha de efecto

c. Reglas de negocio aplicables:

Profesiones excluidas: Ama de casa, Rentista, Estudiante, Desempleado.
Si se selecciona alguna → KO y no se permite continuar.

No existe validación de rango para el importe de deuda.

Si invalidez = Sí → la cobertura IPA no aparece en la oferta.

d. Se pulsa CONTINUAR.








ERROR ENANOS GORDOS
⚠️ KO técnico actual – Validación inexistente en peso/altura
El formulario permite introducir valores incoherentes o invertidos en los campos:

Peso (Kg)

Altura (cm)

Ejemplo: 180 kg / 80 cm.

Actualmente no existe ninguna validación que detecte estos errores.

Consecuencia:  
El sistema envía los valores al servicio médico de AEGON, que devuelve un error técnico prolongado (timeout o KO interno).
Este error no está controlado en el front, por lo que el gestor no recibe un mensaje claro y el flujo queda bloqueado.

Pendiente de implementación:  
Añadir validaciones de coherencia para evitar el envío de datos imposibles al servicio de AEGON.








ESTO PARA LO DE SI FUMAS O NO
Si la respuesta es NO:

El formulario no muestra ningún campo adicional.

Si la respuesta es SÍ:

Se despliega el campo obligatorio “¿Cuántos cigarrillos fumas al día?”

El gestor debe introducir un valor numérico (uds/día).

Este dato se envía al servicio médico de AEGON.






PREREQUISITIS
🟦 CASO 1 – SIN TELESELECCIÓN
Prerrequisitos del usuario
Edad del asegurado: 40 años

Número de cuentas: 1 cuenta
(porque es el caso más simple y no queremos bifurcaciones adicionales)

Capital: 80.000 €
→ ≤ 50 años + ≤ 150.000 € → Declaración de salud  
→ NO Teleselección

🟦 CASO 2 – CON TELESELECCIÓN
Prerrequisitos del usuario
Edad del asegurado: 45 años

Número de cuentas: 2 cuentas
(para que este caso tenga más riqueza funcional)

Capital: 200.000 €
→ ≤ 50 años + >150.000 € y ≤300.000 € → Teleselección

🟦 CASO 3 – CON TELESELECCIÓN + PRUEBAS MÉDICAS
Prerrequisitos del usuario
Edad del asegurado: 48 años

Número de cuentas: 1 cuenta
(para que el foco esté en TS+PM y no en la gestión de cuentas)

Capital: 350.000 €
→ ≤ 50 años + >300.000 € → Teleselección + Pruebas Médicas
