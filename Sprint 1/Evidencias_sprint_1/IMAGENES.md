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

No usamos «borrar el disco 100% REAL»

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

## punto 1.2 requerimiento de los Dos navegadores **Firefox y Chromium**
### chromium (version 158.0.8127.88 for Linux
<img width="959" height="539" alt="gedir_version" src="https://github.com/user-attachments/assets/64f98ff7-1de4-4384-9ecb-0fec77760ca0" />

**Codigo de instalacion:**
- sudo apt update
- sudo apt install -y chromium gedit
<img width="959" height="539" alt="instalacionde navegadores1eraparte" src="https://github.com/user-attachments/assets/81c1e191-1d23-4560-9fce-618ca081277f" />

**chromium funcionando**
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

### **2-VM de consola
## 2. VM de consola (g07-consola)

Instalamos Rocky Linux con particionado manual: `/`, swap, `/home` y `/var`. Disco de 25 GB y 2 CPU.

| Partición | Tamaño | Por qué |
|---|---|---|
| / | 5 GB | El sistema base, sin entorno gráfico |
| /var | 10 GB | Docker guarda sus imágenes en /var/lib/docker |
| swap | 1 GB | Mínimo de la guía |
| /home | 1 GB | Solo guardamos archivos pequeños |

Herramientas instaladas: make, rsync, curl, git y wget.

Comandos: `lsblk`, `df -h`, `cat /etc/fstab`, `make --version`, `rsync --version`, `curl --version`, `git --version`, `wget --version`

**[Captura 4: lsblk, df -h y cat /etc/fstab de g07-consola, con prompt y fecha]**

**[Captura 5: las cinco herramientas mostrando su versión]**
### **3-red
## 3. Red

Cada VM tiene dos adaptadores: el 1 en NAT (internet) y el 2 en red solo-anfitrión (para verse entre ellas).

Comandos: `ip a` en cada VM y `ping` en los dos sentidos.

**[Captura 6: ip a en las dos VMs, mostrando una dirección en cada interfaz]**

**[Captura 7: ping de la gráfica a la consola y de la consola a la gráfica]**

### **4-SSH 
## 4. SSH

Entramos por SSH desde la VM gráfica a la VM de consola.

Comando: `ssh usuario@direccion-de-la-consola`

**[Captura 8: la sesión SSH abierta, con el prompt de la consola]**
### **5-instantáneas
### **-video de 3 minutos 2 commits por integrante 
### **-el archivo codigo_sprint1.txt 



## 5. Instantáneas

Una por VM, llamada `instalacion-limpia`, tomada con la VM apagada y la instalación terminada.

**[Captura 9: pestaña de instantáneas de g07-grafica]**

**[Captura 10: pestaña de instantáneas de g07-consola]**

## Código del sprint

El docente publicó el código en el campus 48 horas antes del cierre. Lo guardamos en las dos VMs y lo mostramos en el video.

Comandos: `echo "XX00-AB12" > codigo_sprint1.txt`, `cat codigo_sprint1.txt` y `date`

## Video del sprint (3 minutos)

Pantalla continua y sin cortes. Cada integrante muestra su parte, dice su nombre y qué hizo en los primeros 10 segundos, y aparece su cara.
<img width="1600" height="720" alt="swapon --show Dos swaps activos" src="https://github.com/user-attachments/assets/58b19990-b8c1-4236-b46d-fc4cdcdb8d5f" />
<img width="1600" height="720" alt="uname -a identifica el sistema (kernel, nombre del equipo, arquitectura). free -m muestra la
memoria en megabytes. ip a lista las interfaces de red y sus direcciones" src="https://github.com/user-attachments/assets/f2bed7b2-6faa-4672-a6bb-ec3089cabd70" />
<img width="1600" height="720" alt="df -h cuánto espacio queda" src="https://github.com/user-attachments/assets/55f18789-807e-4560-9047-195556c69a0e" />
<img width="1600" height="720" alt="lsblk cómo quedó el disco" src="https://github.com/user-attachments/assets/f5ec7549-e2b9-42be-9497-28ffe163d334" />
### Sprint 1 Montaje
<img width="1600" height="720" alt="WhatsApp Image 2026-11-26 at 10 19 44 AM" src="https://github.com/user-attachments/assets/21c1ddfa-f08d-41fb-8edc-34aede710ce1" />
<img width="1600" height="720" alt="WhatsApp Image 2026-11-26 at 10 19 42 AM" src="https://github.com/user-attachments/assets/7cebb1ef-4023-4eb0-8f63-7ff76d76a4d8" />
<img width="1600" height="720" alt="WhatsApp Image 2026-11-26 at 10 19 40 AM" src="https://github.com/user-attachments/assets/47a4a874-1e28-4ecd-87cc-679a8b3641e3" />
<img width="1600" height="720" alt="WhatsApp Image 2026-11-26 at 10 19 46 AM" src="https://github.com/user-attachments/assets/abde14c8-9f78-4575-83f0-2c8d5cc04a7f" />
<img width="1600" height="720" alt="WhatsApp Image 2026-11-26 at 10 19 45 AM" src="https://github.com/user-attachments/assets/b4b86700-b218-4f51-a5a5-f394df842ddc" />


Aquí va el enlace del video de YouTube (público o no listado).

## **DISTRIBUCION DE TRABAJO POR INTEGRANTE DEL EQUIPO**

| Integrante | Qué hizo | Commits |
|---|---|---|
| BRAYAN | Creó las páginas del sitio y revisó la ficha | 2 |
| ANDRES | Instaló y configuró las dos VMs, la red, SSH y las instantáneas | 3 |
