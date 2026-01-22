# Integración de datos de la Convención Constitucional con fuentes externas
Desarrollo de trabajo de memoria para optar al título de Ingeniero civil en Informática

Joaquín Alejandro Castillo Tapia
Universidad Técnica Federico Santa María

En este proyecto se encuentran los archivos, documentos, y procesos necesarios y creados para la implementación documentada en el siguiente [documento](https://github.com/kakodrilo/Memoria/blob/main/Documento/Memoria_Castillo_Joaqu%C3%ADn.pdf)

A continuación, se detalla el orden del proyecto y los aspectos relevantes de cada una de las carpetas.

-------------------
## Estructura 

- **datos:** directorio que contiene los archivos de datos y estructura de las fuentes a integrar. Se consideraron los conjuntos de datos del Instituto Milenio Fundamento de los Datos (IMFD), Comparative Constitute Project (CCP) y Constitute Project (CP). 
- **Documento:** archivos editables utilizados en la construcción del documento. Aquí se consideran las figuras construidas en draw.io, y el comprimido .zip del documento escrito en Latex.
- **Preguntas:** archivos de consultas, resultados y visualizaciones utilizadas como ejemplos y para evaluar la estructura ontología planteada. Se divide en las consultas usadas para el conjunto de datos sobre los Constituyentes, CCP, Integración y Visualizaciones.  Las consultas para cada caso están en un archivo de texto, y los distintos resultados sus respectivos archivos csv. Todas las visualizaciones están en formato pdf para no perder calidad.
- **Ttl:** archivos turtle utilizados para almacenar la estructura y datos duros para poblarla. Aquí se encuentran los archivos descritos en el [documento](https://github.com/kakodrilo/Memoria/blob/main/Documento/Memoria_Castillo_Joaqu%C3%ADn.pdf) y  también los necesarios para cargar los datos del IMFD.

## Desarrollo y Resultados
### Ontología
La ontología propuesta y construida con la herramienta [Protégé](https://protege.stanford.edu/ ) se enceuntra en el archivo ontologia.owl de la ruta raíz del proyecto.  La representación gráfica de la ontología se presenta a continuación:


![Grafo de la ontología completa](https://github.com/kakodrilo/Memoria/blob/main/Visualizaciones/grafoCompleto.png)

### Procesamiento de datos
En el Jupyter Notebook **_Procesamiento de datos.ipynb_** se encuentra el proceso de extracción de datos del conjunto de CCP. Para esto, tal como se define en el documento, fueron utilizados los documento _countries.xml_, _chronology.xml_ y _ccpcnc\_v4.csv_. Como resultado de esto, se generan los archivos _Ttl/countries.ttl_, _Ttl/eventos.ttl_ y _Ttl/datosDuros.ttl_.

Para aplicar la integración entre las dos fuentes, se utilizó el proceso indicado en el Jupyter Notebook **_Integracion.ipynb_**. El cuál hace uso del archivo _Ttl/datosDuros.ttl_ para generar las relaciones respectivas entre los distintos eventos de CCP y los distintos tópicos de BCN. El mapeo de tópicos se documentó en el archivo Excel _Homologación Tópicos.xlsx_.

#### Ingeniería y Normalización de Datos
El mayor desafío técnico consititó en la limpieza y transformación de datos heterogeneos provenientes de las disintitas fuentes.
-	**Normalización**: Se implementaron procesos en Python para estandarizar nombres de países, formatos de fechas y codificación de caracteres, asegurando la compatibilidad con el esquema de carga de Prrotégé.
-	**Integración Semántica**: Se diseñó una ontología en formato OWL que permite el mapeo de tópicos de la Blibioteca del Congreso Nacional (BCN) con estándares internacionales.

### Validación
Una de las validaciones del trabajo realizado, fue la consulta sobre la ontología de conocimiento no trivial y la posterior visualización de los datos obtenidos. Para la creación de las visualizaciones, se utilizaron los distintos archivos csv del directorio _Preguntas_. El proceso para la creación de las visualizaciones presentes en el documento está en el Jupyter Notebook **_Visualizaciones.ipynb_**

#### Análisis y Visualización
Las visualizaciones fueron diseñadas para ser accesibles al público general, transformando procesos de consulta complejos sobre la ontología en información de fácil lectura.

Algunos ejemplos de visualizaciones resultantes son:

**Mapas de calor**

Año de publicación de la constitución actual de cada país
![Año de publicación de la constitución actual de cada país](https://github.com/kakodrilo/Memoria/blob/main/Visualizaciones/A%C3%B1o%20de%20la%20ultima%20constitucion%20de%20cada%20pa%C3%ADs.jpg)

Densidad de reformas constitucionales en Sudamerica entre el año 2000 y 2023
![Cantidad de reformas en sudamerica entre 2020 y 2023](https://github.com/kakodrilo/Memoria/blob/main/Visualizaciones/Cantidad%20enmiendas%20sudamerica%20en%202000.jpg)


**Cruce de datos**

Análisis de los temas con mayor presencia en constituciones a nivel mundial que también fueron discutidos en la Convención Constitucional
![Top 20 temas presentes en las constituciones mundiales que también se discutieron en la Convención Constitucional](https://github.com/kakodrilo/Memoria/blob/main/Visualizaciones/top%2020%20temas%20relacionados%20%20a%20const%20vigentes.jpg)

Cantidad de temas discutidos en la Conveción Constitucional que estén presentes en las constituciones actuales de América y Europa.
![Distribución de cantidad de temas disctutidos en la convención presentes en constituciones actuales de América y Europa](https://github.com/kakodrilo/Memoria/blob/main/Visualizaciones/cantidad%20de%20temas%20de%20la%20CC%20en%20const%20actuales.jpg)
