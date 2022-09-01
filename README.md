# Intro
Con respecto a la asignación de Synapse SQL Pool como Data Source en un Gateway específico, se presenta una guía para realizar la asignación del SQL Pool a un Gateway definido.
## 1.	Linkear PBI en Synapse:
-	Lo primero que debe realizar es asociar el workspace de PBI Service, donde quiere alojar el dataset, en Synapse Analytics.
-	Descargar el archivo pbix y publicarlo en el workspace. Recomiendo que se publique en el mismo workspace asociado a Synapse para que pueda trabajarlo también desde el studio.
## 2.	Configuración Dataset
-	Dirigirse al workspace donde se publicó el dataset (esto sucede al mismo tiempo que se publica el reporte).
-	Al identificar el dataset, darle clic a los 3 puntos y elegir la opción de configuración.
 

-	En caso sea necesario, actualizar las credenciales de conexión.
 
-	Ahí mismo, tenemos la opción de modificar la conexión del Gateway.
 
-	Por defecto no viene asociado a ningún Gateway ya que está en la nube; sin embargo, uno puede optar por alojarlo en un data Gateway.
## 3.	Configurar Gateway en el Dataset
-	Habilitar el uso del dataway (colocarlo en ON)
 
-	Al activarlo, se listarán los gateways que tenemos disponibles. Incluso veremos que el Gateway no está configurado correctamente. Para configurarlo, en acciones darle clic a la rueda (redirección a la configuración directa) o a la fecha (revisar lo que se requiere realizar). En este caso, le daré clic a la fecha.
 
-	Al desplegarlo podemos ver que nos indica que debemos agregar el data source al Gateway. Para ello, le damos clic al hipertexto “Add to Gateway”
 
-	Se abrirá la pantalla de configuración del data source. Completar los datos y darle clic a Add.
 
-	Una vez que se haya agregado, nos redirigirá al dataset. Ingresamos a Gateway Connection. Notaremos que ahora aparece el Gateway en estado running.

-	Habilitaremos el uso del Gateway
 
-	Seleccionaremos el Gateway que queremos utilizar y esté en estado running.
 
-	Asignaremos el dataset al data source que creamos en el Gateway, en la opción de Map to:

-	Darle clic a Apply
 
## 4.	Validar que el data source esté en el Gateway
-	Podemos verificar que el data source se encuentra configurado correctamente en el Gateway.
 
## 5.	Referencias
-	[Synapse Linked Services PBI: Quickstart: Linking a Power BI workspace to a Synapse workspace - Azure Synapse Analytics | Microsoft Docs](https://docs.microsoft.com/en-us/azure/synapse-analytics/quickstart-power-bi)
-	[PBI Data Sources: Power BI data sources - Power BI | Microsoft Docs](https://docs.microsoft.com/en-us/power-bi/connect-data/power-bi-data-sources)
-	[Agregar Data sources en un gateway: Add or remove a gateway data source - Power BI | Microsoft Docs](https://docs.microsoft.com/en-us/power-bi/connect-data/service-gateway-data-sources)
