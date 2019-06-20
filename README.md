# PRÁCTICA DE LABORATORIO 

**NOMBRE:** José Quinde

**CARRERA:** Computación	

**ASIGNATURA:** Programación Aplicada

**NRO. PRÁCTICA:**	08	

**TÍTULO PRÁCTICA:** Manejo de Archivos Binarios Randomicos

## OBJETIVO ALCANZADO:

Como objetivo Principal de esta práctica es poder implementar en un CRUD un archivo binario randomico para poder guardar la información permanentemente como una Base de Datos, sin necesidad de estar guardando los datos cada vez que se ingrese al programa.
Los archivos binarios pueden guardar datos de diferente tipo no solo String y por eso es ideal para poder implementarlo en un CRUD.

## ACTIVIDADES DESARROLLADAS
**1.Crear un repositorio en GitHub**

**Perfil:** JoseQ1996

**URL del proyecto:** https://github.com/JoseQ1996/ManejoArchivosBinariosRandomicos.git

-Se procedió a crear un repositorio con el nombre de Manejo Archivos Binarios Randomicos

 ![image](https://user-images.githubusercontent.com/49071271/59887763-3bd38a80-938a-11e9-9e0d-102b222b28aa.png)

**2. Sincronizar el repositorio creado con un proyecto en NetBeans. Realizar un commit y push por cada requerimiento de los puntos a continuación descritos (incluir un mensaje que identifique claramente los commits realizados a GitHub).**

-Se realizaron 6 commits en el proyecto

-Aquí se puede revisar los commits realizados y que hizo cada uno en específico.
 
![image](https://user-images.githubusercontent.com/49071271/59887781-51e14b00-938a-11e9-902c-d0d894ea534b.png)

**3. Crear clase en el paquete**

- Se proceido a crear 4 paquetes uno para los archivos, otro del controlador,la clase modelo y otro de la vista

 ![image](https://user-images.githubusercontent.com/49071271/59887803-67567500-938a-11e9-82a1-cb09dbeba071.png)

**4. Clase Persona**

La clase Persona tiene implementada excepciones, y los atributos que fueron declarados son los de los nombres, apellidos, cedula, edad, fecha de nacimiento, celular y Salario.

![image](https://user-images.githubusercontent.com/49071271/59887853-940a8c80-938a-11e9-9633-7aacf33a5284.png)
 
La clase también posee los constructores que son los siguientes.

![image](https://user-images.githubusercontent.com/49071271/59887857-9cfb5e00-938a-11e9-9162-557f3ecc17c1.png)

Primero se mostrará la excepción que se implementa al rato de Setear tanto los nombres como los apellidos,

Posee dos excepciones:

-No poder ingresar números.

-Se debe ingresar dos nombres.

![image](https://user-images.githubusercontent.com/49071271/59887864-a258a880-938a-11e9-8444-edec1a4fc62c.png)

Lo que hace primero es comparar si la cadena de texto posee un numero del 0 al 9, en caso de poseerlo saltar un error en el catch que debe ingresar solo letras y no números.

Si el String no posee ningún numero entrara al siguiente if en donde nos preguntara si el String posee un salto de texto, de poseerlo significara que posee dos nombres.

El mismo proceso se realiza para los Apellidos.

Ahora se mostrará la validación de la Cedula que manda a llamar a otra clase creada para validar que es la siguiente:

![image](https://user-images.githubusercontent.com/49071271/59887923-d502a100-938a-11e9-9bab-0a1f3fc163a1.png) 

Esta clase nos valida el ingreso de una cedula.

La cedula también tiene otra excepción aparte de la validación que es la de comprobar que se están ingresado 10 dígitos.

![image](https://user-images.githubusercontent.com/49071271/59887943-e9469e00-938a-11e9-9ffe-e3850799dc52.png) 

A través de un if nos compara el tamaño del String si es de 10 se ingresa caso contrario nos manda una excepción que se debe ingresar 10 dígitos.

El número de teléfono también posee un control de que se ingresen 10 dígitos.

![image](https://user-images.githubusercontent.com/49071271/59887964-fd8a9b00-938a-11e9-957d-928bc318757c.png)

Y así se muestra el toString de la clase Persona.
 
![image](https://user-images.githubusercontent.com/49071271/59887986-1430f200-938b-11e9-9a24-0cc5b62a0946.png)

**5. Controlador Persona**

El controlador de Persona es muy diferente al hecho anteriormente ya que este controlar nos ingresa, actualiza, elimina, busca y lista una persona de un Archivo Binario Randomico.

![image](https://user-images.githubusercontent.com/49071271/59888014-2f036680-938b-11e9-9940-26265a83fb9e.png)

Para poder ingresar una persona se pide un parámetro de la Persona, para que luego el archivo lo guarde con el write (), dependiendo el tipo de dato en el archivo, una persona debe contar con 152 bytes,

-Cédula (máximo 10 caracteres)

-Nombres (máximo 50 caracteres)

-Apellidos (máximo 50 caracteres)

-Edad (4 caracteres)

-Fecha de nacimiento en formato dd/mm/yyyy (máximo 10 caracteres)

-Número de celular (máximo 10 caracteres)

-Salario (8 caracteres).

Por lo que se ha hecho un control en los nombres y apellidos para que puedan rellenar con espacios los 50 caracteres.

![image](https://user-images.githubusercontent.com/49071271/59888030-4cd0cb80-938b-11e9-8b07-6eb25b6f082f.png)

Para poder leer una persona se pide que ingrese la posición del registro de la persona, para que se pueda leer a la persona a través del read (), y luego te devuelve una persona P para solo mostrarlo en pantalla.

![image](https://user-images.githubusercontent.com/49071271/59888044-61ad5f00-938b-11e9-9add-c79f04129b32.png)

Para el actualizar es la mezcla del Ingresar y el buscar ya que nos pide la posición y la persona que se va actualizar, a través del write (), va sobrescribiendo en el archivo dependiendo la posición de la persona escogida.

![image](https://user-images.githubusercontent.com/49071271/59888050-6b36c700-938b-11e9-8d31-9ea28f1164e2.png)

Para el eliminar te pide la posición de la persona y lo que hace es a través del write (), sobrescribir los 152 caracteres de esa persona con espacios en blanco.

![image](https://user-images.githubusercontent.com/49071271/59888053-6ffb7b00-938b-11e9-97f1-db4bbeb22184.png)

Finalmente, para listar lo que hace el programa es contar el total de bytes y dividirlo para 152 y ahí nos da el número de registros ingresados y a través de un bucle for nos va leyendo los 152 bytes de cada registro y luego los setea como persona para poder ingresarlos en un Set list.

![image](https://user-images.githubusercontent.com/49071271/59888061-7984e300-938b-11e9-8c4e-e2d061f784e0.png)

***NOTA:** Cabe recalcar que los métodos de Buscar, Actualizar, Eliminar y Listar tiene un if que nos controla para ver si el registro que se quiere obtener ya fue eliminado anteriormente.*

**6. Interfaz Grafica**

El programa cuenta con una Ventana Principal en donde nos permite llamar a cada Ventana para poder realizar el CRUD del programa
 
![image](https://user-images.githubusercontent.com/49071271/59888215-455df200-938c-11e9-9f66-741df529c981.png)

A continuación, se mostrará lo que realiza cada parte del CRUD.

-Ingresar Persona 

![image](https://user-images.githubusercontent.com/49071271/59888219-4abb3c80-938c-11e9-9d74-44f61c8f6a54.png)

Lo que hace el código principalmente es setear un Persona a través de los text field obteniendo el texto ingresado con el getText () , luego se verifica las excepciones de la persona con un try y catch y finalmente llama al controlador para poder ingresar la persona en el archivo, si cumple todas las excepciones el programa ingresara correctamente la persona en el archivo binario.

![image](https://user-images.githubusercontent.com/49071271/59888225-527ae100-938c-11e9-81f6-159e89b8760c.png)
![image](https://user-images.githubusercontent.com/49071271/59888228-5575d180-938c-11e9-817a-c62009ca013c.png)
  
La persona ingresara con diferente registro dependiendo cuantas personas estén ya en el archivo.

-Para el Buscar persona

![image](https://user-images.githubusercontent.com/49071271/59888268-85bd7000-938c-11e9-8b22-75069c4f5e8f.png)

Lo que hace el código es primero pedir la posición del registro, luego manda a llamar al controlador de buscar que nos devuelve una persona, para luego setear a la persona en los TextField, si la persona no existe nos saltara un cuadro diciendo que la persona no existe.
 
![image](https://user-images.githubusercontent.com/49071271/59888274-8fdf6e80-938c-11e9-9978-9eacc88d3717.png)

-Actualizar Persona

![image](https://user-images.githubusercontent.com/49071271/59888279-95d54f80-938c-11e9-83a6-e2ab34eaaf22.png)

Es una mezcla del buscar e ingresar persona, el botón de buscar hace exactamente lo mismo que el buscar Persona, solo que en este caso los text field están habilitados para modificar la información, y luego con el botón de actualizar y validar, nos ingresa una persona en el controlador de actualiza con su posición del registro para que sobrescriba en el archivo la persona actualizada.
 
![image](https://user-images.githubusercontent.com/49071271/59888286-9b329a00-938c-11e9-9270-26e90921f1a4.png)
![image](https://user-images.githubusercontent.com/49071271/59888288-9ff74e00-938c-11e9-9e3b-f04f6b44a2df.png)
 
-Eliminar Persona

![image](https://user-images.githubusercontent.com/49071271/59888318-bc938600-938c-11e9-8327-6d977a37c3e9.png)

Para el eliminar persona lo único que se debe ingresar es el registro o la posición de la persona a eliminar, luego se ingresa al controlador en donde sobrescribe esa persona con espacios en blanco, si la persona ya fue eliminada anteriormente nos dará un mensaje que esa persona ya no existe.

![image](https://user-images.githubusercontent.com/49071271/59888323-c0270d00-938c-11e9-80e2-8fdbd536273a.png)

-Listar Persona

Lo único que hace el listar persona en llenar la tabla con las personas que se obtiene en el controlador de persona, agregando las filas solo a las personas que existen.

![image](https://user-images.githubusercontent.com/49071271/59888328-c5845780-938c-11e9-9326-bacf46fa6fa4.png)
 
La interfaz seria así:

![image](https://user-images.githubusercontent.com/49071271/59888340-cae1a200-938c-11e9-8c9f-42b0b6128a61.png)

## RESULTADO(S) OBTENIDO(S):

Para el resultado obtenido se debe tener en cuenta que en el archivo ya existen 3 registros y el 2 ya fue eliminado 

![image](https://user-images.githubusercontent.com/49071271/59888340-cae1a200-938c-11e9-8c9f-42b0b6128a61.png)

Ahora se procederá a crear una persona

![image](https://user-images.githubusercontent.com/49071271/59888368-efd61500-938c-11e9-8375-afdba15d4358.png)

Nos ha mostrado el mensaje de persona creada, por lo que todos los datos fueron validos

![image](https://user-images.githubusercontent.com/49071271/59888372-f5cbf600-938c-11e9-9ebc-f10f0f6b8203.png)

Ahora procederemos a buscar esa persona que estaría en el registro 4.

![image](https://user-images.githubusercontent.com/49071271/59888373-fb294080-938c-11e9-8f4a-52b90e3c241f.png)

Procederemos a actualizar esa misma persona creada.
 
![image](https://user-images.githubusercontent.com/49071271/59888380-febcc780-938c-11e9-9ef7-f3ff02dbfc38.png)
![image](https://user-images.githubusercontent.com/49071271/59888383-05e3d580-938d-11e9-829f-81828b34fbe3.png)

Al momento de buscar podemos comparar que se ha modificado algunos datos.

Para el eliminar procedemos primero a listar las personas totales.

![image](https://user-images.githubusercontent.com/49071271/59888389-0c724d00-938d-11e9-95ff-180afca69bb0.png)

Ahora eliminaremos a la persona con el registro 3.

![image](https://user-images.githubusercontent.com/49071271/59888415-31ff5680-938d-11e9-8cff-d16e929bbea9.png)

Y luego listaremos nuevamente para ver si se eliminó la persona con el registro 3.

![image](https://user-images.githubusercontent.com/49071271/59888419-375ca100-938d-11e9-9c1e-ec4bcc1b4080.png)

Efectivamente se eliminó, así se podría demostrar el funcionamiento del programa

## CONCLUSIONES:
Utilizar un archivo binario como base de datos para un CRUD es mucho más factible ya que así nos permite guardar datos permanentemente sin importar si el programa se cierra.

El uso del controlador, de la interfaz y la clase también nos fue muy útil ya que así se pudo desarrollar una pequeña base de datos para el control de personas.

## RECOMENDACIONES:
Implementar la clase File para poder realizar el manejo de Archivos Binario Randomicos y también implementar el Controlador, Modelo y Vista aprendió anteriormente.
.
**Nombre de estudiante:** José Quinde

**Firma de estudiante:** 

![image](https://user-images.githubusercontent.com/49071271/59888423-3b88be80-938d-11e9-8ea0-ee085e383c51.png)


