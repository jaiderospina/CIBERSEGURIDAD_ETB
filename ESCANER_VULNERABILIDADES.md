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
Sigue las recomendaciones proporcionadas por Lynis para mejorar la seguridad de tu sistema.

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


###  Revisa los resultados y exámina los resultados.

a. ¿Investiga sobre algunas  del las advertencias?

¿Cuántas sugerencias existen?

b. Desplázate hasta las sugerencias y seleccione ters. Investiga las sugerencias para resolver el problema.

Documenta las investigación realizada detallando la vulnerabilidad, su impacto y 

### 4. Documentación Adicional
Si deseas profundizar más, puedes consultar la [documentación oficial de Lynis](https://github.com/CISOfy/lynis).

Recuerda que Lynis es una herramienta poderosa para mejorar la seguridad de tus servidores. 🛡️

https://github.com/CISOfy/lynis.
