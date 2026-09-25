# INSTITUTO TECNOLOGICO DE LAS AMERICAS

**Nombre:** Ezequiel Jiménez Rodríguez

**Matricula:** 2025-0863

**Carrera:** Seguridad Informática

**Materia:** Seguridad de Redes

**Maestro:** Jonathan Rondon

**Trabajo:** Practica I

**Fecha:** 25/09/2026

---

## I. Practica 1

El propósito de esta topología es poder demostrar como aplicar seguridad de redes en una infraestructura con diversos servidores, red de usuarios, conexión a la nube, y el uso de un fortigate como primera defensa.

Esto permite que podamos comprender el funcionamiento de una infraestructura y poder utilizarla como modelo a la hora de crear la nuestra en entornos profesionales y empresariales. Esperando el resultado esperado debido a las configuraciones exitosas previas.

Enlace del Video Aquí.

### I. Imagen de la topología:

*(Imagen de la topología de red: Nube "Net" conectada a Fortinet (port1), Fortinet (port2) conectado a un Switch (Gi0/0), el Switch conectado a una Linux PC (Gi0/1, VLAN 10, IP - DHCP), a un Web Server (Gi0/3, VLAN 15, 172.8.63.130) y a un DB Server (Gi0/2, VLAN 15, 172.8.63.131))*

---

## II. Direccionamiento IP

En este apartado estaré mostrando el direccionamiento IP, utilizado en la topología, se realizó un VLSM que tenga dígitos similares a mi matricula (2025-0863), y el direccionamiento es el siguiente:

| Nombre Red | Dispositivos | Primera Interfaz | Ultima Interfaz |
|---|---|---|---|
| Red Publica 192.8.63.0/24 | Fortigate(port1) - Cloud | 192.8.63.200 | 192.8.63.2 |
| VLAN 10 (Usuarios) 172.8.63.0/25 | Interfaz - Usuario | 172.8.63.1 | DHCP |
| VLAN 15 (Servidores) 172.8.63.128/28 | Server Web – Server DB | 172.8.63.130 | 172.8.63.131 |

---

## III. Imágenes en los dispositivos.

Aquí encontrara información de los componentes de la topología. Que fueron esenciales para poder comprobar y validar esta configuración con la cual contamos, para probar el funcionamiento del equipo Fortigate.

| Dispositivo | Nodo | Imagen |
|---|---|---|
| Fortigate | fortinet | Fortinet-FGT-7.0.9 |
| Switch | Cisco vIOS | Switch Viosl2-adventerprisek9-m.ssa.high_iron_20200929 |
| Linux PC | Docker.io | Pnetlab/linux-desktop:latest |
| DBServer | Docker.io | Pnetlab/mysql_server:latest |
| Web Server | Docker.io | Vulnerables/web-dvwa:latest |

---

## IV. Diagrama de la topología.

*(Diagrama de la topología de red: Nube "Net" conectada a Fortinet (port1), Fortinet (port2) conectado a un Switch (Gi0/0), el Switch conectado a una Linux PC (Gi0/1, VLAN 10, IP - DHCP), a un Web Server (Gi0/3, VLAN 15, 172.8.63.130) y a un DB Server (Gi0/2, VLAN 15, 172.8.63.131))*
