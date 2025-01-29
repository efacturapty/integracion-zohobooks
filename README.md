# Integración de ZohoBooks con Efacturapty

## Crear campos personalizados 

### Campos personalizados para los clientes

Debe crear los campos personalizados para los clientes: 
- RUC 
- DV

![image](https://github.com/efacturapty/integracion-zohobooks/assets/145995728/4331ee2f-322a-43b4-a816-dc73c4eda4a5)


### Campos personalizados de facturas (Invoices) y notas de crédito (Credit Notes)

Debe crear los siguientes campos personalizados para las facturas y las notas de crédito: 
- Fecha de autorización
- Protocolo de autorización
- CUFE

Todos los campos personalizados deben crearse con tipo de dato de TEXTO y contener los mismos nombres en las etiquetas, respetando las tildes en los nombres.

![image](https://github.com/efacturapty/integracion-zohobooks/assets/145995728/09996e35-4663-4b01-a6dc-02b4c4c1fed6)


![image](https://github.com/efacturapty/integracion-zohobooks/assets/145995728/ba7a3f20-d43e-40a2-8459-b0a6df5a8177)


### Botón personalizado para autorización y anulación de facturas y notas de crédito.

Para enviar la factura a ser autorizada, debe crear un botón personalizado, el cual debe contener los scripts correspondientes que están en este repositorio, tal como se ve en la siguiente imagen.

![image](https://github.com/efacturapty/integracion-zohobooks/assets/151682173/b4873ab7-9deb-4643-8ad4-7ca4c0ae8039)

Código disponible en https://github.com/efacturapty/integracion-zohobooks/blob/main/invoices-authorize.dg

![image](https://github.com/efacturapty/integracion-zohobooks/assets/151682173/3719d207-ffef-4ea0-a141-1a42fc19d0d6)

Código disponible en https://github.com/efacturapty/integracion-zohobooks/blob/main/invoices-void.dg

![image](https://github.com/efacturapty/integracion-zohobooks/assets/145995728/bf6df7a6-7283-4e12-ad85-bce092953d69)

Código disponible en https://github.com/efacturapty/integracion-zohobooks/blob/main/credit-notes-authorize.dg

![image](https://github.com/efacturapty/integracion-zohobooks/assets/151682173/3f6fff11-b8b1-4bd1-bccc-f57f2957f68f)

Código disponible en https://github.com/efacturapty/integracion-zohobooks/blob/main/credit-notes-void.dg

Debe reemplazar el APIKEY del script por uno generado en el apartado de integraciones con la cuenta correspondiente de efacturapty

![image](https://github.com/efacturapty/integracion-zohobooks/assets/145995728/e52dd382-52de-4ef9-8247-cf853a9a83b0)

### Habilitar integración de API de Zoho 

Para habilitar la integración entre ambas plataformas, ir al menú principal de ZohoBooks, ir a "Settings" y seleccionar "Developer Space". 

![image](https://github.com/efacturapty/integracion-zohobooks/assets/151682173/e7130e84-5fd8-496e-91f8-51cb783b9152)

Ahí, seleccionar el submenú "Connections". Dentro de este submenú, elegir "View My Connections", luego "System Connections".
Para que la comunicación entre eFacturapty y ZohoBooks se habilite se debe seleccionar “Zoho OAuth”.

![image](https://github.com/efacturapty/integracion-zohobooks/assets/151682173/b5ee938a-069b-47cc-822f-6fb961770bba)

![image](https://github.com/efacturapty/integracion-zohobooks/assets/151682173/7cc0c12d-967e-4edb-b54c-7948fe5cb644)

En el caso de habilitar el código de adjuntar PDF del Comprobante Auxiliar de Factura Electrónica (CAFE) a la factura o nota de crédito en Zoho Books, es necesario habilitar una seguna conexión. Para ello se ingresa a la sección de "Mis conexiones" o "My Connections" para crear dicha conexión.

<img width="1362" alt="My_Connections_ZohoBooks" src="https://github.com/user-attachments/assets/a471b46f-b998-4c11-974e-1de7baa70df1" />

Utilizano el botón para crear una nueva conexión, se puede buscar la conexión con Zoho Books con ayuda del campo de búsqueda, y seleccionar la conexión "Zoho Books".

<img width="1362" alt="ZohoBooks_NewConnection" src="https://github.com/user-attachments/assets/163434a4-2d87-4782-a530-34563f468d9f" />

Se asigna un nombre a la conexión, que será utilizado en el script, recomendamos utilizar "zbooks". Se debe deshabilitar la opción de utilizar credenciales del usuario que ingresó (Use credential of login User). Finalmente en la sección de autorización, utilizando la el campo de búsqueda marcar ZohoBooks.Invoices.All , a continuación, se muestran estos datos ingresados. 

<img width="1361" alt="ZohoBooks_ConnectionForm" src="https://github.com/user-attachments/assets/f80e7c0f-9b08-4266-a3c8-829af658a040" />

Finalmente, se presional botón "Create and connect", con lo cual se solicitarán confirmaciones para completar la conexión. Con ello estará listo para habilitar la sección del código para adjuntar el PDF del CAFE a sus facturas al momento de emitirlas.







