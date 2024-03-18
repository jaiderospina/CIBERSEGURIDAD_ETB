### Esteganografia

La esteganografía es la práctica de ocultar información dentro de un medio de comunicación, de manera que prevenga la detección de la información oculta. Se diferencia de la criptografía, que oculta el contenido del mensaje, ya que la esteganografía oculta la existencia misma del mensaje. Las técnicas de esteganografía pueden aplicarse a imágenes, videos, audio y textos, entre otros. A continuación, se describen algunas de las principales técnicas utilizadas en la esteganografía:

### 1. **Técnicas de Esteganografía en Imágenes:**

- **Sustitución de bits menos significativos (LSB):** Esta técnica consiste en modificar los bits menos significativos de los píxeles en una imagen para incrustar la información. Dado que los cambios son mínimos, son casi imperceptibles al ojo humano.
  
- **Transformada de dominio:** Utiliza métodos matemáticos para modificar ciertos aspectos de una imagen, como la Transformada Discreta de Fourier (DFT) o la Transformada Discreta del Coseno (DCT), para ocultar información. Es comúnmente utilizada en formatos de compresión como JPEG.

- **Máscaras y filtros:** Se aplican sobre la imagen original alterando ciertos aspectos visuales para ocultar la información, de manera que solo pueda ser recuperada a través del uso de la máscara o filtro correcto.

### 2. **Técnicas de Esteganografía en Audio:**

- **Codificación Eco:** Introduce un eco muy sutil en la señal de audio. La presencia o ausencia de este eco en segmentos específicos puede utilizarse para codificar datos.

- **Sustitución de LSB en audio:** Similar a la técnica utilizada en imágenes, esta técnica cambia los bits menos significativos en un archivo de audio para incrustar información sin alterar perceptiblemente la calidad del sonido.

- **Modulación de Frecuencia Espectral (SSM):** Altera ciertas frecuencias dentro de la señal de audio para incrustar información.

### 3. **Técnicas de Esteganografía en Texto:**

- **Formato de texto:** Cambia aspectos del formato del texto, como espacios, tamaño de fuente o color, para representar los datos ocultos.

- **Marcado lingüístico:** Utiliza peculiaridades lingüísticas o patrones gramaticales para ocultar información dentro del texto.

- **Canal Cero Ancho:** Inserta caracteres de espacio o puntuación de cero ancho que no son visibles pero pueden ser interpretados para extraer información oculta.

### 4. **Técnicas de Esteganografía en Video:**

- **Inserción en fotogramas:** Similar a la esteganografía en imágenes, pero aplicada a los fotogramas individuales de un vídeo.

- **Modificación del tiempo de aparición de los fotogramas:** Altera ligeramente el tiempo de aparición de ciertos fotogramas para codificar información.

### 5. **Técnicas de Redes:**

- **Protocolo y metadatos:** Oculta información en cabeceras de protocolos de red, paquetes o metadatos, donde los datos pueden ser encubiertos dentro del tráfico de red normal.

Cada una de estas técnicas tiene sus ventajas y limitaciones en términos de capacidad de datos, detectabilidad y robustez frente a la compresión o transformaciones. La elección de la técnica depende del medio de comunicación y de los requisitos específicos del escenario de comunicación secreta.


---

# Manual Básico de Steghide

Steghide es una herramienta de esteganografía que permite ocultar datos dentro de archivos de imagen y audio. Este manual proporciona una guía básica sobre cómo usar Steghide para ocultar y extraer información.

## Instalación

Para instalar Steghide en sistemas Unix-like, puedes utilizar el administrador de paquetes de tu distribución:

```
sudo apt install steghide       # Debian/Ubuntu
sudo yum install steghide       # CentOS/RHEL
```

Para sistemas macOS, puedes usar Homebrew:

```
brew install steghide
```

## Ocultar Datos

Para ocultar datos dentro de un archivo de imagen o audio, sigue estos pasos:

1. **Selecciona el archivo de cubierta:** Elige el archivo de imagen o audio en el que quieres ocultar los datos.
2. **Ejecuta el comando Steghide:** Utiliza el siguiente comando para ocultar los datos:

```
steghide embed -cf <archivo_de_cubierta> -ef <archivo_a_ocultar>
```

3. **Proporciona una contraseña:** Steghide te pedirá que ingreses una contraseña para proteger los datos ocultos.

## Extraer Datos Ocultos

Para extraer datos ocultos de un archivo de imagen o audio, sigue estos pasos:

1. **Selecciona el archivo de cubierta:** Elige el archivo de imagen o audio del que quieres extraer los datos ocultos.
2. **Ejecuta el comando Steghide:** Utiliza el siguiente comando para extraer los datos:

```
steghide extract -sf <archivo_de_cubierta>
```

3. **Proporciona la contraseña:** Si se ha protegido con contraseña, Steghide te pedirá que ingreses la contraseña para extraer los datos ocultos.

## Consejos de Seguridad

- Utiliza contraseñas seguras para proteger los datos ocultos.
- Mantén una copia de seguridad de los archivos originales y los archivos con datos ocultos, ya que Steghide puede causar pérdida de datos si se utilizan comandos incorrectos.

## Ejemplo de Uso

Supongamos que queremos ocultar un archivo de texto llamado `secreto.txt` dentro de una imagen llamada `imagen.jpg`. Ejecutamos los siguientes comandos:

```
steghide embed -cf imagen.jpg -ef secreto.txt
```

Luego, para extraer el archivo oculto de `imagen.jpg`, ejecutamos:

```
steghide extract -sf imagen.jpg
```

---

## FLUJO RESOLUCIÓN RETO ESTEGANOGRAFIA -  ESTEGOANALISIS

**Reto de Esteganografía para Hacking Ético**

**Descripción del Reto:**
En este reto de esteganografía, se te proporciona una imagen aparentemente normal, pero oculta dentro de ella hay un mensaje secreto. Tu tarea es utilizar técnicas de esteganografía para extraer este mensaje oculto y revelar su contenido. Este reto simula una situación de hacking ético donde necesitas recuperar información confidencial sin dañar el sistema o la propiedad.

**Archivo Adjunto:** [imagen.png](link_a_la_imagen.png)

**Solución:**

Paso 1: Inspección de la Imagen
- Descarga la imagen proporcionada y ábrela en un visor de imágenes.
- Realiza una inspección visual de la imagen para detectar cualquier anomalía obvia.

Paso 2: Análisis de Metadatos
- Examina los metadatos de la imagen para buscar pistas ocultas.
- Utiliza herramientas como ExifTool o la función de propiedades del archivo en tu sistema operativo para ver información incrustada en la imagen.

Paso 3: Esteganografía Visual
- Emplea herramientas de software especializadas en esteganografía para detectar posibles datos ocultos dentro de la imagen.
- Aplica técnicas como el análisis de LSB (Least Significant Bit) para buscar cambios sutiles en los bits menos significativos de la imagen que podrían indicar la presencia de datos ocultos.

Paso 4: Prueba de Esteganografía de Archivos
- Intenta extraer el mensaje oculto utilizando herramientas de esteganografía de archivos. Esto implica aplicar técnicas específicas para extraer datos ocultos de la imagen sin dañarla.
- Utiliza herramientas como Steghide o OpenStego para intentar recuperar el mensaje oculto.

Paso 5: Análisis Manual de Píxeles
- Si las técnicas automáticas no revelan el mensaje oculto, realiza un análisis manual de los píxeles de la imagen.
- Examina áreas específicas de la imagen que podrían parecer sospechosas o haber sido modificadas.

Paso 6: Esteganografía de Color
- Considera la posibilidad de que la información se haya ocultado mediante cambios sutiles en los colores de la imagen.
- Utiliza herramientas de análisis de color para detectar cambios mínimos que podrían indicar la presencia de datos ocultos.

Paso 7: Decodificación del Mensaje
- Una vez que hayas extraído los datos ocultos, decodifica el mensaje utilizando la técnica de cifrado o codificación que se haya utilizado.
- Aplica cualquier clave o algoritmo necesario para revelar el mensaje en texto legible.

**Nota:** La solución exacta dependerá de las técnicas utilizadas y la complejidad del ocultamiento del mensaje. Es importante tener en cuenta que el hacking ético implica el uso de estas habilidades para propósitos legítimos y autorizados, respetando siempre la privacidad y la legalidad.


///////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////


# VishwaCTF2023
    
  

  ![](https://github.com/albertominan/WriteUps/blob/9ee610cb82de3432e4316c9185fd3c584385207c/Esteganograf%C3%ADa/VishwaCTF2023/GUATEMALA/capturas/AV.gif)
  
### Solución
    
    
    vishwaCTF{pr073c7_ur_3X1F}
  
  
### Análisis

Analizamos metadatos y encontramos un Comment de la imagen en base64 que tras decodificarlo nos da la flag. 

![](https://github.com/albertominan/WriteUps/blob/9ee610cb82de3432e4316c9185fd3c584385207c/Esteganograf%C3%ADa/VishwaCTF2023/GUATEMALA/capturas/1.png)


********************************************************************************************************************************************************************


## Codificación Base 64

La codificación Base64 es un método para representar datos binarios utilizando un conjunto de 64 caracteres imprimibles. Estos caracteres incluyen letras mayúsculas y minúsculas, dígitos numéricos y algunos caracteres especiales como '+' y '/'. A menudo, una cadena codificada en Base64 terminará con uno o dos caracteres '=' que se utilizan para la alineación de los datos.

Aquí hay algunos indicadores que podrían ayudar a reconocer la codificación Base64:

1. **Caracteres específicos**: Una cadena codificada en Base64 contendrá caracteres específicos del conjunto de 64 caracteres permitidos, como letras mayúsculas y minúsculas, dígitos numéricos, '+' y '/'.

2. **Longitud y alineación**: La longitud de una cadena codificada en Base64 generalmente es un múltiplo de 4, ya que cada grupo de 4 caracteres en la codificación Base64 representa tres bytes de datos binarios. Además, puede haber uno o dos caracteres '=' al final de la cadena, los cuales se utilizan para la alineación.

3. **Preambulo**: En algunos casos, los datos codificados en Base64 pueden estar precedidos por un prefijo que indica que la cadena está codificada en Base64. Por ejemplo, "data:image/png;base64," es un preámbulo común en datos codificados en Base64 para imágenes en formato PNG.

4. **Decodificación exitosa**: Si tratas de decodificar una cadena en Base64 y obtienes éxito, eso es una fuerte indicación de que la cadena estaba codificada en Base64. La decodificación fallará si la cadena no está codificada en Base64 o si ha sido alterada de alguna manera.

Aquí tienes un ejemplo de una cadena codificada en Base64:

```
SGVsbG8gV29ybGQhIQ==
```

Y aquí está la versión decodificada:

```
Hello World!!
```

Si se sospecha que una cadena y sospechas que está codificada en Base64, puedes intentar decodificarla usando una herramienta en línea o un script en el lenguaje de programación de tu elección para confirmar si está en formato Base64 y para obtener los datos originales.

