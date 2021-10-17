# Recogida de información II (Nmap)

## Práctica del módulo de **Seguridad y Alta Disponibilidad**

- Alumno: Tomás Castejón Acosta
- Curso: 2ºB - A.S.I.R.
- IES Punta del Verde

![alt text](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSWigCAVznxugU0L4DmAYOqciDJxhISSJR63g&usqp=CAU)


Haremos una busqueda de información sobre esta herramienta que permite explorar vulnerabilidades, se utiliza para identificar que dispositivos se están ejecutando en sus sistemas, 
descubrir los hosts diponibles, encontrar puertos abiertos y poder detectar riesgos de seguridad. En el fondo se trata de una herramienta de escanea de puertos, lo que hace es enviar paquetes sin procesar a los puertos del sistema para así poder comprobar si existen puertos abiertos, cerrados o filtrados.

Recordamos que **partimos de 2 máquinas virtuales**, una vulnerable como es **metasploitable** y la otra **kali linux** en la cual tenemos ya instalado Nmap y desde ahi es desde donde haremos los escaneos correspondientes, también es **importante recordar que hemos puesto las dos máquinas en Red Nat** configurando la red dentro de virtual box en ambas máquinas.


## 1. Analizar un sistema con nombre de host y la dirección IP ##

La herramienta Nmap ofrece varios métodos para analizar un sistema. En este ejemplo, estoy realizando una exploración utilizando el nombre de host como server2.mimaquina.com para averiguar todos los puertos abiertos, servicios y la dirección MAC del sistema.

### Escaneo mediante el nombre de host ###

![alt text](https://github.com/Tomkas33/Recogida-de-informaci-n-II-Nmap-/blob/main/Captura.PNG)

### Escaneo mediante direcciones IP ###

![alt text](https://github.com/Tomkas33/Recogida-de-informaci-n-II-Nmap-/blob/main/Captura2.PNG)

## 2. Escanear utilizando la opción “-v” ##

### Este comando con la opción "-v" está dando una información más detallada acerca de la máquina remota ###

![alt text](https://github.com/Tomkas33/Recogida-de-informaci-n-II-Nmap-/blob/main/Captura3.PNG)

## 3. Escanear varios hosts ##

### Se puede escanear múltiples hosts simplemente escribiendo sus direcciones IP o nombres de host con Nmap ###

![alt text](https://github.com/Tomkas33/Recogida-de-informaci-n-II-Nmap-/blob/main/Captura4.PNG)

## 4. Analizar todo una subred ##

### Se puede escanear toda una subred o rango de direcciones IP con Nmap proporcionando el comodín * con él ###


![alt text](https://github.com/Tomkas33/Recogida-de-informaci-n-II-Nmap-/blob/main/Captura5.PNG)

## 5. Analizar varios servidores utilizando el último octeto de la dirección IP ##

### Puede llevar a cabo exploraciones en varias direcciones IP simplemente especificando el último octeto de la dirección IP. Por ejemplo, aquí se realiza un análisis de las direcciones IP 192.168.0.101, 192.168.0.102 y 192.168.0.103. ###


![alt text](https://github.com/Tomkas33/Recogida-de-informaci-n-II-Nmap-/blob/main/Captura6.PNG)

## 6. Analizar la lista de los ejércitos de un archivo ##

### Si  tienes más hosts para escanear y todos los detalles de acogida están escritos en un archivo, se puede hacer que nmap directamente lea ese archivo y realice el análisis. Vamos a ver cómo hacerlo.

### Crear un archivo de texto llamado "nmaptest.txt" y definir todas las direcciones IP o nombre de host del servidor que desea hacer una exploración. ###


![alt text](https://github.com/Tomkas33/Recogida-de-informaci-n-II-Nmap-/blob/main/Captura7.PNG)

### A continuación, se ejecuta el siguiente comando con la opción "iL" con el comando nmap para escanear todas las direcciones IP que aparece en el archivo ###

![alt text](https://github.com/Tomkas33/Recogida-de-informaci-n-II-Nmap-/blob/main/Captura8.PNG)

## 7. Escanear un rango de direcciones IP ##

### Se puede especificar un rango de direcciones IP en el desempeño de escaneo con Nmap. ###


![alt text](https://github.com/Tomkas33/Recogida-de-informaci-n-II-Nmap-/blob/main/Captura9.PNG)

## 8. Escaneado por Red Excluyendo hosts remotos ##

### Se puede excluir algunos hosts al realizar una exploración de red completa o cuando se escanea con los comodines con la opción de "–exclude" ###


![alt text](https://github.com/Tomkas33/Recogida-de-informaci-n-II-Nmap-/blob/main/Captura10.PNG)

## 9. Información Scan OS y Traceroute ##

### Con Nmap, se puede detectar qué sistema operativo y la versión que está ejecutando en el host remoto. Para habilitar la detección de sistema operativo y versión, la exploración de la escritura y la Ruta de seguimiento, podemos usar la opción "-A" con NMAP. ###


![alt text](https://github.com/Tomkas33/Recogida-de-informaci-n-II-Nmap-/blob/main/Captura11.PNG)

## 10. Activar la Detección de OS con Nmap ##

### Hay que itilizar la opción "-O" y "-osscan-guess" también ayuda a descubrir la información del sistema operativo. ###


![alt text](https://github.com/Tomkas33/Recogida-de-informaci-n-II-Nmap-/blob/main/Captura12.PNG)

## 11. Escanear un anfitrión para Detectar Firewall ##

### El siguiente comando realizará una búsqueda en un host remoto para detectar si los filtros de paquetes o Firewall se utiliza por el anfitrión. ###


![alt text](https://github.com/Tomkas33/Recogida-de-informaci-n-II-Nmap-/blob/main/Captura13.PNG)

## 12. Escanear un anfitrión para comprobar su protección por Firewall ##

### Para escanear un host si está protegido por ningún software de filtrado de paquetes o cortafuegos. ###


![alt text](https://github.com/Tomkas33/Recogida-de-informaci-n-II-Nmap-/blob/main/Captura14.PNG)

## 13. Averigüe que redes están activas (vivas) ##

### Con la ayuda de la opción "-sP" simplemente podemos comprobar qué hosts están vivos y en red, con esta opción se salta nmap detección de puertos y otras cosas. ###


![alt text](https://github.com/Tomkas33/Recogida-de-informaci-n-II-Nmap-/blob/main/Captura15.PNG)

## 14. Realizar un análisis rápido ##

### Se realiza un análisis rápido con la opción "-F" para las exploraciones para los puertos que figuran en los archivos de nmap-services y deja todos los demás puertos. ###


![alt text](https://github.com/Tomkas33/Recogida-de-informaci-n-II-Nmap-/blob/main/Captura16.PNG)

## 15. Encontrar versión de Nmap ##

### Se puede encontrar la versión de Nmap está ejecutando en su máquina con la opción "-V" ###


![alt text](https://github.com/Tomkas33/Recogida-de-informaci-n-II-Nmap-/blob/main/Captura17.PNG)

## 16. Puertos de escaneo de forma consecutiva ##

### Se utiliza el indicador "-r" para hacerlo de forma no aleatoria ###


![alt text](https://github.com/Tomkas33/Recogida-de-informaci-n-II-Nmap-/blob/main/Captura18.PNG)

## 17. Interfaces de impresión de host y Rutas ##

### Se puede encontrar la interfaz y ruta de información de host con nmap con la opción "-iflist" ###


![alt text](https://github.com/Tomkas33/Recogida-de-informaci-n-II-Nmap-/blob/main/Captura19.PNG)

## 18. Analizar en busca de puerto específico ##

### Hay varias opciones para descubrir los puertos en la máquina remota con Nmap. Se puede especificar el puerto que desee nmap para escanear con la opción "-p", por defecto escanea nmap sólo puertos TCP. ###


![alt text](https://github.com/Tomkas33/Recogida-de-informaci-n-II-Nmap-/blob/main/Captura20.PNG)



Finalmente partimos de la base de dos máquinas virtuales, Kali Linux con Nmap instalado por defecto y Metasploitable, máquina virtual vulnerable, desde Virtualbox configuramos la red de estas máquinas para que puedan verse en el apartado red, veamos el siguiente vídeo con varias ejemplos.


## 18. EJEMPLOS DE USO NMAP ##











