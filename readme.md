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



