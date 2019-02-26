# Inf1ArquitecturaBasica


## Integrantes

	César Alarcón
	Yhon Esteves
	Sara Guzmán
	
### Descripción

El ejercicio se realizó para la gestión documental de peticiones realizadas a la dirección de peticiones, quejas y reclamos, dirigidas al área de "Centro de Soluciones" de una empresa de Telefonía, estas peticiones son recibidas a traves de una página web o call center, para su posterior envío y procesamiento de acuerdo al tipo de solicitud, finalizando con un estudio de caso y respuesta al usuario una vez la petición ha sido solucionada. 

### Diagrama de arquitectura Básica

![Diagrama de flujo del colisionador](
        /images/BasicDiag1.jpg
      )
	  
	  
### Justificación

Para esta situación se pensó en una Arquitectura Cliente/ Servidor, debido a que se tiene un cliente, el cual realiza una petición (telefónica o vía página web), el servidor está a la espera del tipo de solicitud que el cliente espera realizar y de esta forma devolver el formulario correspondiente al tipo de solicitud, para que nuevamente el cliente realice una petición.

Esta petición es recibida nuevamente por el servidor, el cual es el encargado de almacenarla junto con los soportes documentales de la misma en la base de datos.

Una vez almacenada la solicitud, esta será consultada por el centro de soluciones, quienes determinarán el proceso que se debe realizar para la gestión de cada una, el resultado de este proceso será informado al usuario previa modificación del estado de la solicitud en la base de datos.

Consideramos ideal esta Arquitectura, debido a que el proceso de gestión documental de PQR tiene intrínsecamente un grado de complejidad no muy elevado y no requiere la implementación de nuevos servicios o funcionalidades a futuro; por otro lado, la Arquitectura Monolítica no es conveniente ya que no permite una correcta mantenibilidad del sistema para garantiza  la operación de las funcionalidades ya implementadas, y además no corre en una sola unidad de procesamiento.
