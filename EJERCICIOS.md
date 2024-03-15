###  Actividad CRUNCH - Construcción de Diccionarios.

1. Valide los primeros 8 ejemplos presentados en https://github.com/jaiderospina/CIBERSEGURIDAD_ETB/blob/main/ATAQUES_DICCIONARIO.md

2. Tome dos ejemplos del manual de crunch, valide su funcionalidad y explique cada paramétro del comando

3. Corriga el siguiente comando:

```
crunch 3 3 -t ,@@@^^
```
Suba a la carpeta CRUNCH del repositorio de tallares la evidencia de los puntos 2 y 3. 
No olvide subir la evidencia con el formato previamente acordado en el curso.

###  Actividad defensa - ataque "Por persuación - Cognitivo"

1.  Realizar el ejercicio eplicado en clase y explicado paso a paso en el link presentado a coninuación.
2.  Suba la evidencia en la carpeta Seguridad_Persuación del repositorio de talleres. Esta consiste en un print screen del banner con su nombre y apellidos e idnetificado con la nomenclatura establecida.

- https://www.youtube.com/watch?v=6szaEd7_ky4

### Taller: Uso de Crunch y Hydra en un Escenario de Ataque de Diccionario

#### Objetivo
El objetivo de este taller es proporcionar una comprensión práctica de cómo se pueden combinar herramientas como Crunch y Hydra para ejecutar un ataque de diccionario contra un servicio SSH. Este ejercicio está diseñado para fines educativos y éticos, con el fin de mejorar la comprensión y las habilidades en ciberseguridad. **No se debe utilizar esta información para actividades no éticas o ilegales.**

#### Escenario Hipotético
Imagina que eres un auditor de seguridad ética realizando una prueba de penetración autorizada para una empresa. Se te ha asignado la tarea de evaluar la fortaleza de las contraseñas utilizadas en el servicio SSH de un servidor que corre en el puerto 2245. Se sabe que el nombre de usuario es "kali". Se te ha pedido generar un diccionario de posibles contraseñas usando Crunch y luego utilizar este diccionario para intentar acceder al servicio SSH usando Hydra.

- Presentar un informe individual que recoga los siguientes aspectos y los comandos y print screen de la actidad realizada.
- Subir la evidencia en la carpeta "ATAQUE_DICCIONARIO" y seguir la metodología de presentación ya definida en nuestro curso. 

#### Pasos de Resolución

1. **Generación del Diccionario**: Inicia con la generación del diccionario usando Crunch. Determina los parámetros deseados para el diccionario basado en el escenario y las políticas de contraseña que creas que la empresa podría estar utilizando.

2. **Ejecución de Hydra**: Utiliza el diccionario generado para ejecutar un ataque de diccionario contra el servicio SSH de la máquina objetivo con Hydra. Ajusta los parámetros según sea necesario para coincidir con el entorno objetivo (p.ej., el puerto SSH).

3. **Análisis de Resultados**: Analiza la salida de Hydra para determinar si se ha logrado acceder con éxito utilizando alguna de las contraseñas del diccionario. Identifica la contraseña (si alguna) que permitió el acceso.

4. **Informe y Recomendaciones**: Redacta un informe detallando tu metodología, los resultados obtenidos, y ofrece recomendaciones para mejorar la seguridad del servicio SSH. Esto podría incluir el uso de contraseñas más fuertes, la implementación de autenticación de dos factores, o limitar los intentos de inicio de sesión fallidos.

#### Consideraciones Éticas y Legales
Es fundamental realizar este tipo de pruebas solo en entornos autorizados y con permiso explícito. La realización de ataques de fuerza bruta o de diccionario contra sistemas no autorizados es ilegal y éticamente reprobable. Este taller está diseñado con propósitos educativos y debe usarse como una herramienta para mejorar la seguridad y conciencia en el ámbito de la ciberseguridad.

### Ejercicio en Clase. Caso de estudio "Controles PCI"

Inspeccionar y reflecionar sobre el documento "Caso de Estudio_PCI.pdf", ubicado en https://drive.google.com/file/d/1-TX5W8yAdZbtS12jqpDzLokTqzaJOt88/view?usp=drive_link
