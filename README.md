# Tarea_Volumenes

    Descarga la imagen 'httpd' y comprueba que está en tu equipo.
        $ docker pull httpd
    Crea un contenedor con el nombre 'asir_httpd'.
        Ayuda
        $ docker run -it --name asir_httpd-app -p 8080:80 -v "$PWD":/usr/local/apache2/htdocs/ httpd:2.4
    Mapea el puerto 80 del contenedor con el puerto 8000 de tu máquina.
         $ docker run -dit --name asir_apache -p 8000:80 httpd:2.4
    Utiliza bind mount para que el directorio del apache2 'htdocs' este montado un directorio que tu elijas.

        Utiliza -v "$PWD"/htdocs:/usr/local/apache2/htdocs/
        
        $docker container run -d -p 8000:80 -v "$$PWD"/htdocs:/usr/local/apache2/htdocs/

    Realiza un 'hola mundo' en html y comprueba que accedes desde el navegador.
    Crea un contenedor 'asir_web1' que use este mismo directorio para 'htdocs' y el puerto 8000
    Utiliza Code para hacer un hola mundo en html
    Crea otro contenedor 'asir_web2' con el mismo directorio y a otro puerto, por ejemplo 9080.
    Comprueba que los dos servidores 'sirven' la misma página, es decir, cuando consultamos en el navegador:
        http://localhost:9080 
        http://localhost:8000
    Tienen que salir la misma página web
