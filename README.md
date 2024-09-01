OBJETIVO DEL PRGRAMA:

  Este código genera contraseñas seguras y permite al usuario elegir la longitud de la contraseña y decidir si desea una nueva o si está satisfecho con la generada. A continuación te explico su funcionamiento paso a paso:
  
INTRODUCCIÓN AL PROYECTO

1.Importación de módulos:

  import secrets
  import string

  secrets: Se usa para generar datos criptográficamente seguros, como contraseñas. La función secrets.choice() se usa para elegir un elemento aleatorio de una secuencia.
  string: Contiene constantes relacionadas con cadenas, como ascii_letters, digits, y punctuation.

2.Definición de la función generar_contraseña:

  def generar_contraseña(longitud):
  Esta función genera una contraseña de una longitud específica (longitud) utilizando caracteres al azar de un conjunto definido de caracteres.

3.Conjunto de caracteres permitidos:

  caracteres = string.ascii_letters + string.digits + string.punctuation
  string.ascii_letters:  Letras mayúsculas y minúsculas (abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ).
  string.digits: Dígitos (0123456789).
  string.punctuation: Caracteres de puntuación (!"#$%&'()*+,-./:;<=>?@[\]^_{|}~`).

4.Generación de la contraseña:

  contraseña = ''.join(secrets.choice(caracteres) for _ in range(longitud))
  Usa secrets.choice(caracteres) para seleccionar un carácter al azar del conjunto caracteres, repitiendo el proceso longitud veces.
  ''.join(...): Une los caracteres seleccionados en una única cadena para formar la contraseña.

5.Bloque principal del programa:

  Primero, muestra un banner ASCII del nombre de la aplicación.
  Luego, solicita al usuario que introduzca la longitud deseada para la contraseña, verificando que sea un número positivo. Si el usuario introduce un valor no válido, muestra un mensaje de error y vuelve a solicitar la entrada.
  Una vez que se introduce una longitud válida, genera una contraseña segura utilizando la función generar_contraseña.

6.Interacción con el usuario:

  Después de generar la contraseña, el programa le pregunta al usuario si está satisfecho con ella (y/n).
  Si el usuario responde con 'y', el programa finaliza con un mensaje de agradecimiento.
  Si responde con 'n', genera una nueva contraseña.
  Si la entrada no es válida (ni 'y' ni 'n'), muestra un mensaje de error y vuelve a intentar.

7.Finalización del programa:

  El programa sigue solicitando al usuario hasta que esté satisfecho con la contraseña generada y se cierra automáticamente cuando el usuario está contento con la contraseña generada.

FECHA 01/09/2024

