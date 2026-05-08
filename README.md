# Instalar-Archlinux
## Guia oficial
https://wiki.archlinux.org/title/Installation_guide_(Espa%C3%B1ol)

## Instalación
1. Nada más iniciar con la iso tendremos este terminal.
<img width="1276" height="796" alt="1" src="https://github.com/user-attachments/assets/d2e9ad06-a238-470c-a13d-279c857a0a59" />

2. Asignamos la distribución del teclado en el idioma que queramos.
<img width="1276" height="797" alt="2 cambiar idioma teclado" src="https://github.com/user-attachments/assets/00a8a7ec-5bf5-49bd-8b03-d6de85a1aed3" />

3. Verificamos que la arquitectura UEFI es correcta.

<img width="453" height="57" alt="3 arquitectura uefi" src="https://github.com/user-attachments/assets/5abd21c9-7d05-4f51-9f17-0a7859d1ef12" />

5. Comprobamos que tenemos conexión a internet.
<img width="842" height="446" alt="4 comprvar que tenemos conexion a internet" src="https://github.com/user-attachments/assets/77754dca-9ea1-4934-99b0-2c6229474ad7" />

6. Sincronizamos el reloj del sistema.
   
<img width="447" height="141" alt="5 comprovar fecha" src="https://github.com/user-attachments/assets/3cbbdcf4-b3e5-48c9-8355-c9769966f3c2" />

8. Comprobamos que discos tenemos para hacer posteriormente las particiones.
<img width="529" height="208" alt="6 comprovamos discos" src="https://github.com/user-attachments/assets/051a7456-5532-4308-93a4-bc5b01fcc257" />


9. Usaremos fdisk/dev/nuestro_disco para hacer las particiones UEFI (en nuestro caso, también se puedo con BOOT).
1.Pondremos el comando g para indicar que usaremos UEFI
2.Crearemos la partición 1 (será la partición para el boot de arranque)
3.Crearemos la partición 2 que usaremos como memoria swap y asignamos que sea swap
4.Crearemos la partición 3 que usaremos como partición raíz y asignamos que sea la raíz
5.Guardamos con w
<img width="1206" height="206" alt="7 1" src="https://github.com/user-attachments/assets/501ee3f5-7a25-4237-b7eb-357faafe34a4" />
<img width="801" height="785" alt="7  configuracion de discos (guardamos con w)" src="https://github.com/user-attachments/assets/c0d0c64f-1372-4aef-b4eb-e2580182160e" />

10. Formateamos los discos
    
<img width="644" height="625" alt="8  formateamos particiones" src="https://github.com/user-attachments/assets/52587c1a-2843-4671-8987-a5d9c8b73cb2" />

11. Montamos el sistema de arhivos
    
<img width="571" height="377" alt="9 montamos sistema de archivos" src="https://github.com/user-attachments/assets/4ec54a76-764b-4795-9b5f-dd99418ad5d7" />

12. Editamos el archivo /etc/pacman.d/mirror y ponemos arriba del todo los servidores mas cercanos a nosotros. (Es donde se harán nuestras actualizaciones

<img width="1279" height="798" alt="10  editamos archivo con nuestra region" src="https://github.com/user-attachments/assets/b50b1cfa-e794-4820-b2fd-40b2a80739e4" />

13. Instalamos los paquetes más basicos
    
<img width="482" height="15" alt="11 instalar packetes basicos" src="https://github.com/user-attachments/assets/a626090a-a400-43f3-9b38-74e4ffaed37d" />

14. Añadimos paquetes imprescindibles:
- nano (para editor de texto)
- networkmanager (para gestión de red)
- amd-ucode o intel-ucode (para parches de seguridad de la cpu)
  
<img width="508" height="20" alt="13" src="https://github.com/user-attachments/assets/0d4e2f83-3a82-41c5-8641-035fa6bdf161" />

15. Creamos archivo para indicar al sistema que particiones tiene que montar automáticamente al encender el sistema.
<img width="405" height="17" alt="14 indicaos al sistema que hace cada particion " src="https://github.com/user-attachments/assets/865815e5-c54c-454f-b47a-36ec60fe6dad" />

16. Indicamos la raíz del sistema.
    
<img width="275" height="22" alt="15  cambiamos la raiz del sistema" src="https://github.com/user-attachments/assets/362056bd-11a9-4f19-b4c8-61d72c8d9766" />

17. Cambiamos zona horaria y generamos archivo para que se sincronice cada vez que encendamos el pc con hwclock --systohc.
<img width="620" height="70" alt="16  cambamos zona horaria y generamos archivo etc adjtime" src="https://github.com/user-attachments/assets/77874fa2-837c-43d0-9c49-bc1f1976323f" />

18. Editamos archivo locale.gen para asignar el idioma que queremos al encender el pc.
<img width="1278" height="795" alt="17 editamos archivo locale gen para seleccionar idioma" src="https://github.com/user-attachments/assets/8b487863-532a-4065-988f-5bbabd709192" />

19. Creamos archivo locale.gen para asignar la distribucion del teclado que queremos al encender el pc.
<img width="1276" height="797" alt="18  creamos archivo y ponemos idoma del teclado que queremos" src="https://github.com/user-attachments/assets/0e7dc62b-9f9c-4092-a940-0a81c87cd1db" />

20. Creamos archivo indicando como se llamara el hostname.
<img width="1274" height="795" alt="19 creamos archivo hostname" src="https://github.com/user-attachments/assets/8c4bda97-3db4-4079-aaf5-2502d45779e6" />

21. Generamos initramfs para indicar como cargar todo el sistema de arranque.
    
<img width="608" height="346" alt="20  generamos initramfs" src="https://github.com/user-attachments/assets/ad473d90-e3f9-4b1b-9fc2-09edbbbafccf" />

22. Cambiamos contraseña a usuario root.
    
<img width="309" height="83" alt="21  creamos contraseña root" src="https://github.com/user-attachments/assets/53e69b5c-af11-4794-8074-eee0f5dbb5ae" />

24. Instalamos paquetes necesarios para instalar GRUB (que es el gestor de arranque que usaremos)
    
<img width="360" height="17" alt="22 instalamos paquetes necesarios" src="https://github.com/user-attachments/assets/b783a1d3-10f2-40ef-8c06-12cd33127fea" />

26. Instalamos GRUB
<img width="750" height="16" alt="23  instalamos grub en el disco" src="https://github.com/user-attachments/assets/2165a31c-404a-4694-bea8-a215725d4291" />

27. Creamos el archivo de configuración para que funcione GRUB
<img width="612" height="158" alt="24  creamos archivo de configuracion" src="https://github.com/user-attachments/assets/1a4619a4-5af1-4707-a440-df3040c211f7" />

28. Desmontamos discos de forma segura.
<img width="255" height="21" alt="25  desmontamos discaos de forma segura" src="https://github.com/user-attachments/assets/f2e67778-5885-4bba-8cf9-05885189f6e6" />

29. Reiniciamos y quitamos imagen iso para iniciar en Archlinux.
<img width="1274" height="797" alt="26" src="https://github.com/user-attachments/assets/ddd92b80-8d23-4df5-9b4a-7c282ae9f37c" />

