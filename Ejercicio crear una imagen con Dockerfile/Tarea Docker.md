1. Pantallazo/bloque de código con el Dockerfile

   ```bash
   nano /Desktop/ejemplo1/Dockerfile
   ```

   ![image-20220201201245533](C:\Users\Sergio\Desktop\Tarea crear imagen Docker\image-20220201201245533.png)

2. Pantallazo donde se vea el comando que crea la nueva imagen.

   ```bash
   sudo docker build -t imagenprueba
   ```

   

3. ![image-20220201204414189](C:\Users\Sergio\Desktop\Tarea crear imagen Docker\image-20220201204414189.png)

4. Pantallazo donde se vea la imagen subida a tu cuenta de Docker Hub.

   ![image-20220202124956490](C:\Users\Sergio\Desktop\Tarea crear imagen Docker\image-20220202124956490.png)

5. Pantallazo donde se vea la bajada de la imagen - por parte de otra persona del grupo - y la creación de un contenedor.

   ```bash
   sudo docker pull inufirot/ejemplo1:imgdf
   ```

   ![unknown](C:\Users\Sergio\Desktop\unknown.png)![unknown (1)](C:\Users\Sergio\Desktop\unknown (1).png)

6. Pantallazo donde se ve el acceso al navegador con el sitio servido

