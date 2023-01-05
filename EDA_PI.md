## **Informe EDA en Power bi:**  

<hr>  

**Tablas con las que vamos a trabajar:**

- `penint100hogares:` Penetración de Internet fijo (accesos por cada 100 hogares).   

- `tecnologias:` Acceso a Internet fijo por tecnología y provincia  

- `mbps de bajada:` Velocidad media de bajada de Internet fijo por provincia  

- `pen_hogares_int:` Penetración por hogares nacional de Internet fijo  

- `ingresos:` Ingresos trimestrales por la prestación del servicio de Internet fijo  

- `acceso a banda ancha/ang:` Accesos a banda ancha y banda angosta por provincia  

- `vel_internet:` Distribución de los accesos totales nacionales a Internet fijo por velocidad 

<hr>  

**El proceso de EDA (Exploratory Data Analysis) en Power BI incluye los siguientes pasos:**  

 <p align="center">
<img src="https://cdn-images-1.medium.com/max/1000/1*Owa2rsDG6Rwv1IM_RdsL3A.gif"  height=300>
</p>   

1- `Carga y limpieza de los datos:` en este primer paso, cargamos los datos en Power BI a través de un script de python (versión 3.7.7). Realizamos una limpieza de los mismos para eliminar duplicados, valores faltantes o errores. Se encontraron los siguientes errores:  
        - Columna año: se corrigió el error "2019 *" por año "2019".  
        - Columna trimestre: ya que tenía errores "3*", "2*" y "1*", se corrigió a "3", "2", "1".  
        - Columna cablemodem: se cambió el error "-0" a "0", eran equivalente al 1% de los datos.  
        - Se eliminó una columna que tenía datos vacíos en "vel_internet".  
        - Se eliminaron filas vacías que estaban al final de las tablas.  

2- `Transformación de los datos:` en este segundo paso, transformamos los datos de manera que sean más fáciles de analizar.  
        - Agregué una columna "fecha" en cada tabla que combinaba el año y trimestre para poder relacionarlos.  
        - Cree una tabla "calendario" para relacionar todas las tablas por "fecha".  
        - Se cambió el valor de columnas que estaban en "texto" a "decimal" o "entero" ya que correspondían a números.  
        - Se creó una tabla "inflación" para poder usarla con los ingresos.  

3- `Visualización de los datos:` en este tercer paso, cree gráficos y tablas para visualizar los datos y obtener una mejor comprensión de los mismos.  

4- `Análisis de los datos:` en este cuarto paso, realicé pruebas estadísticas y otras técnicas de análisis de datos para profundizar en los patrones y tendencias encontrados en los datos.  




