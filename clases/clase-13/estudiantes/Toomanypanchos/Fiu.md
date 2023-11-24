# Proyecto final Fiu

Inicialmente el proyecto buscaba entrenar una para que pudiera reconocer entre sonidos de la naturaleza y de la ciudad, la idea era principalmente que luego de que fueran clasificados los sonidos, se generara una representación visual de estos, en un espacio de la pantalla. Diferenciándose principalmente por los colores que aportaban, siendo los dibujos originados de sonidos de naturaleza, brillantes y coloridos, en contraste con los provenientes de la ciudad, los que no mostrarían más color que una escala de grises.

Estas formas se irían superponiendo en un espacio para formar una composición, de la que podrían darse conclusiones respecto al tipo de ambiente en que nos encontrábamos.

Se recopilaron los sonidos y se realizaron los dibujos, incluso se entrenó a la IA

![image](https://github.com/Toomanypanchos/audiv027-2023-2/assets/89993556/b3f4ae1f-ac21-483f-ae76-1ab5fd83afa3)
![image](https://github.com/Toomanypanchos/audiv027-2023-2/assets/89993556/84639235-cca9-4164-9a7c-17a7c8d1dc30)
Realizacion propia
![image](https://github.com/Toomanypanchos/audiv027-2023-2/assets/89993556/fe25a88f-8d14-40b8-a40e-869fd54fa781)

---------------------------------------------------------

Durante este proceso nos dimos cuenta de que era mucho más interesante ser capaces de discernir entre diversas especies de aves. y no considerar a el sonido de la naturaleza como uno solo. 
Tomando la decisión de cambiar el proyecto, manteniendo un enfoque similar, pero solo involucrando sonidos de aves.
Esta decisión se toma en parte luego de conversaciones con una compañera que está realizando su proyecto de título respecto a un tema similar.

## Pequeño resumen del proyecto:

UNÍSONO es la publicación y edición de una especulación ecológica que se pregunta sobre la representación de la animalidad, de la relación comunicativa interespecie y la que surge entre los humanos para hacer ciencia, investigación y creación alrededor de la naturaleza. Surge a partir de la creación de un sistema de escritura experimental ECOS, una representación gráfica espontánea vinculada a la vocalización de las aves. 

Sitúa una ruta de exploración al cerro la Cruz en la precordillera andina-metropolitana desde donde se avistan 26 especies distintas de aves. El sonido y la capacidad de escucha humana en el recorrido al territorio resultan en ECOS. Esta escritura explora la posibilidad de expresar el sonido percibido en un signo gráfico en contacto con la naturaleza, abriendo así un canal interpretativo interespecie desde un emisor animal y un receptor humano. El resultado son 26 signos o caracteres digitalizados y sistematizados para su uso, adquiriendo así un nuevo lenguaje que posibilita la investigación a través de la creación de territorios imaginados, con el fin último de especular sobre las relaciones entre seres vivos que den pie a una construcción distinta de la realidad, modificando así las prácticas humanas con el hábitat y el entorno natural, generando a su vez un acervo cultural del patrimonio sonoro del paisaje que habitamos. 

[''Afiches''.pdf](https://github.com/Toomanypanchos/audiv027-2023-2/files/13454963/Afiches.pdf)

Por lo que en el proyecto actual se busca entrenar a una IA para que sea capaz de discernir entre especies de aves dependiendo de sus sonidos.
los que luego de identificados se traduzcan al abecedario construido por nuestra amiga, letras que se escribirán, simulando un texto y creando párrafos que permitan generar un contexto visual de aquello que se escuchó y fue interpretado por la IA.

Una vez concretada la dirección del proyecto se hicieron los siguientes pasos en orden.
 -Se recolectaron los audios de cada especie y se ordenaron:
 ![image](https://github.com/Toomanypanchos/audiv027-2023-2/assets/89993556/77c166fe-c5c6-421c-ad8c-73b8c56cc868)

-Se alimento a la IA con los audios recolectados:
![image](https://github.com/Toomanypanchos/audiv027-2023-2/assets/89993556/897a1bb3-075d-4401-97a0-b23678c7f038)
algo que destacar de este proceso fue la manipulación los archivos para incrementar la cantidad de muestras con las que alimentábamos al modelo.
esto se hizo cortando los sonidos en diferentes momentos de los cantos de la aves, pensando que asi la IA podría reconocer secciones de los cantos también y no solo uno completo.
![image](https://github.com/Toomanypanchos/audiv027-2023-2/assets/89993556/b7fcf260-b4ce-4a5f-b97d-ef5ccffe986d)

-Se entreno la IA con 200 épocas:
![image](https://github.com/Toomanypanchos/audiv027-2023-2/assets/89993556/99fb5783-a7b6-4518-a080-1f33ccabffdd)
Con el modelo entrenado podíamos proceder a escribir el código para utilizarla.


texto
