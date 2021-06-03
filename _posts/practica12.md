# IAW_practica12

Vamos a crear un sitio web con worpress haciendo uso de bitnami, el cual es un servicio que ofrece imagenes de Amazon web services preconfiguradas, en nuestro caso cogeremos una de las maquinas que raen un debian con wordpress ya listo para funcionar

![image](https://user-images.githubusercontent.com/60846344/116872035-80cad800-ac15-11eb-9907-e81f2313ab16.png)

al hacer click en la AMI se nos abrira el lanzador d einstancias de EC2 para poder configurarla, le añadiremos el grupo de seguridad configurado para permitir el paso de ssh, http, https y mysql

![image](https://user-images.githubusercontent.com/60846344/116872095-993af280-ac15-11eb-92cb-4fd2246bdf7e.png)

![image](https://user-images.githubusercontent.com/60846344/116872140-b374d080-ac15-11eb-9d49-b4defc81551b.png)


![image](https://user-images.githubusercontent.com/60846344/116872572-63e2d480-ac16-11eb-9a7e-ae82e317b358.png)


una vez lanzada podremos acceder al sitio con la ip publica de la maquina, y si pulsamos en la esquina inferior derecha accederemos a la pagina de ayuda para loguearnos, en ella veremos como obtener las credenciales necesarias para iniciar sesion como administradores del sitio.
![image](https://user-images.githubusercontent.com/60846344/116872601-7230f080-ac16-11eb-86c5-d4b6d1f03185.png)

Tambien nos indicara que para acceder a phpmyadmin tendremos que hacer un tunel ssh, ya que solo se puede acceder desde el localhost, por lo que haremos una conexion ssh uniendo nuestro puerto 8888 a el puerto 80 de la maquina, de tal forma que podremos acceder a phpmyadmin poniendo en nuestro buscador la direccion localhost:8888

ssh -N -L 8888:127.0.0.1:80 -i "D:\clase\SEGUNDO\SRI\clavepem\sri.pem" bitnami@35.174.207.217
![image](https://user-images.githubusercontent.com/60846344/116873258-ab1d9500-ac17-11eb-8383-d2a78a079380.png)

Por ultimo para obtener las credenciales de acceso de administrador a wordpress mostraremos el archivo de las credenciales por consola

![image](https://user-images.githubusercontent.com/60846344/116873393-e6b85f00-ac17-11eb-8d51-b4143d10f126.png)

y ya podremos acceder a la administracio de nuestro sitio con esas credenciales

![image](https://user-images.githubusercontent.com/60846344/116873471-08b1e180-ac18-11eb-817d-907f01b4c031.png)
