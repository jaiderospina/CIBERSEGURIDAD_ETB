# Laboratorio Hardening ETB 2024

En grupos de dos a cuatro integrantes (se recomienda mínimo un integrante con experticia en cada uno de ellos), realizar el siguiente laboratorio. 

NOTA: 

Teniendo en consideración que nuestro curso es para un público experto; sumado al hecho de que toda formación técnica implica conocimiento y competencias profesionales de investigación, se presenta retos que potencialice las competencias profesionales individuales.   


## Uso de Lynis para Hardening de Servidores

### 1. Instalación de Lynis
Para comenzar, sigue estos pasos para instalar Lynis:

1. **Clona o descarga los archivos del proyecto** desde el repositorio oficial de Lynis en GitHub:
   ```
   #git clone https://github.com/CISOfy/lynis
   ```

2. **Accede al directorio de Lynis**:
   ```
   #cd lynis
   ```

### 2. Ejecución de la Auditoría
Una vez instalado, puedes ejecutar una auditoría de seguridad en tu servidor o equipo de uso particular:

1. **Inicia la auditoría** con el siguiente comando:
   ```
   #./lynis audit system
   ```

2. **Verifica los reportes generados**:
   - Para ver información de depuración y pruebas:
     ```
     cat /var/log/lynis.log
     ```
   - Para acceder a los datos del informe:
     ```
     cat /var/log/lynis-report.dat
     ```
Interpretación de los Resultados

Lynis mostrará una lista de sugerencias y advertencias sobre posibles problemas de seguridad en tu sistema. Aquí hay algunas pautas para interpretar los resultados:

[+]: Indica una sugerencia.

[-]: Indica una advertencia.

[?]: Indica una nota o sugerencia de mejora.


###  Algunos comandos de interés.

 - Ver la versión instalada.

    ```
    ./lynis show version
    ```
 - MODO DE ESCANEO SIN PRIVILEGIOS, algunas pruebas no se ejecutarán ya que requieren permiso de root.
   
    ```
    ./lynis audit system -Q
    ```
 - Resumen de principales comandos. 
   
    ```
    ./lynis show commands
    ```

### 3. Parámetros Útiles
Aquí algunos parámetros comunes que puedes utilizar al ejecutar Lynis:

- `--checkall` (`-c`): Inicia la auditoría completa.
- `--help` (`-h`): Muestra los parámetros válidos.
- `--quick` (`-Q`): No espera entrada del usuario, excepto en caso de errores.
- `--version` (`-V`): Verifica la versión de Lynis.
- `--auditor "Nombre"`: Asigna un nombre de auditor al informe.
- `--check-update`: Verifica si Lynis está actualizado.
- `--cronjob`: Ejecuta Lynis como una tarea programada (incluye `-c -Q`).
- `--manpage`: Muestra el manual de Lynis.
- `--nocolors`: Desactiva los colores en la salida.
- `--pentest`: Realiza un escaneo de prueba de penetración (sin privilegios).
- `--quiet`: Muestra solo advertencias (incluye `--quick`, pero no espera).
- `--reverse-colors`: Utiliza un esquema de colores diferente para fondos claros.


###  4. Revisa los resultados y exámina los resultados.

a. ¿Investiga sobre algunas  del las advertencias?

¿Cuántas sugerencias existen?

b. Desplázate hasta las sugerencias y seleccione ters. Investiga las sugerencias para resolver el problema.

Documenta las investigación realizada detallando la vulnerabilidad, su impacto y 

###  5. Reto

Averigua sobre la automatización de tareas mediante cron y automatiza la labor para ejecutar lynis una vez a la semana.
    
   Fuentes:
   -  https://www.godaddy.com/resources/es/recursos/cron-que-es
   -  https://www.hostinger.co/tutoriales/cron-job

### 4. Documentación Adicional
Si deseas profundizar más, puedes consultar la [documentación oficial de Lynis](https://github.com/CISOfy/lynis).

Recuerda que Lynis es una herramienta poderosa para mejorar la seguridad de tus servidores. 🛡️

https://github.com/CISOfy/lynis.
https://es.linux-console.net/?p=3332
