# Proyecto Final Fiu

Inicialmente el proyecto buscaba entrenar un modelo para que pudiera reconocer sonidos de la naturaleza y de la ciudad, la idea era principalmente que luego de que fueran clasificados los sonidos, se generara una representación visual de estos, en un espacio de la pantalla/lienzo, diferenciándose principalmente por los colores que aportaban, siendo los dibujos originados de sonidos de naturaleza, brillantes y coloridos, en contraste con los provenientes de la ciudad, los que no mostrarían más color que una escala de grises.

Estas formas se irían superponiendo en un espacio para formar una composición, de la que podrían darse conclusiones respecto al tipo de ambiente en que nos encontrábamos.

Se recopilaron los sonidos y se realizaron los dibujos, incluso se entrenó a la IA

![image](https://github.com/Toomanypanchos/audiv027-2023-2/assets/89993556/b3f4ae1f-ac21-483f-ae76-1ab5fd83afa3)
![image](https://github.com/Toomanypanchos/audiv027-2023-2/assets/89993556/84639235-cca9-4164-9a7c-17a7c8d1dc30)
Realizacion propia

![image](https://github.com/Toomanypanchos/audiv027-2023-2/assets/89993556/fe25a88f-8d14-40b8-a40e-869fd54fa781)

---------------------------------------------------------

Durante este proceso nos dimos cuenta de que era mucho más interesante ser capaces de discernir entre diversas especies de aves. y no considerar a el sonido de la naturaleza como uno solo. 
Tomando la decisión de cambiar el proyecto, manteniendo un enfoque similar, pero utilizando unicamente sonidos de aves.
Esta decisión se toma en parte luego de conversaciones con una compañera que está realizando su proyecto de título respecto a un tema similar.

## Pequeño Resumen del Proyecto:

UNÍSONO es la publicación y edición de una especulación ecológica que se pregunta sobre la representación de la animalidad, de la relación comunicativa interespecie y la que surge entre los humanos para hacer ciencia, investigación y creación alrededor de la naturaleza. Surge a partir de la creación de un sistema de escritura experimental ECOS, una representación gráfica espontánea vinculada a la vocalización de las aves. 

Sitúa una ruta de exploración al cerro la Cruz en la precordillera andina-metropolitana desde donde se avistan 26 especies distintas de aves. El sonido y la capacidad de escucha humana en el recorrido al territorio resultan en ECOS. Esta escritura explora la posibilidad de expresar el sonido percibido en un signo gráfico en contacto con la naturaleza, abriendo así un canal interpretativo interespecie desde un emisor animal y un receptor humano. El resultado son 26 signos o caracteres digitalizados y sistematizados para su uso, adquiriendo así un nuevo lenguaje que posibilita la investigación a través de la creación de territorios imaginados, con el fin último de especular sobre las relaciones entre seres vivos que den pie a una construcción distinta de la realidad, modificando así las prácticas humanas con el hábitat y el entorno natural, generando a su vez un acervo cultural del patrimonio sonoro del paisaje que habitamos. 

[''Afiches''.pdf](https://github.com/Toomanypanchos/audiv027-2023-2/files/13454963/Afiches.pdf)

Por lo que en el proyecto actual se busca entrenar a una IA para que sea capaz de discernir entre especies de aves dependiendo de sus sonidos.
los que luego de identificados se traduzcan al abecedario construido por nuestra amiga, letras que se escribirán, simulando un texto y creando párrafos que permitan generar un contexto visual de aquello que se escuchó y fue interpretado por la IA.

Modelo de como deberian clasificarse los objetos para poder ordenar la imagenes.

![image](https://github.com/Toomanypanchos/audiv027-2023-2/assets/89993556/01f8697d-dee5-4add-a3ee-f06c056eed5e)

Una vez concretada la dirección del proyecto se hicieron los siguientes pasos en orden.
 1   -Se recolectaron los audios de cada especie y se ordenaron:
 
 http://avesdechile.cl (biblioteca de aves de chile)
 https://xeno-canto.org (biblioteca de cantos de aves geolocalizados)
 ![image](https://github.com/Toomanypanchos/audiv027-2023-2/assets/89993556/77c166fe-c5c6-421c-ad8c-73b8c56cc868)


2   -Se alimento a la IA con los audios recolectados:

![image](https://github.com/Toomanypanchos/audiv027-2023-2/assets/89993556/897a1bb3-075d-4401-97a0-b23678c7f038)
![image](https://github.com/Toomanypanchos/audiv027-2023-2/assets/89993556/cf02b90b-21cf-4487-8298-0bceb7e57684)

Algo que destacar de este proceso fue la manipulación los archivos para incrementar la cantidad de muestras con las que alimentábamos al modelo.
esto se hizo cortando los sonidos en diferentes momentos de los cantos de la aves, pensando que asi la IA podría reconocer secciones de los cantos también y no solo uno completo.

![image](https://github.com/Toomanypanchos/audiv027-2023-2/assets/89993556/b7fcf260-b4ce-4a5f-b97d-ef5ccffe986d)

3   -Se entreno la IA con 200 épocas:

![image](https://github.com/Toomanypanchos/audiv027-2023-2/assets/89993556/99fb5783-a7b6-4518-a080-1f33ccabffdd)

Con el modelo entrenado podíamos proceder a escribir el código para utilizarla.

4   -Escribir Codigó

nosotros escribiendo el código 
![image](https://github.com/Toomanypanchos/audiv027-2023-2/assets/89993556/fa755f33-4ae5-4cc9-932b-202aea8a0075)

5   -Convertir letras a imágenes:
ahora que el código es capaz de reconocer un sonido e ir a buscar la imagen que corresponde a ese sonido se "convirtió" cada letra en una imagen.

![image](https://github.com/Toomanypanchos/audiv027-2023-2/assets/89993556/a7378acf-6e8e-4205-889e-672158e7febb)

6   -Manipular cómo se posicionaban las imágenes, primeramente las imágenes se sobreponían encima de ellas por lo que no era posible ver un historial de lo que se escribía (escuchaba) por lo que se determinó un orden en el que se ponían las imágenes usando el concepto de (i) y (i++) para que usando un padding las letras se fueran ordenando de izquierda a derecha, presentándose el problema de que las letras se salían del lienzo por lo que se delimitó a escribir solo dentro del canvas, llegado el momento de topar con el borde derecho volver a la izquierda considerando el espaciado de una imagen hacia abajo y en el caso de llegar al final del canva volver al inicio y remplazar la imagen que usaba esa posición anteriormente.

![image](https://github.com/Toomanypanchos/audiv027-2023-2/assets/89993556/68ba7e25-2d2d-4910-80ee-9d9632f65650)

### actualidad 
El código funciona y es capaz de diferenciar sonidos de aves, siendo el mayor problema los espacios de silencio que se generaban entre los cantos de aves, creemos que es algo interesante de igual forma, porque parte del sonido es la falta de este, pero no fuimos más allá respecto a esta decisión.

https://editor.p5js.org/pargato/full/wLlQCdmfT

### Conclusión y proyecciones.
- La captura de datos y su claridad es super importante para el funcionamiento correcto

- Para la clasificación de sonidos, en particular de aves, que pueden ser similares en varias oportunidades, la data debe ser mas grande para que pueda arrojar un resultado con mayor precision.
  
- Cuando existen demasiadas variables el algoritmo es muy facil de confundir y pierde su precision (no necesariamente algo negativo
  
- Seria interesante trabajar esto desde un nivel tipografico, no tratando a las letra como imagenes sino como glifos, lo que permitiria una comprension y distribucion mas similar a la escritura

- Con un codigo mejor entrenado podria tratarse la identificación en relacion a los porcentajes con los que se identifique un ave.


Referencias 
-codigo base para clasificar sonidos
https://github.com/orgs/CodingTrain/repositories?page=2

https://p5js.org/reference/#/p5/image

https://www.youtube.com/@TheCodingTrain


