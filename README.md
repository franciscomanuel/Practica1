Practica1:Infraestructura Virtual
=================================

El objetivo de la práctica es la creación de una aplicación y despliege en un PaaS. Yo he creado una sencilla aplicación 
en PHP y el PaaS que he escogido ha sido "OpenShift"

"OpenShift" es un producto de computación en la nube de plataforma como servicio de Red Hat.Este software funciona como 
un servicio que es de código abierto bajo el nombre de "OpenShift Origin", y está disponible en GitHub.
Los desarrolladores pueden usar Git para desplegar sus aplicaciones Web en los diferentes lenguajes de la plataforma.

Mi aplicación desarrollada ha sido una pequeña web en la que aparece una foto mia, seguida de mis datos (nombre, correo 
y twitter) y dos tablas. La primera de ella es mi horario para el primer cuatrimestre y la segunda tabla contiene
información sobre cada una de mis asignaturas(nombre, código, tipo ...).

He usado una licencia GPLV3. Esta licencia la he generado creando un nuevo archivo en el proyecto y seleccionando como 
LICENCE GPLV3.

Dicho esto, procedo a explicar los pasos para la creación de mi aplicación:

* En primer lugar, debemos darnos de alta en: https://www.openshift.com/
* Una vez dado de alta creo mi aplicacion con add application.
* Elegimos un lenguaje de programación para nuestra aplicación: yo he elegido PHP 5.3
* Damos un nombre a nuestra aplicación: practica1
* OpenShift registrará automáticamente el nombre de dominio para su aplicación: -franciscomanuel.rhcloud.com
* Genero mi clave pública (ssh-keygen) y la inserto para mi aplicación.  
* Pulsamos create application
* Después de crear la aplicación se puede activar funciones adicionales, como bases de datos.

Ya tengo creada mi aplicación. Ahora nos descargamos la aplicación a nuestro ordenador con la siguiente orden de git:

    git clone ssh://525e7c214382ec128e00014a@practica-franciscomanuel.rhcloud.com/~/git/practica.git/
    
Dentro de la carpeta practica tenemos nuestra carpeta php donde vamos a programar la aplicación (index.php)

Terminada de programar la aplicación subimos todos los archivos a "openShift":

    git add php
    git commit -a -m "añadido mi aplicación"
    git push
    
Ya está mi aplicación subida a "openshift" funcionando correctamente:

http://practica-franciscomanuel.rhcloud.com/
