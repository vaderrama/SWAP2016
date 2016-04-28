#Pr�ctica 2 
## Realizada por: Esperanza Jim�nez �vila, Juan Alvarez Carrasco


A continuaci�n pongo las diferentes capturas de pantalla con los resultados obtenidos de la pr�ctica 2:


##Uso herramienta rsync

Primero probamos el funcionamiento del rsync, clonando la carpeta con el contenido del servidor web principal, en la m�quina 2 (secundaria). Finalmente comprobamos que se encuentra compartida dicha carpeta en la m�quina 2:

![img](https://github.com/espe90/swap/blob/master/practicas/P2/rsync_servidor2.png)


##Acceso sin contrase�a para ssh

Para realizar el acceso de una m�quina a otra sin la necesidad de poner contrase�as, realizaremos los siguientes pasos:

Con el comando ssh-keygen generaremos la clave de tipo dsa. Ver siguiente captura.
![img](https://github.com/espe90/swap/blob/master/practicas/P2/ssh-keygen.png)
		
A continuaci�n, hacemos la copia de la clave existente con la ayuda del comando ssh-copy-id. Ver siguiente captura.

![img](https://github.com/espe90/swap/blob/master/practicas/P2/copy-id.png)
		
Finalmente hacemos la comprobaci�n para ver que se puede tomar el control de la m�quina 1 desde la m�quina 2. Ver siguiente captura.

![img](https://github.com/espe90/swap/blob/master/practicas/P2/acceso_sin_passwd.png)

		
##Programar tareas con crontab

Para esta parte de la pr�ctica establecemos una tarea en cron que se ejecute cada hora para mantener actualizado el contenido del directorio /var/www entre las dos m�quinas. Para ello accedemos al archivo /etc/crontab y a�adimos la tarea. Esto queda de la siguiente manera:

![img](https://github.com/espe90/swap/blob/master/practicas/P2/crontab.png)