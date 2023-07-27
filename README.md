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

![Alt text](https://lh3.googleusercontent.com/fife/AKsag4MH-S-VxJDeuJT5Ab3tItHiSEuAEo8AwEBXFY4V3om0tCH95kR9ZifowNlNCvWKO-Xo2DWsfC4szOsQQRCXCnvaz-wfvmLUDtev8DpsmNj8TMdIZtRsVy1FPHBl5wsrasdz8QrhWVUhzzhvqj_12nYY3e9yEwlR5_kAGT3MjJYP-Q8TvSap8iNsh9_K3oE5KV2o4n57OHXU_yBLT0nDwXWRvg0ATFt0ES86fGp_YOqedtfeVMFDcN1WQKA_wo-5JHnOMuYDPquyVGh-Og8G3r2bX9dRjQPIDAJgX5Dtn8I1xj5tjiahPAHNwaWXTRVEah_bRMUQ3CfDz79c20AN-QQ2JNenA2u8lsNsL1Pn5x1z8G4p0Ap4c-faBmriCW7Pa_xSGUtvXfuJs7B4-nw1oU3YDNwctpSg49FX5H0TBHFSkHsFx4epLaJWT_rnC_nTVvaI3xYy0C3BnU9l38H2HruBPQvQ4fmSGc3f66AFiNu8XHrBocNtv21tRAZ2pU9Wv5585nfRc5zNzLmCj-HPptSORcR5tyg-tXkfJERkWWrT9sMtSckRIjtXGTtBRoH2UJ4gsRrw9h3G1vY-hZR63ly-VW0quC2qoz-apCM78KcaAWkqqMsqABNEaRTR0lIUwGnSdcIukvZw7aDad5IiBCrBLIcaf6u-GFDnsfHHdmKZSXO4GoLv_RwwP1F9Rwrb6yMUngmvG2KKLi-oDtYWSX6MK7CA18C_IVM50_2D0cyvNoeSgu6OZnZxMdxy3tj3UTNgceQBN_NFxgLHF-8lBHfVWEiXX7G6WNy-IX8_QMoUJrcOymmkbY3ekyoTAE5ql_OjFB6EgJdWJZIPPzGC_7KTESZGuan5CyiJaZNE_kuemqWJdBao6TeARBMvYXK1XhwT2N53lexGaP_kbZDA4Gexl1pIJnJV4MauV4StyfJHc6jLXI3turcdwujBvv22rqA1CqIqN4-gj0nXp7OAlhygxm--hiAV__qkdLofR_5q4cP7GPxx8QqMoabF8Bv6zmiY40kLHi8fiQ6Kv7u3gn8CXU8lF3ZkutmEP33OSoJ0k--bXC6Gbhz5kUq6WoYoT_CsUMnfelGhou0YrsgFsA1Au68gb9xvmYVvP-On0K6hzpqaEZV7yS2QXDdZ_OCA6O4u5E3tM_QIy_pGAWahAKrDIls4CIDXSSnRkFTBgOb-P0k7F_PcWiggyN42DmP4USXEed4oTG-GhacNUWwzkU1b_P_zwnWx--aQeEtqHRDw1t8sVU2KMg87zHvQLoQulOQ4llei337-P2xMPKfjlEywftD2ILvcKRug0cxNYQ2bXOrXpXw9S2HoKoJFrWrVHmmoGMRRDIemCKHy4qnVbg04VN-lcgTeO-CpbqIfDIpwooKi6qEV9BgRYylqsGwmyphc9AQ4wQenS8hYE4te91tPu6Gr0RkY37Yk5VIR4KCoGufdQdYjG6--brR42Wgs01c0Akar2SVh2XywC2Z9hOUP_PuEFixk2QZJ0mV9Gz7wQETBXk6whpEVgyLKexplvwW3p_Spz5g8RH1LrejGE7Tu4aRYb4srp9_AlJWOak3YmjRKwXNf2uNfNs-yFi89ZxXfqYaLBXacqeD7Cg=w1920-h929)

### Procesamiento de datos
En el Jupyter Notebook **_Procesamiento de datos.ipynb_** se encuentra el proceso de extracción de datos del conjunto de CCP. Para esto, tal como se define en el documento, fueron utilizados los documento _countries.xml_, _chronology.xml_ y _ccpcnc\_v4.csv_. Como resultado de esto, se generan los archivos _Ttl/countries.ttl_, _Ttl/eventos.ttl_ y _Ttl/datosDuros.ttl_.

Para aplicar la integración entre las dos fuentes, se utilizó el proceso indicado en el Jupyter Notebook **_Integracion.ipynb_**. El cuál hace uso del archivo _Ttl/datosDuros.ttl_ para generar las relaciones respectivas entre los distintos eventos de CCP y los distintos tópicos de BCN. El mapeo de tópicos se documentó en el archivo Excel _Homologación Tópicos.xlsx_.

### Validación
Una de las validaciones del trabajo realizado, fue la consulta sobre la ontología de conocimiento no trivial y la posterior visualización de los datos obtenidos. Para la creación de las visualizaciones, se utilizaron los distintos archivos csv del directorio _Preguntas_. El proceso para la creación de las visualizaciones presentes en el documento está en el Jupyter Notebook **_Visualizaciones.ipynb_**
