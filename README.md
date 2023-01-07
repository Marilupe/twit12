# token_API_V1.1
Generate user credentials to access the Twitter API V1.1

## APIs de Twitter

Twitter ofrece desde el inicio de su creación un conjunto de **APIs** (**A**plication **P**rogramming **I**nterface) que permiten acceder mediante programas a sus datos. Con el tiempo han ido apareciendo nuevas APIs según las necesidades de acceso a la información, algunas gratis y otras de pago. También han ido evolucionando las versiones. Actualmente conviven la **V1.1** y la **V2**.

Las APIs gratuitas que se usan para descargar datos son la **API Standard**(V1.1) y la **API Académica**(V2). Para la primera no se requiere ningún permiso, pero para la segunda hay que solicitar el acceso y está reservada a investigadores académicos.

## Credenciales de acceso a la API Standard

A las APIs se accede mediante un protocolo OAuth (**O**pen **Auth**orization). Se trata de un protocolo para permitir la autorización de un servicio a otro sin compartir las credenciales de usuario reales, como un nombre de usuario y contraseña.

Para acceder a las APIs es necesario crear una **app** de la que se obtendrán las claves **consumer_key**, **consumer_secret** y **Bearer Token**. Con estas claves existen dos métodos de acceso:

-   **Modo aplicación**: Solo hay que usar la clave **Bearer Token**. Con esta opción solo se pueden hacer consultas para descargar tweets.
-   **Modo usuario**: Es necesario crear un token de usuario con las claves de la app **consumer_key** y **consumer_secret**. Cuando el usuario da permiso a la aplicación, se generarán las credenciales **access_token** y **access_secret**

Desde la creación de la **API V2** ya no es posible crear aplicaciones nuevas, por lo tanto hay que utilizar una app ya creada. Con este ejemplo se pone a disposición una app y un programa en python para crear un token con un usuario.

### Crear credenciales para modo usuario

Para obtener las credenciales que nos permitan trabajar en **Modo usuario** usaremos el script de **python make_token_Twitter.ipynb**. Este script se puede ejecutar en el [entorno colab de google](https://colab.research.google.com/).

![guia para crear credenciales](https://github.com/congosto/congosto.github.io/blob/master/crear_credenciales.jpg)

Seguiremos los siguientes pasos:

1.  Sustituiremos en la fila 10 el valor "xxxxxx" por el nombre de nuestro usuario en Twitter con el que vamos a acceder a la API
2.  Ejecutamos el script pulsando en el icono del play
3.  Si en unos segundos no aparece ninguna página web, pulsamos en el enlace que aparece en la fila inferior. Esto desplegará una ventana que nos solicitará permiso para la app. Cuando concedemos el permiso, nos proporcionará un PIN. Lo copiamos
4.  Pegaremos el PIN en la casilla situada en la zona inferior. Esto nos creará un fichero de claves
5.  Descargaremos el fichero de claves a nuestro disco local
