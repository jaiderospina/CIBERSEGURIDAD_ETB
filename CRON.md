# Manual de Uso de Cron en Kali Linux

Cron es un administrador de procesos en segundo plano que ejecuta tareas a intervalos regulares de tiempo. Estas tareas son comúnmente conocidas como "cron jobs". En Kali Linux, puedes configurar cron jobs para automatizar diversas tareas.

## Editar la Tabla de Cron

Para editar la tabla de cron, que contiene tus cron jobs, utiliza el siguiente comando:

```bash
crontab -e
```

Si es la primera vez que usas `crontab`, puede que te pida seleccionar un editor. `nano` es una opción común para principiantes por su facilidad de uso.

## Estructura de un Cron Job

Cada línea en la tabla de cron tiene la siguiente estructura:

```
* * * * *  command_to_execute
- - - - -
| | | | |
| | | | +---- Día de la semana (0 - 7) [Domingo = 0 o 7]
| | | +------ Mes (1 - 12)
| | +-------- Día del mes (1 - 31)
| +---------- Hora (0 - 23)
+------------ Minuto (0 - 59)
```



Los primeros cinco campos (fecha y hora) también aceptan los siguientes parámetros:

- *– El asterisco significa todos los valores permitidos. Si tiene el símbolo de asterisco en el campo Minuto, significa que la tarea se realizará cada minuto.
- -– El guion le permite especificar un rango de valores. Si lo establece 1-5 en el campo Día de la semana, la tarea se ejecutará todos los días de la semana (de lunes a viernes). El rango es inclusivo, lo que significa que el primer y último valor se incluyen en el rango.
- ,– La coma le permite definir una lista de valores para su repetición. Por ejemplo, si tiene 1,3,5 en el campo Hora, la tarea se ejecutará a la 1 am, 3 am y 5 am. La lista puede contener valores y rangos únicos, 1-5,7,8,10-15
- /– La barra inclinada le permite especificar valores de paso que se pueden usar junto con rangos. Por ejemplo, si lo tiene 1-10/2 en el campo Minutos, significa que la acción se realizará cada dos minutos en el rango 1-10, igual que se especifica 1,3,5,7,9. En lugar de un rango de valores, también puede utilizar el operador de asterisco. Para especificar que un trabajo se ejecute cada 20 minutos, puede utilizar «* / 20«.

La sintaxis de los archivos crontab de todo el sistema es ligeramente diferente a la de los crontabs del usuario. Contiene un campo de usuario obligatorio adicional que especifica qué usuario ejecutará el trabajo cron.


```
* * * * * <username> command(s)
```
          
## Ejemplos de Cron Jobs

Aquí tienes algunos ejemplos de cron jobs:

### Ejecutar un Script Cada Día a Medianoche

```bash
0 0 * * * /ruta/a/mi_script.sh
```

### Ejecutar una Tarea Cada Hora

```bash
0 * * * * /ruta/a/mi_tarea
```

### Ejecutar una Tarea Cada Lunes a las 5 PM

```bash
0 17 * * 1 /ruta/a/mi_tarea
```

### Ejecutar una Tarea Cada 15 Minutos

```bash
*/15 * * * * /ruta/a/mi_tarea
```

### Enviar el Contenido de un Directorio por Correo Electrónico Todos los Días

```bash
0 0 * * * ls /algun/directorio | mail -s "Contenido del Directorio" mi_correo@dominio.com
```

Recuerda reemplazar `/ruta/a/mi_script.sh`, `/ruta/a/mi_tarea` y `mi_correo@dominio.com` con la ruta del script que quieres ejecutar y tu dirección de correo electrónico respectivamente.

## Listar los Cron Jobs

Para ver la lista de cron jobs configurados para el usuario actual, usa:

```bash
crontab -l
```

## Eliminar la Tabla de Cron

Para eliminar todos los cron jobs para el usuario actual, usa:

```bash
crontab -r
```

## Notas Finales

# ComandoS crontab

- -e para editar el archivo crontab actual.
- -l para obtener una lista de las tareas del archivo crontab actual.
- -r para eliminar de forma permanente el archivo crontab actual.
- -u <usuario> <opción> para ejecutar una opción en el archivo crontab de otro usuario.


- Asegúrate de que el script o comando que planeas ejecutar con cron tiene los permisos adecuados.
- Es una buena práctica redirigir la salida de los comandos a un archivo de registro para su revisión.

  ## ACTIVIDAD.

  1. Programe un cron job  para crear una carpeta cada 30 minutos
  2. Cree una tarea que 5 minutos de programada se ejecute y cambie los permisos de una carpeta existente que se llama Ejercicio2 y se encuentra en la ruta /home/kali/12


