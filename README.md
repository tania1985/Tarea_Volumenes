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

        https://localhost/hola.htm
   
    Crea un contenedor 'asir_web1' que use este mismo directorio para 'htdocs' y el puerto 8000
        $docker run -dit --name asir_web1 -p 8000:80 -v /home/asir2/sri/apache/paginas:/usr/local/apache2/htdocs httpd:2.4
    Utiliza Code para hacer un hola mundo en html
        echo "<p>Hola mundo</p>" >> README.html
    Crea otro contenedor 'asir_web2' con el mismo directorio y a otro puerto, por ejemplo 9080.
    
      $docker run -dit --name asir_web2 -p 9080:80 -v /home/asir2/sri/apache/paginas:/usr/local/apache2/htdocs httpd:2.4

    Comprueba que los dos servidores 'sirven' la misma página, es decir, cuando consultamos en el navegador:
        http://localhost:9080 
        http://localhost:8000

         Aparece: Index of/
    Tienen que salir la misma página web
        Aparece: "Index of/" en ambas igual