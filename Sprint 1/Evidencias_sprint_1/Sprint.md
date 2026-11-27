# **SPRINT 1 DESARROLLO**
## **Los cinco puntos que aseguran la nota máxima para sprint 1  
### ** 1-VM gráfica **
**primer punto VM gráfica (g02-grafica)**
Iniciamos con la Instalación de Linux Mint XCFE version 22.3 edicion 64 bits "por economizar recursos en un PC de 8GB" con particionado manual (hasta este punto se cumple que no se borro el disco evitando des conteo de puntos)
## Propiedades de la maquina virtual ya montada :)

<img width="959" height="539" alt="caracteristicas de la maquina virtual" src="https://github.com/user-attachments/assets/b745fa09-c53d-4146-a454-018adc5ddc3f" />

### MAPEO/PARTICION

|ASIGNACION DE MEMORIA|DIR|
|---------|-----------|
|dev/sda1-| ext4      |
|dev2/sda2| swap      |
|dev3/sda3| home      |

**No usamos «borrar el disco 100% REAL**

<img width="959" height="539" alt="Captura de pantalla 2026-11-26 170339" src="https://github.com/user-attachments/assets/3015851a-2249-4174-a847-9a7b4c9d17da" />

## comprobante el disco todavía sigue ahí después de haber instalado Linux con todo y particiones
<img width="959" height="539" alt="comprobante_de_que_el_disco_quedo_bien_instalado" src="https://github.com/user-attachments/assets/911a5c80-78e7-45b9-bdae-0a452e986820" />

## Mapeo de particiones 

| Partición | Tamaño | Por qué |
|---|---|---|
| ext4 | 15 GB | es por que es la raíz va montado el SO y el software a descargar y el instalado |
| swap | 3 GB | por si la RAM falla por alcanzar su máxima capacidad accede a la virtual |
| home | 3.9 GB | Los archivos de los usuarios documentos, descargas etc separados del sistema |

### Tabla de asignación de recursos
<img width="959" height="539" alt="TABLA_DE_PARTICION" src="https://github.com/user-attachments/assets/98f02729-4c4e-4074-ac3c-89a4dc72896d" />

## Punto 1.1 Captura de pantalla los cuatro codigos

|Codigo|para que sirve|
|------|--------------|
|hostname|sirve para saber el nombre del host en este caso go2-grafica|
|lsblk|sirve para ver las particiones en este caso las tres que se crearon previamente|
|df -h|sirve para ver el espacio|
|cat /etc/fstab| sirve para ver el batch|

## Captura de pantalla de los cuatro codigos

<img width="959" height="539" alt="todos los comandos ejecutados" src="https://github.com/user-attachments/assets/6975a199-b708-40ba-a993-1679c373acc0" />

## Punto 1.2 Requerimiento de los Dos navegadores **Firefox y Chromium**
### Chromium (Version 158.0.8127.88 for Linux)
### Gedit (Version 46.2)

<img width="959" height="539" alt="gedir_version" src="https://github.com/user-attachments/assets/64f98ff7-1de4-4384-9ecb-0fec77760ca0" />

**Codigo de instalacion:**
- sudo apt update
- sudo apt install -y chromium gedit
<img width="959" height="539" alt="instalacionde navegadores1eraparte" src="https://github.com/user-attachments/assets/81c1e191-1d23-4560-9fce-618ca081277f" />

### **Chromium funcionando**

<img width="959" height="539" alt="chrorium" src="https://github.com/user-attachments/assets/2700efa6-953e-4c09-8cc1-40589cc3d9d1" />

### Curiosidad del dia 1
- Linux Mint ya viene con Mozilla Firefox instalado asi que solo se procedera
a mostrar junto al Chromium funcionando

## Punto 1.3 requerimiento de los Dos editores **gedit y nano**
**Codigo de instalacion:**
- sudo apt update
- sudo apt install -y chromium gedit

### Curiosidad del dia 2 
- Linux Mint ya viene con Nano instalado asi que solo se procedera
a mostrar junto al gedit funcionando
- se utiliza el mismo codigo que el chromium debido a que se instala los dos
en paquete

## Captura de pantalla de confirmación paso completado con extito
- se procede a demostrar que el Chromium el Gedit junto con
Mozilla Firefox y Nano estan funcionando normalmente en Linux
mint montado en virtual box :)

<img width="959" height="539" alt="los dos navegadores y dos editores" src="https://github.com/user-attachments/assets/a0f5d687-d82c-4841-abbc-2eba0231ab38" />

## Captura de la maquina virtual apagada tomado una instantanea

<img width="959" height="539" alt="image" src="https://github.com/user-attachments/assets/1ca88c91-15f1-4409-933a-692ec88c4019" />

# **Punto 2 VM de consola
## VM de consola (g02-consola)

### Iniciamos con la Instalación de Rocky Linux version 9 XCFE "por que era mas liviana la version DVD pesaba 16GB mucho para un equipo" con particionado manual

### Propiedades de la maquina virtual

<img width="959" height="539" alt="caracteristicas de maquin consola" src="https://github.com/user-attachments/assets/0f792ae3-b352-4997-b4bb-7d95b65fb479" />

### Captura asignación de recursos
- (Estan planteados obligatoriamente en el pdf **proyecto final** para evitar desconteo de puntos)

<img width="959" height="539" alt="rlinux" src="https://github.com/user-attachments/assets/00a39cc0-476b-4955-9149-0fccebdaa161" />

### Punto a destacar
- se opto por instalación tipo consola de Rocky Linux a diferencia de Linux Mint para poner en practica lo aprendido en la clase Docker en consola de Google

<img width="959" height="539" alt="instalacion sin grafica" src="https://github.com/user-attachments/assets/825a57de-32ab-4dbc-8b9f-e1cf5e835f89" />

### MAPEO/PARTICION

|ASIGNACION DE MEMORIA|DIR|
|---------|-----------|
|dev1/sda1| ext4      |
|dev2/sda2| swap      |
|dev3/sda3| home      |
|dev4/sda4| var       |

### Evidencia de que se usa la partición manual

<img width="959" height="539" alt="particionmanual" src="https://github.com/user-attachments/assets/0407e412-c946-4963-ba7b-5e4a5c56f8ec" />

### Tabla de particion

| Partición | Tamaño | Por qué |
|---|---|---|
| / | 15 GB | El sistema base, sin entorno gráfico |
| /var | 3 GB | Docker guarda sus imágenes en /var/lib/docker |
| swap | 3 GB | Mínimo de la guía |
| /home | 4 GB | Solo guardamos archivos pequeños |

### Captura de particiones confirmadas :)

<img width="959" height="539" alt="distrubucion de memoria yameoa" src="https://github.com/user-attachments/assets/093eafcb-778c-46a9-b7c9-9dc9a6dcf93a" />

### Instalación ya finalizada

<img width="959" height="539" alt="image" src="https://github.com/user-attachments/assets/f6e80c83-56c2-4d77-8c60-78ad9f5a3cfd" />

### Maquina funcionando

<img width="959" height="539" alt="image" src="https://github.com/user-attachments/assets/d3d0c774-35b1-49f0-abcb-46850c8a7891" />

# Ejecución de los 4 códigos para g02-consola

|Codigo|para que sirve|
|------|--------------|
|hostname|sirve para saber el nombre del host en este caso go2-consola|
|lsblk|sirve para ver las particiones en este caso las cuatro que se crearon previamente|
|df -h|sirve para ver el espacio en disco|
|cat /etc/fstab| sirve para ver el batch|

### Código 1 host (g02-consola)
<img width="959" height="539" alt="image" src="https://github.com/user-attachments/assets/a53b8965-0bef-4ad8-ab8c-c1d99c06af74" />

### Codigo 2 lsblk (particion correcta de los /, /home, swam, /var)

<img width="959" height="539" alt="image" src="https://github.com/user-attachments/assets/7311b388-942f-455f-80ca-222dd13f8f3b" />

### Código 3 df -h (espacio de disco)

<img width="959" height="539" alt="image" src="https://github.com/user-attachments/assets/521d96f3-e97b-4e3c-a15d-8820a7b99127" />

### Código 4 cat /etc/fstab (para ver el contenido de archivo)

<img width="959" height="539" alt="image" src="https://github.com/user-attachments/assets/4e1d30b9-2507-4fc5-bfa7-8b309e774034" />

# las 5 Herramientas instaladas
## Requerido obligatoriamente en el PDF

|HERRAMIENTA|PARA QUE SIRVE|VERSION|
|---|---|---|
|MAKE|para automatizar codigo que se repite verifica **GNU MAKE**|4.3|
|RSYNC|para copiar y sincronizar archivos o carpetas de manera eficiente|3.2.7 protocol v31|
|CURL|para transferir datos desde o hacia un servidor usando múltiples protocolos (HTTP, HTTPS, FTP etc)|7.76.1 red hat|
|GIT|para guardar el historial de cambios del código fuente y colaborar en proyectos de software|2.52.0|
|WGET|para descargar archivos desde internet de forma no interactiva con soporte para descargas recursivas (bajar sitios completos o múltiples carpetas)|V3|


### Código de instalación para las 5 herramientas
"sudo dnf install -y make rsync curl git wget"

### Primera herramienta make (version 4,3) 

<img width="959" height="539" alt="image" src="https://github.com/user-attachments/assets/c0f5aba9-9406-4998-81e6-b0ba39f052e9" />

### Segunda herramienta rsync (version 3.2.7 protocol v31)

<img width="959" height="539" alt="image" src="https://github.com/user-attachments/assets/034e9ef2-ec6b-4b3a-a541-92eb5670c765" />

### Tercera herramienta curl (versión 7.76.1)

<img width="959" height="539" alt="image" src="https://github.com/user-attachments/assets/9d2ed1ba-ff15-4dc0-b474-2b0ce439edec" />

### cuarta herramienta git (versión 2.52.0)

<img width="959" height="539" alt="image" src="https://github.com/user-attachments/assets/aab6e296-1a7f-4e91-9dd5-0a59e6f5e609" />

### Quinta herramienta wget (version V3)

<img width="959" height="539" alt="image" src="https://github.com/user-attachments/assets/9d677901-c3b9-42d4-8335-8c45276910ce" />

### Captura (instantánea **instalacion limpia**) maquina apagada
- **Es aquí en donde se finaliza el punto numero 2 instalación de la consola esta imagen simboliza que todo se cumplio correctamente para asi asegurar la nota maxima :)** 

<img width="959" height="539" alt="image" src="https://github.com/user-attachments/assets/c136b106-154b-473a-8fe5-8b4fd1e61c5e" />

# **Punto numero 3 configuracion de Red **
- sabemos por medio del PDF **proyecto final** que VirtualBox usa NAT así que nuestras dos maquinas tanto la grafica como la de consola no interactuaran entre ellas a través de este tipo de red por lo que se procede a hacer la instalación de adaptadores para hacer posible una comunicación entre las maquinas virtuales se va a realizar en forma ordenada para una clara comprencion del lector ╰(*°▽°*)╯  

## Configuracion inicial de VMs

### Estado inicial red maquina grafica

<img width="959" height="539" alt="image" src="https://github.com/user-attachments/assets/178dc06d-2977-43b2-b372-6638c01a31c7" />

### Estado inicial red maquina consola
<img width="959" height="539" alt="image" src="https://github.com/user-attachments/assets/e4844a43-3037-4d9b-abd5-fe4a50584cfe" />

## Comandos de uso para este proceso

|Codigo|Para que sirve|ejemplo|
|---|---|---|
|IP a|sirve para conocer la IP de nuestra maquina virtual asi como la NAT|192.168.56.XX|
|ping -c 4 (IP)|sirve para enviar los paquetes de datos entre las maquinas y si llegan con exito o se pierden|4 enviados, perdidos, recibidos|

## Ejecución de los comandos para conocer la IP en ambas maquinas virtuales

### Comandos: (ip a) en grafica 

<img width="959" height="539" alt="image" src="https://github.com/user-attachments/assets/37f4c08f-1744-4c0c-884b-b87d37555898" />

### Comandos: (ip a) en consola
<img width="959" height="539" alt="image" src="https://github.com/user-attachments/assets/9dfb1d21-8c2e-48f3-9b5a-e11f52806419" />

## DATO IMPORTANTE
- Es muy necesario anotar la IP del anfitrión en cada maquina para posteriormente completar el segundo código por ejemplo **ping -c 4 192.168.56.XX (maquina grafica)** **ping -c 4 192.168.56.XX (maquina consola)** de lo contario no podrá establecer una comunicación  

## Ejecución de los comandos para conectar enviar Datos en ambas Maquinas Virtuales

### Ping maquina grafica enviado con éxito :)

<img width="959" height="539" alt="image" src="https://github.com/user-attachments/assets/cef821fe-46a2-4990-9759-d7fb83281b13" />

### Ping maquina consola enviado con éxito :)

<img width="959" height="539" alt="image" src="https://github.com/user-attachments/assets/50e7217c-b8ae-41fa-9610-11cd70183fd0" />

# **4-SSH** 
## "SECURE SHELL controlar de manera remota la consola" El objetivo principal de este punto es saber si estamos haciendo una conexión entre ambas maquinas por SSH para controlar la consola de Rocky Linux por medio de Linux Mint la maquina virtual de la grafica.

## Comandos a utilizar para completar este punto
|Codigo|para que sirve|ejemplo|
|---|---|---|
|SSH usuario@direccion-de-la-consola|sirve para conectar la consola a la grafica a través de los servicios SSH|pepitoperez@192.168.56.xx|
|sudo systemctl status sshd|sirve para saber si el servicio esta activo de lo contario el codigo anterior no funcionara|it's rinning|

## El servicio esta activo

<img width="959" height="539" alt="image" src="https://github.com/user-attachments/assets/b687791f-4d7a-40ac-a737-37eed7718b77" />

### Captura la sesión SSH abierta con el prompt de la consola
-con esto queda evidente que lo hicimos correctamente los pasos ╰(*°▽°*)╯

<img width="959" height="539" alt="image" src="https://github.com/user-attachments/assets/7ae55ba1-a7f2-4128-9ec9-fc89407f88b2" />

# **Paso FINAL 100% DEL SPRINT 1 (instantáneas)** 
### Instantanea maquina virtual grafica Linux Mint

<img width="959" height="539" alt="image" src="https://github.com/user-attachments/assets/53bfcc7c-2261-484a-b897-f8d33e212040" />

### Instantánea maquina virtual grafica Rocky Linux 

<img width="959" height="539" alt="image" src="https://github.com/user-attachments/assets/991d3d87-1ed5-4841-bb78-333ea0765c56" />

### **-video de 3 minutos 2 commits por integrante 
- LINK: [https://youtu.be/95-AqUwfWZQ]

## **codigo archivo codigo_sprint1.txt** 
### Este Codigo fue enviado el dia miercoles es muy necesario para obtener la nota maxima sin el es Sprint 1 queda descalificado 

## Recursos importantes para completar el paso

|recurso|para que sirve|
|---|---|
|NN02-DT7E|codigo subido al campus correspondiente al grupo 2 para que la entrega del sprint 1 sea valida|
|echo "SU CODIGO" > codigo_sprint1.txt|comando para crear el archivo txt|

## Codigo en linux mint 

<img width="959" height="539" alt="image" src="https://github.com/user-attachments/assets/76f252f4-576a-44d5-98fb-982e7a50184a" />

## Codigo en rocky linux

<img width="959" height="539" alt="image" src="https://github.com/user-attachments/assets/5e695eaa-8361-404c-91b1-f17de76543d3" />

## las dos maquinas funcionando correctamente

<img width="959" height="539" alt="image" src="https://github.com/user-attachments/assets/c5565e92-af5b-448b-a0fe-244e1ead4e1f" />

## **DISTRIBUCION DE TRABAJO POR INTEGRANTE DEL EQUIPO**

| Integrante | Qué hizo | Commits |
|---|---|---|
| BRAYAN | instale las maquinas virtuales y añadí comits al repositorio | 22 |
| ANDRES | Instaló y configuró las dos VMs, la red, SSH y las instantáneas | 3 |
