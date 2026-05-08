# Instalar-Archlinux
## Guia oficial
https://wiki.archlinux.org/title/Installation_guide_(Espa%C3%B1ol)

## Instalación
1. Nada más iniciar con la iso tendremos este terminal.
![1](https://hackmd.io/_uploads/B1fhfKsCZe.png)

2. Asignamos la distribución del teclado en el idioma que queramos.
![2 cambiar idioma teclado](https://hackmd.io/_uploads/By6F7KoCbg.png)

3. Verificamos que la arquitectura UEFI es correcta.

![3 arquitectura uefi](https://hackmd.io/_uploads/SktTXFjCWx.png)

5. Comprobamos que tenemos conexión a internet.
![4 comprobar que tenemos conexión a internet](https://hackmd.io/_uploads/H1FJEFsCbe.png)

6. Sincronizamos el reloj del sistema.
   
![5 comprobar fecha](https://hackmd.io/_uploads/HkTMNKjC-x.png)

8. Comprobamos que discos tenemos para hacer posteriormente las particiones.
![6 comprobamos discos](https://hackmd.io/_uploads/BJnBNYoCWl.png)

9. Usaremos fdisk/dev/nuestro_disco para hacer las particiones UEFI (en nuestro caso, también se puedo con BOOT).
1.Pondremos el comando g para indicar que usaremos UEFI
2.Crearemos la partición 1 (será la partición para el boot de arranque)
3.Crearemos la partición 2 que usaremos como memoria swap y asignamos que sea swap
4.Crearemos la partición 3 que usaremos como partición raíz y asignamos que sea la raíz
5.Guardamos con w
![7.1](https://hackmd.io/_uploads/B11AStoCbe.png)
![7. configuración de discos (guardamos con w)](https://hackmd.io/_uploads/ryd8VtiCbe.png)

10. Formateamos los discos
![8. Formateamos particiones](https://hackmd.io/_uploads/H1CEqFsAZx.png)

11. Montamos el sistema de arhivos
![9 montamos sistema de archivos](https://hackmd.io/_uploads/S1rD5YsCbg.png)

12. Editamos el archivo /etc/pacman.d/mirror y ponemos arriba del todo los servidores mas cercanos a nosotros. (Es donde se harán nuestras actualizaciones

![10. Editamos archivo con nuestra región](https://hackmd.io/_uploads/ByOd9YoAZl.png)

13. Instalamos los paquetes más basicos
    
![11 instalar paquetes basicos](https://hackmd.io/_uploads/Sy86qFiCWx.png)

14. Añadimos paquetes imprescindibles:
- nano (para editor de texto)
- networkmanager (para gestión de red)
- amd-ucode o intel-ucode (para parches de seguridad de la cpu)
![13](https://hackmd.io/_uploads/rkk1iFsCbg.png)

15. Creamos archivo para indicar al sistema que particiones tiene que montar automáticamente al encender el sistema.
![14 indicaos al sistema que hace cada particion ](https://hackmd.io/_uploads/Syg6sYoR-l.png)

16. Indicamos la raíz del sistema.
    
![15. Cambiamos la raíz del sistema](https://hackmd.io/_uploads/SyHXpti0bl.png)

17. Cambiamos zona horaria y generamos archivo para que se sincronice cada vez que encendamos el pc con hwclock --systohc.
![16. cambiamos zona horaria y generamos archivo etc adjtime](https://hackmd.io/_uploads/BycDaKjCZg.png)

18. Editamos archivo locale.gen para asignar el idioma que queremos al encender el pc.
![17 editamos archivo locale.gen para seleccionar idioma](https://hackmd.io/_uploads/SJs1RKoAWg.png)

19. Creamos archivo locale.gen para asignar la distribucion del teclado que queremos al encender el pc.
![18. creamos archivo y ponemos idioma del teclado que queremos](https://hackmd.io/_uploads/Hyjf0Ko0Wl.png)

20. Creamos archivo indicando como se llamara el hostname.
![19 creamos archivo hostname](https://hackmd.io/_uploads/S1X_J5iAWe.png)

21. Generamos initramfs para indicar como cargar todo el sistema de arranque.
    
![20. generamos initramfs](https://hackmd.io/_uploads/Sk_tJ9sRWx.png)

22. Cambiamos contraseña a usuario root.
    
![21. creamos contraseña root](https://hackmd.io/_uploads/Skebgqi0bx.png)

24. Instalamos paquetes necesarios para instalar GRUB (que es el gestor de arranque que usaremos)
    
![22 instalamos paquetes necesarios](https://hackmd.io/_uploads/SJyMxcjA-l.png)

26. Instalamos GRUB
![23. instalamos grub en el disco](https://hackmd.io/_uploads/HkDdgci0-l.png)

27. Creamos el archivo de configuración para que funcione GRUB
![24. creamos archivo de configuracion](https://hackmd.io/_uploads/BJz6gcsAZx.png)

28. Desmontamos discos de forma segura.
![25. desmontamos discaos de forma segura](https://hackmd.io/_uploads/SJ59-coAbx.png)

29. Reiniciamos y quitamos imagen iso para iniciar en Archlinux.
![26](https://hackmd.io/_uploads/Hk8hZ5jCZg.png)
