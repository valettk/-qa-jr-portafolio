Semana 1 - Fundamentos


<h2> Reto 1.5 · Reportes de bug reproducibles en Jira </h2>

<h3> Reporte de bug 1</h3>
Título: [Transferencias] Una cuenta con monto en 0 puede hacer transferencias y su saldo se vuelve negativo. 
Ambiente: Url: https://parabank.parasoft.com/parabank/overview.html Navegador: Chrome. Version:  158.0.8127.36. Usuario: john. Contraseña: demo.
Precondiciones: Haber iniciado sesión y tener dos cuentas, la primera cuenta 18339 con $0 y la segunda cuenta 13344 con $5022.93.
Pasos para reproducir:
1. Ir a la sección Transfer Funds.
2. Seleccionar la cuenta 18339 con 0 de saldo para transferir.
3. Seleccionar la cuenta 13344 que recibirá el dinero.
4. Poner la cantidad 100 en la sección Amount.
5. Click en el botón "Transfer"
Datos usados: Usuario john y contraseña demo. Cuentas 18339 y 13344
Resultado esperado: Debería mostrar un mensaje diciendo que no se puede realizar la acción sin saldo en la cuenta.
Resultado obtenido: La transferencia se realiza y la cuenta 18339 termina con el saldo en negativo ($-100) y la 13344 en $5122.93.
Evidencias: Captura de Accounts Overview: cuenta 18339 en -$100.00 y cuenta 13344 en $5122.93.
Severidad / Prioridad sugeridas: Severidad: Alta. Prioridad: Alta.

<h3> Reporte de bug 2 </h3>
Título: [Transferencias] Pagina con el texto "Error!
An internal error has occurred and has been logged." al dar doble click en el botón "Transfer"
Ambiente: Url: https://parabank.parasoft.com/parabank/overview.html Navegador: Chrome. Version:  158.0.8127.36. Usuario: john. Contraseña: demo.
Precondiciones: haber iniciado sesión.
Pasos para reproducir: 
1. Ir a la sección Transfer Funds.
2. No seleccionar ninguna cuenta.
3. No poner ningun monto en la sección  Amount.
4. Dar doble click en el botón "Transfer"
Datos usados: Usuario john y contraseña demo. Ninguna cuenta usada.
Resultado esperado: La pagina debería mostrar un mensaje que indique que hace falta seleccionar las cuentas y especificar el monto a transferir.
Resultado obtenido: Una pagina con el mensaje "Error!
An internal error has occurred and has been logged."
Evidencias: Captura de Transfer Funds: Mensaje "Error!
An internal error has occurred and has been logged.".
Severidad / Prioridad sugeridas: Severidad: Baja. Prioridad: Baja.

<h3> Reporte de bug 3 </h3>
Título: [Transferencias] Al transferir un monto en negativo el saldo de la cuenta que lo recibió disminuye.
Ambiente: Url: https://parabank.parasoft.com/parabank/overview.html Navegador: Chrome. Version:  158.0.8127.36. Usuario: john. Contraseña: demo.
Precondiciones: Haber iniciado sesión y tener dos cuentas, la primera cuenta 12900 con $100 y la segunda cuenta 13011 con $100.
Pasos para reproducir: 
1. Ir a la sección Transfer Funds.
2. Seleccionar la cuenta 12900 para transferir.
3. Seleccionar la cuenta 13011 para recibir.
4. Escribir -10 en la sección Amount.
5. Click en el botón "Transfer".
Datos usados: Usuario john y contraseña demo. Cuentas 12900 y 13011.
Resultado esperado: Se debería mostrar un mensaje indicando que no se pueden hacer transferencias con montos negativos.
Resultado obtenido: La transferencia se realiza y el saldo de la cuenta que recibió la transferencia (13011) disminuye de $100 a $90 y la cuenta que transfirió (12900) aumento su saldo de $100 a $110.
Evidencias: Captura de Accounts Overview: cuenta 12900  en $110.00 y cuenta 13011 en $90.
Severidad / Prioridad sugeridas: Severidad: Alta. Prioridad: Alta.
