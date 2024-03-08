# Conexión a Kali Linux desde Windows usando X11 


## Teoría del Procedimiento

La conexión X11 es un protocolo que permite ejecutar aplicaciones gráficas remotas en un sistema X Window local. En este caso, estamos utilizando SSH para cifrar la conexión entre Windows y Kali Linux, y X11 forwarding para reenviar las aplicaciones gráficas desde Kali Linux a través de SSH hacia el servidor Xming en Windows.

El servidor Xming interpreta estas aplicaciones gráficas y las muestra en el escritorio de Windows. Este proceso proporciona una forma segura y conveniente de ejecutar aplicaciones gráficas de Linux en un entorno Windows, lo que es especialmente útil para administradores de sistemas y desarrolladores que necesitan acceder a herramientas específicas de Linux desde una máquina Windows.

## Procdimiento.

## Habilitar el Servicio SSH en Kali Linux

1. **Instalar SSH Server**: Si no tienes el servidor SSH instalado en Kali Linux, puedes hacerlo ejecutando el siguiente comando en la terminal:
   ```
   sudo apt update
   sudo apt upgrade
   sudo apt install openssh-server
   ```

2. **Iniciar el Servicio SSH**: Asegúrate de que el servicio SSH esté en funcionamiento ejecutando:
   ```
   sudo systemctl start ssh 
   sudo systemctl enable ssh
   ```
NOTA_1:

Para validar el estado del servicio ingresa:

   ```
   sudo systemctl status ssh 
   ```
NOTA_2:

Archivo de configuración ssh  -->  

   ```
   #cd /etc/ssh
   #vi sshd_config
   ```




3. **Configurar el servicio**: Abre el archivo de configuración SSH:

 ```
nano /etc/ssh/sshd_config
 ```
Asegurarte  que se encuentre habilitado el X11 forwarding. Para ello debe encontrarse seteado la variable en el archivo de configuración del servidor ssh (sshd_config)

 ```
 X11Forwarding yes
 ```


4. **Configurar el Firewall (opcional)**: Si estás utilizando un firewall, asegúrate de permitir conexiones entrantes al puerto SSH (por defecto, el puerto 22).

## Instalación de Xming en Windows

Xming es un servidor X Window System para Windows que te permitirá mostrar las aplicaciones gráficas de Kali Linux en tu escritorio de Windows.

1. **Descargar Xming**: Visita el sitio web oficial de [Xming](https://sourceforge.net/projects/xming/) y descarga la última versión estable.

2. **Instalar Xming**: Una vez descargado, ejecuta el instalador de Xming y sigue las instrucciones en pantalla. Durante la instalación, asegúrate de seleccionar todas las opciones relevantes, como la integración con el menú contextual de Windows y la creación de un acceso directo en el escritorio.

## Instalar Putty 

Abre PuTTY en Windows.
Ingresa la dirección IP o el nombre de host de tu máquina Kali Linux.
En la sección Connection > SSH > X11, marca la casilla Enable X11 forwarding.
Inicia la conexión SSH.

![ Putty X11.](https://github.com/jaiderospina/CIBERSEGURIDAD_ETB/blob/main/images/REPOS/X11_PUTTY.png)


![ Putty X11.](https://github.com/jaiderospina/CIBERSEGURIDAD_ETB/blob/main/images/REPOS/X11_PUTTY_Conexion%20(Phone).png)


## Conectar a Kali Linux desde Windows y Abrir Nautilus

1. **Iniciar Xming**: Después de instalar Xming, inicia el programa desde el acceso directo en el escritorio o desde el menú de inicio de Windows.

2. **Conectar a Kali Linux**: Abre tu cliente SSH favorito en Windows (como PuTTY) y conecta a la dirección IP de tu Kali Linux. Asegúrate de habilitar X11 forwarding en la configuración de conexión SSH.

4. **Abrir Nautilus**: Ahora, puedes abrir Nautilus (o cualquier otra aplicación gráfica) desde la línea de comandos de Kali Linux. Simplemente escribe:
   
   ```
   $xeyes
   ```


### NOTA:

Guía paso a paso de instalación de Xming y Putty 

https://www.csusb.edu/sites/default/files/SSH%20X11%20Forwarding%20on%20Windows%20with%20Putty.pdf
