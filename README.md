# LOGIN
En este repositorio se encuentra el código fuente y la documentación de cómo realizar mantenimiento de la página de LOGIN. A continuación se muestran detalles del uso de la aplicación y el funcionamiento del código.

## CÓMO FUNCIONA

La página de ingreso a tiene como finalidad mapear la frecuencia y el motivo principal de la visita de los usuarios a la Biblioteca Digital de Instructores. Es un complemento de la información estadística que se obtiene mediante el uso de Google Analytics. El último en mención, nos permite recopilar información genérica sobre cuáles son las páginas más visitadas dentro del Site y los dispositivos desde los que acceden los usuarios. Debido a que una de las necesidades mencionadas por el Gerente del área de Desarrollo Técnico es la de poder conocer la información de ambos medios, se justifica la creación de una implementación de App Scripts de Google Workspace que permita que los visitantes se registren antes de ingresar al Site. Esto se basa en las limitaciones de Google Sites como página extensible de Google Drive, la que por su naturaleza gratuita, no permite añadir Tags de mapeo en el código fuente pues este es inaccesible. 

### PÁGINA DE INGRESO

El acceso a la Web App para ingreso a la Biblioteca Digital se realiza mediante el siguiente [enlace](https://script.google.com/a/macros/ferreyros.com.pe/s/AKfycbzzB0Akz0v8WNORsDdRPF8o9t50v6aDsrdb4jZTwRGPBACiW68B2KZ2AXbBpxsGc2uv/exec). Esta Web App tiene como base de datos al archivo de Google Spreadsheets al que se puede acceder mediante el siguiente [enlace](https://docs.google.com/spreadsheets/d/1Ufc0bTdm7j9-vZc0Ld9iqHZYSSDq_MEn9WbFj7AzSCo/edit#gid=0).
Cuando el usuario ingrese y otorgue todos loe permisos necesarioa a la Web App observará la siguiente interface:

![image](https://github.com/DISENOINSTRUCCIONALFSAA/LOGIN/assets/144281326/d207a78b-791c-472a-ae18-76721fb62176)

El llenado de todos los campos es obligatorio. Es preciso mencionar que la información que se recolecta como parte del acceso del usuario a la Web App es la hora en la que ingresó y su correo electrónico. No se almacenan datos mediante cookies para salvaguardar la privacidad de los datos personales del usuario. Si se desea conocer a detalle la información y cómo se almacena, debe ingresar al link del párrafo anterior que lo dirige al archivo de Google Spreadsheets que se encuentra en el siguiente [enlace](https://docs.google.com/spreadsheets/d/1Ufc0bTdm7j9-vZc0Ld9iqHZYSSDq_MEn9WbFj7AzSCo/edit#gid=0). 

Luego de ingresar, el usuario debe bucar su nombre en el primer desplegable, y el principal motivo de su visita en el segundo desplegable. Finalmente debe marcar la casilla de verificación en la que acepta que conoce que la información contenida en la página a la que ingresará es confidencial y que su uso se hace bajo los lineamientos del Procedimiento de uso de la   Biblioteca Digital de Instructores, donde se detalla el nivel de confidencialidad de la información contenida.

Si es que intenta ingresar sin haber completado los campos de los desplegables y sin haber marcado el casillero de verificación, el usuario visualizará una advertencia flotante en los campos que ha omitido, lo cual se muestra a continuación:

![image](https://github.com/DISENOINSTRUCCIONALFSAA/LOGIN/assets/144281326/1f71cbed-451d-42e5-a581-9da88576a40c)

Cuando el registro sea exitoso, en cambio, será redirigido a la página principal del site de la Biblioteca Digital de Instructores y se mostrará el siguiente mensaje en la Web App para que cierre la pestaña:

![image](https://github.com/DISENOINSTRUCCIONALFSAA/LOGIN/assets/144281326/99a9360c-2e8a-435b-a397-37ee0e951149)


### ACERCA DEL CÓDIGO

Se cuenta con dos archivos para el funcionamiento de esta implementación. Son los archivos Code.gs e Index.html. Se muestra a continuación donde se ubican dentro del Editor de Secuencias de Comandos del archivo de Google Spreadsheets que se usa como base de datos y a la que se puede acceder mediante el siguiente [enlace](https://docs.google.com/spreadsheets/d/1Ufc0bTdm7j9-vZc0Ld9iqHZYSSDq_MEn9WbFj7AzSCo/edit#gid=0).

![image](https://github.com/DISENOINSTRUCCIONALFSAA/LOGIN/assets/144281326/27ba3210-c414-4541-90db-b5922ddeea1a)

Para poder agregar funcionalidades relacionadas a acciones dentro del Google Spreadsheets, como por ejemplo, adicionar nuevos campos dentro de la hoja, quitar esos campos, o nuevas funcionalidades de edición de filas y columnas, se debe realizar en el archivo Code.gs desde lo que comprende desde la línea 1 del archivo:

![image](https://github.com/DISENOINSTRUCCIONALFSAA/LOGIN/assets/144281326/7258337f-e1da-44c5-a383-93e7e974ce2c)

y también la sección de <script> en el archivo Index.html, que contiene los comandos de JavaScript para la WebApp, lo que comprende desde la línea 102 hasta la línea 129.

![image](https://github.com/DISENOINSTRUCCIONALFSAA/LOGIN/assets/144281326/0f2d51f7-c0d6-4f21-be8d-4b8212d47a7d)

Por otro lado, si es que se desea modificar el diseño o el formato de la Web App, se pueden cambiar las secciones de CSS y HTML del archivo de Index.html, que se encuntran en las líneas que no contienen la sección de <script> mencionada anteriormente. Ambas secciones se encuentran codificadas en <head> y <body> como se muestra a continuación:

![image](https://github.com/DISENOINSTRUCCIONALFSAA/LOGIN/assets/144281326/f27f19ef-427f-4275-b601-8caced304e9f)

![image](https://github.com/DISENOINSTRUCCIONALFSAA/LOGIN/assets/144281326/44c36fdf-77e7-4809-865b-1ba0f15c86a2)

Finalmente, se hace mención a los diferentes <em>source</em> que se usan para poder mejorar la presentación y garantizar el funcionamiento de la Web App. Estos se encuentran en la parte superior e inferior del código. El <em>source</em> de Bootstrap que se usa para el diseño, se incluye mendiante el uso de <link> y al final mediante <script src>; mientras que ajax para JavaScript se encuentra referenciado al final mediante <script src>.

![image](https://github.com/DISENOINSTRUCCIONALFSAA/LOGIN/assets/144281326/7525f7ab-735d-4ccd-a523-1938b209e422)

![image](https://github.com/DISENOINSTRUCCIONALFSAA/LOGIN/assets/144281326/e698e193-140a-4cd1-8d71-a25805128264)





