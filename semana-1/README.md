Semana 1 - Fundamentos


<h2> Reto 1.5 · Reportes de bug reproducibles en Jira </h2>

<h3> Reporte de bug 1</h3>
Título: [Transferencias] Una cuenta con monto en 0 puede hacer transferencias y su saldo se vuelve negativo. <br>
Ambiente: Url: https://parabank.parasoft.com/parabank/overview.html Navegador: Chrome. Version:  158.0.8127.36. Usuario: john. Contraseña: demo. <br>
Precondiciones: Haber iniciado sesión y tener dos cuentas, la primera cuenta 18339 con $0 y la segunda cuenta 13344 con $5022.93. <br>
Pasos para reproducir: <br>
1. Ir a la sección Transfer Funds. <br>
2. Seleccionar la cuenta 18339 con 0 de saldo para transferir. <br>
3. Seleccionar la cuenta 13344 que recibirá el dinero. <br>
4. Poner la cantidad 100 en la sección Amount. <br>
5. Click en el botón "Transfer" <br>
Datos usados: Usuario john y contraseña demo. Cuentas 18339 y 13344. <br>
Resultado esperado: Debería mostrar un mensaje diciendo que no se puede realizar la acción sin saldo en la cuenta. <br>
Resultado obtenido: La transferencia se realiza y la cuenta 18339 termina con el saldo en negativo ($-100) y la 13344 en $5122.93. <br>
Evidencias: Captura de Accounts Overview: cuenta 18339 en -$100.00 y cuenta 13344 en $5122.93. <br>
<img width="509" height="204" alt="Captura de pantalla 2026-11-23 121401" src="https://github.com/user-attachments/assets/aed5a7b8-d275-46de-9ad4-443a4c3ff9ad" /> <br>
Severidad / Prioridad sugeridas: Severidad: Alta. Prioridad: Alta. <br>

<h3> Reporte de bug 2 </h3>
Título: [Transferencias] Pagina con el texto "Error!
An internal error has occurred and has been logged." al dar doble click en el botón "Transfer" <br>
Ambiente: Url: https://parabank.parasoft.com/parabank/overview.html Navegador: Chrome. Version:  158.0.8127.36. Usuario: john. Contraseña: demo. <br>
Precondiciones: haber iniciado sesión. <br>
Pasos para reproducir: <br>
1. Ir a la sección Transfer Funds. <br>
2. No seleccionar ninguna cuenta. <br>
3. No poner ningun monto en la sección  Amount. <br>
4. Dar doble click en el botón "Transfer" <br>
Datos usados: Usuario john y contraseña demo. Ninguna cuenta usada. <br>
Resultado esperado: La pagina debería mostrar un mensaje que indique que hace falta seleccionar las cuentas y especificar el monto a transferir. <br>
Resultado obtenido: Una pagina con el mensaje "Error!
An internal error has occurred and has been logged." <br>
Evidencias: Captura de Transfer Funds: Mensaje "Error!
An internal error has occurred and has been logged.". <br>
<img width="509" height="204" alt="Captura de pantalla 2026-11-23 121401" src="https://github.com/user-attachments/assets/aed5a7b8-d275-46de-9ad4-443a4c3ff9ad" /> <br>
Severidad / Prioridad sugeridas: Severidad: Baja. Prioridad: Baja. <br>

<h3> Reporte de bug 3 </h3>
Título: [Transferencias] Al transferir un monto en negativo el saldo de la cuenta que lo recibió disminuye. <br>
Ambiente: Url: https://parabank.parasoft.com/parabank/overview.html Navegador: Chrome. Version:  158.0.8127.36. Usuario: john. Contraseña: demo. <br>
Precondiciones: Haber iniciado sesión y tener dos cuentas, la primera cuenta 12900 con $100 y la segunda cuenta 13011 con $100. <br>
Pasos para reproducir: <br>
1. Ir a la sección Transfer Funds. <br>
2. Seleccionar la cuenta 12900 para transferir. <br>
3. Seleccionar la cuenta 13011 para recibir. <br>
4. Escribir -10 en la sección Amount. <br>
5. Click en el botón "Transfer". <br>
Datos usados: Usuario john y contraseña demo. Cuentas 12900 y 13011. <br>
Resultado esperado: Se debería mostrar un mensaje indicando que no se pueden hacer transferencias con montos negativos. <br>
Resultado obtenido: La transferencia se realiza y el saldo de la cuenta que recibió la transferencia (13011) disminuye de $100 a $90 y la cuenta que transfirió (12900) aumento su saldo de $100 a $110. <br>
Evidencias: Captura de Accounts Overview: cuenta 12900  en $110.00 y cuenta 13011 en $90. <br>
<img width="509" height="204" alt="Captura de pantalla 2026-11-23 121401" src="https://github.com/user-attachments/assets/aed5a7b8-d275-46de-9ad4-443a4c3ff9ad" /> <br>
Severidad / Prioridad sugeridas: Severidad: Alta. Prioridad: Alta. <br>

