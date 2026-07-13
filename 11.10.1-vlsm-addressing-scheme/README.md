**Packet Tracer - Diseñe e implemente un esquema** de direccionamiento VLSM

![Topologia](CISCO/CCNA%20CISCO/Curso%201de3%20CCNA1/CURSO%20CCNA1/PRACTICAS%20PORTAFOLIO/SUBNETTING-Labs/11.10.1-vlsm-addressing-scheme/img/topologia.png)


# Tabla de asignación de direcciones

| Dispositivo | Interfaz | Dirección IP     | Máscara de subred   | Puerta de enlace predeterminada |
| ----------- | -------- | ---------------- | ------------------- | ------------------------------- |
| HQ          | G0/0     | **172.19.67.1**  | **255.255.255.224** | N/A                             |
| HQ          | G0/1     | **172.19.67.33** | **255.255.255.224** | N/A                             |
| HQ          | S0/0/0   | **172.19.67.97** | **255.255.255.252** | N/A                             |
| Remote      | G0/0     | **172.19.67.65** | **255.255.255.240** | N/A                             |
| Remote      | G0/1     | **172.19.67.81** | **255.255.255.240** | N/A                             |
| Remote      | S0/0/0   | **172.19.67.98** | **255.255.255.252** | N/A                             |
| HQ-2        | VLAN 1   | **172.19.67.34** | **255.255.255.224** | **172.19.67.33**                |
| HQ-1        | VLAN 1   | **172.19.67.2**  | **255.255.255.224** | **172.19.67.1**                 |
| Remote 1    | VLAN 1   | **172.19.67.66** | **255.255.255.240** | **172.19.67.65**                |
| Remote 2    | VLAN 1   | **172.19.67.82** | **255.255.255.240** | **172.19.67.81**                |
| WS145       | NIC      | **172.19.67.62** | **255.255.255.224** | **172.19.67.33**                |
| WS116       | NIC      | **172.19.67.30** | **255.255.255.224** | **172.19.67.1**                 |
| WS203       | NIC      | **172.19.67.78** | **255.255.255.240** | **172.19.67.65**                |
| WS234       | NIC      | **172.19.67.94** | **255.255.255.240** | **172.19.67.81**                |

# Nota: 

# He tenido que intercambiar las direcciones IP por que packet tracert esperaba asi las direcciones de HQ1 y HQ2

# Objetivos

En este laboratorio diseñará un esquema de direccionamiento VLSM dado una dirección de red y requisitos de host. Configurará el direccionamiento en routers, switches y hosts de red.

· Diseñe un esquema de direccionamiento IP VLSM según los requisitos.

· Configure direccionamiento en dispositivos de red y hosts.

·         Verifique la conectividad IP.

·         Solucione problemas de conectividad según sea necesario.

# Antecedentes/Escenario

Se le ha pedido que diseñe, implemente y pruebe un esquema de direccionamiento para un cliente. El cliente le ha proporcionado la dirección de red adecuada para la red, la topología y los requisitos del host. Implementará y probará su diseño.

# Instrucciones

Su cliente le ha dado la dirección de red. Los requisitos de dirección de host son:

# Requisitos

Requisitos de host

| LAN           | Número de direcciones requeridas |
| ------------- | -------------------------------- |
| HQ-2          | 23                               |
| HQ-1          | 19                               |
| Remote 1      | 11                               |
| Remote 2      | 7                                |
| Hq1 to Remote | 2                                |

Requisitos de diseño

· Cree el diseño de direccionamiento. Siga las directrices proporcionadas en el plan de estudios con respecto al orden de las subredes.

· Las subredes deben ser contiguas. No debe haber espacio de direcciones no utilizado entre subredes.

· Proporcione la subred más eficiente posible para el enlace punto a punto entre los routers.

· Documente su diseño en una tabla como la siguiente.

| Descripción de la subred | Cantidad de hosts necesarios | Dirección de red/CIDR | Primera dirección de host utilizable | Dirección de difusión |
| ------------------------ | ---------------------------- | --------------------- | ------------------------------------ | --------------------- |
| HQ-1                     | 19                           | **172.19.67.0/27**    | **172.19.67.1**                      | **172.19.67.31**      |
| HQ-2                     | 23                           | **172.19.67.32/27**   | **172.19.67.33**                     | **172.19.67.63**      |
| Remote 1                 | 11                           | **172.19.67.64/28**   | **172.19.67.65**                     | **172.19.67.79**      |
| Remote 2                 | 7                            | **172.19.67.80/28**   | **172.19.67.81**                     | **172.19.67.95**      |
| HQ to Remote             | 2                            | **172.19.67.96/30**   | **172.19.67.97**                     | **172.19.67.99**      |

Requisitos de configuración

**Nota**: Configurará el direccionamiento en **todos los** dispositivos y hosts de la red.

·         Asigne las primeras direcciones IP utilizables en las subredes apropiadas a HQ para los dos enlaces LAN y el enlace WAN

·         Asigne las primeras direcciones IP utilizables en las subredes apropiadas a Remote para los dos enlaces de LAN. Asigne la última dirección IP utilizable para elenlace WAN .

· Asigne las segundas direcciones IP utilizables en las subredes apropiadas a los switches .

· La interfaz de administración del switch debe ser accesible desde los hosts de todas las LAN.

· Asigne las últimas direcciones IP utilizables en las subredes apropiadas a los hosts .

Si el diseño y la implementación de direcciones son correctos, todos los hosts y dispositivos deben ser accesibles a través de la red.

![HQ configuracion](HQ-config.png)

![Remote config](remote-config.png)



![Configuracion HQ-1](HQ-1-config.png)


![Remote 1 config](Remote-1-config.png)

![configuracion Remote2](remote2config.png)

![Configuracion de IP en los hosts](confi-hosts.png)

![Check 100%](CISCO/CCNA%20CISCO/Curso%201de3%20CCNA1/CURSO%20CCNA1/PRACTICAS%20PORTAFOLIO/SUBNETTING-Labs/11.10.1-vlsm-addressing-scheme/img/check.png)

