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

2. Pantallazo donde se vea el acceso al servidor web utilizando un navegador web (recuerda que tienes que acceder a la ip del ordenador donde tengas instalado docker)

3. Pantallazo donde se vean las imágenes que tienes en tu registro local.

4. Pantallazo donde se vea cómo se elimina el contenedor (recuerda que antes debe estar parado el contenedor).