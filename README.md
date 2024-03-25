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
