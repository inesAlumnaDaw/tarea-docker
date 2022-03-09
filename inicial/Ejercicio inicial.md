# Resolución del ejercicio inicial

> Realizado por Inés Menéndez

Crear un contenedor demonio a partir de la imagen `nginx`, el contenedor se debe llamar `servidor_web` y se debe acceder a él utilizando el puerto 8181 del ordenador donde tengas instalado docker.

### Cuestiones 

1. Pantallazo donde se vea la creación del contenedor y podamos comprobar que el contenedor está funcionando.

   ```bash
   docker run -d -p 8181:80 --rm --name servidor-web nginx
   docker ps -a
   ```

   <img src="Ejercicio%20inicial.assets/image-20220309161117043.png" alt="image-20220309161117043" style="zoom:80%;" />

   > Se muestra a modo de ejemplo cómo va avanzando el repositorio 
   >
   > Fijarse en que se ha utilizado una rama **c1** para resolver la primera cuestión, y una vez finalizado se fusionó con 'main'
   >
   > -- NO es necesario documentarlo

   ![image-20220309161645365](Ejercicio%20inicial.assets/image-20220309161645365.png)

2. Pantallazo donde se vea el acceso al servidor web utilizando un navegador web (recuerda que tienes que acceder a la ip del ordenador donde tengas instalado docker)

<img src="Ejercicio%20inicial.assets/image-20220309161929825.png" alt="image-20220309161929825" style="zoom:67%;" />

> Vemos, a modo de ejemplo, cómo está el repositorio con las dos ramas:

<img src="Ejercicio%20inicial.assets/image-20220309162242419.png" alt="image-20220309162242419" style="zoom:50%;" />

3. Pantallazo donde se vean las imágenes que tienes en tu registro local.

```bash
docker images
```

<img src="Ejercicio%20inicial.assets/image-20220309173417360.png" alt="image-20220309173417360" style="zoom:80%;" />

> Se muestra cómo vamos actualizando el repositorio, utilizando ramas y subiendo los cambios al remoto -- NO es necesario documentar esto en la tarea, se muestra como orientación...

<img src="Ejercicio%20inicial.assets/image-20220309173847256.png" alt="image-20220309173847256" style="zoom:60%;" />

3. Pantallazo donde se vea cómo se elimina el contenedor (recuerda que antes debe estar parado el contenedor).

   Para resolver esta cuestión, creamos un contenedor que expone el puerto 80 al puerto 8181 de nuestro cliente, vemos que está 'corriendo'-UP, lo paramos, vemos que se ha parado y lo borramos

```bash
docker run -d -p 8181:80 --name servidor-web nginx
docker ps
docker stop servidor-web
docker ps -a
docker rm servidor-web
```

<img src="Ejercicio%20inicial.assets/image-20220309175040912.png" alt="image-20220309175040912" style="zoom:80%;" />