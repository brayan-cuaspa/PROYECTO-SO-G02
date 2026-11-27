<img width="856" height="385" alt="error en instalacion" src="https://github.com/user-attachments/assets/f7e1dabc-a69c-47b7-a7c7-625f0f7761b9" />
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

### **Los cinco puntos que aseguran la nota máxima para sprint 1  
### **1-VM gráfica
**primer punto VM gráfica (g02-grafica)**
**Iniciamos con la Instalación de Linux Mint XCFE version 22.3 edicion 64 bits "por economizar recursos en un PC de 8GB" con particionado manual (hasta este punto se cumple que no se borro el disco evitando des conteo de puntos) 
: dev/sda1 ext4 `, swap y `/home`. No usamos «borrar el disco».

| Partición | Tamaño | Por qué |
|---|---|---|
| / | 14 GB | El sistema y los programas, con margen para actualizar |
| swap | 2 GB | Igual a la RAM de la VM, por si falta memoria |
| /home | 9 GB | Los archivos de los usuarios, separados del sistema |

Dos navegadores y dos editores instalados: Firefox y Chromium, nano y gedit.

Comandos: `lsblk`, `df -h`, `cat /etc/fstab`

**[Captura 1: editor de particiones durante la instalación]**

**[Captura 2: lsblk, df -h y cat /etc/fstab, con el prompt usuario@g07-grafica y la salida de date]**

**[Captura 3: los dos navegadores y los dos editores abiertos]**

### **2-VM de consola
### **3-red 
### **4-SSH 
### **5-instantáneas
### **-video de 3 minutos 2 commits por integrante 
### **-el archivo codigo_sprint1.txt 



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

## 3. Red

Cada VM tiene dos adaptadores: el 1 en NAT (internet) y el 2 en red solo-anfitrión (para verse entre ellas).

Comandos: `ip a` en cada VM y `ping` en los dos sentidos.

**[Captura 6: ip a en las dos VMs, mostrando una dirección en cada interfaz]**

**[Captura 7: ping de la gráfica a la consola y de la consola a la gráfica]**

## 4. SSH

Entramos por SSH desde la VM gráfica a la VM de consola.

Comando: `ssh usuario@direccion-de-la-consola`

**[Captura 8: la sesión SSH abierta, con el prompt de la consola]**

## 5. Instantáneas

Una por VM, llamada `instalacion-limpia`, tomada con la VM apagada y la instalación terminada.

**[Captura 9: pestaña de instantáneas de g07-grafica]**

**[Captura 10: pestaña de instantáneas de g07-consola]**

## Código del sprint

El docente publicó el código en el campus 48 horas antes del cierre. Lo guardamos en las dos VMs y lo mostramos en el video.

Comandos: `echo "XX00-AB12" > codigo_sprint1.txt`, `cat codigo_sprint1.txt` y `date`

## Video del sprint (3 minutos)

Pantalla continua y sin cortes. Cada integrante muestra su parte, dice su nombre y qué hizo en los primeros 10 segundos, y aparece su cara.

Aquí va el enlace del video de YouTube (público o no listado).

## Lo que hizo cada integrante en este sprint

| Integrante | Qué hizo | Commits |
|---|---|---|
| Ana | Creó las páginas del sitio y revisó la ficha | 2 |
| Luis | Instaló y configuró las dos VMs, la red, SSH y las instantáneas | 3 |
