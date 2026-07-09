# Instrucciones
![[Topologia de red.png|TOPOLOGIA DE RED]]
## Parte 1: Subred de la red

### asignada Paso 1: Cree un esquema de subredes que cumpla con el número requerido de subredes y el número requerido de direcciones de alojamiento.

En este escenario, usted es un técnico de red asignado para instalar una nueva red para un cliente. Debe crear varias subredes en el espacio de la dirección de red 192.168.0.0/24 que cumplan los siguientes requisitos:

a. La primera subred es la red LAN-A. Necesita un mínimo de 50 direcciones IP de hosts.

b. La segunda subred es la red LAN-B. Necesita un mínimo de 40 direcciones IP de hosts.

c. También necesita al menos dos subredes adicionales no utilizadas para una futura expansión de la re d.

**Nota**: no se utilizarán máscaras de subred de longitud variable. Todas las máscaras de subred de los dispositivos tendrán la misma longitud.

d. Responda las siguientes preguntas para ayudar a crear un esquema de subredes que cumpla con los requisitos de red establecidos:

#### Preguntas:

¿Cuántas direcciones de host se necesitan en la subred requerida más grande?

**Se necesitan 64 direcciones para cubrir la porción de red que tiene 50 hosts, de las cuales solo 62 seran utiles y se necesitan 6 bits de la porcion de host para cubrirla

¿Cuál es la cantidad mínima de subredes requeridas?

**4

La red que se le asigna a la subred es 192.168.0.0 / 24. ¿Cómo se escribe la máscara de subred /24 en binario?

**11111111.11111111.11111111.00000000

e. La máscara de subred se compone de dos porciones, la porción de red y la porción host. Esto está representado en el binario por los unos y los ceros en la máscara de subred.

#### Preguntas:

En la máscara de red, ¿qué representan los unos?

**Los unos representan la porción de red.

En la máscara de red, ¿qué representan los números cero?

**Los ceros representan la porción de host

f. Para crear una subred en una red, los bits de la parte del host de la máscara de red original se cambian a bits de subred. La cantidad de bits de subred define la cantidad de subredes.

#### Preguntas:

Dadas cada una de las máscaras de subred posibles representadas en el siguiente formato binario, ¿cuántas subredes y cuántos hosts se crean en cada ejemplo?

**Sugerencia**: recuerde que la cantidad de bits de host (elevada al cuadrado) define la cantidad de hosts por subred (menos 2), y la cantidad de bits de subred (elevada al cuadrado) define la cantidad de subredes. Los bits de subred (indicados en negrita) son los bits que se tomaron prestados de la máscara de red original /24. /24 es la notación de prefijo de barra que corresponde a la máscara 255.255.255.0 en formato decimal punteado.

1) (/25) 11111111.11111111.11111111.**1**0000000

**2 subredes

**128 direcciones

**126 host útiles

Máscara de subred decimal con puntos equivalente:

Cantidad de subredes: ¿Número de anfitriones?

2) (/26) 11111111.11111111.11111111.**11**000000

	**4 subredes
	
	**64 direcciones
	
	**62 host útiles
	
	**255.255.255.192

Máscara de subred decimal con puntos equivalente:

Cantidad de subredes: ¿Número de anfitriones?

3) (/27) 11111111.11111111.11111111.**111**00000

**8 Subredes

**255.255.255.224

**30 hosts útiles

**32 direcciones

Máscara de subred decimal con puntos equivalente:

Cantidad de subredes: ¿Número de anfitriones?

4) (/28) 11111111.11111111.11111111.**1111**0000

**255.255.255.240

**16 Subredes

**14 host útiles

**16 direcciones

Máscara de subred decimal con puntos equivalente:

Cantidad de subredes: ¿Número de anfitriones?

5) (/29) 11111111.11111111.11111111.**11111**000

**6 direcciones host útiles

**8 direcciones

**32 subredes

**255.255.255.248

Máscara de subred decimal con puntos equivalente:

Cantidad de subredes: ¿Número de anfitriones?

6) (/30) 11111111.11111111.11111111.**111111**00


**64 subredes

**255.255.255.252

**2 direcciones útiles

**4 direcciones



Máscara de subred decimal con puntos equivalente:

Cantidad de subredes: ¿Número de anfitriones?

Considerando sus respuestas, ¿qué máscara de subred cumple la cantidad mínima de direcciones de host requeridas?

 (/26) 11111111.11111111.11111111.**11**000000

**4 subredes
	
**64 direcciones
	
**62 host útiles
	
**255.255.255.192

Considerando sus respuestas, ¿qué máscara de subred cumple la cantidad mínima de subredes requeridas?

**La máscara que cumple la cantidad mínima de subredes requeridas es /26.**  
  
Con /26 se toman prestados 2 bits de la porción de host:  
  
2^2 = 4 subredes  
  
Por tanto, cumple el requisito mínimo de 4 subredes.

Considerando sus respuestas, ¿qué máscara de subred cumple tanto la cantidad mínima de hosts como la cantidad mínima de subredes requeridas?

**La máscara que cumple tanto la cantidad mínima de hosts como la cantidad mínima de subredes requeridas es /26.**  
  
/26 permite:  
  
- 4 subredes  
- 64 direcciones por subred  
- 62 hosts útiles por subred  
  
Esto permite cubrir LAN-A con 50 hosts, LAN-B con 40 hosts y dos subredes futuras.

Una vez que haya determinado qué máscara de subred cumple todos los requisitos de red especificados, derivará cada subred a partir de la dirección de red original. Enumere las subredes del primero al último en la tabla. Recuerde que la primera subred es 192.168.0.0 con la máscara de subred adquirida recientemente.

|                     |         |                     |
| ------------------- | ------- | ------------------- |
| Dirección de subred | P       | Máscara de subred   |
| **192.168.0.0**     | **/26** | **255.255.255.192** |
| **192.168.0.64**    | **/26** | **255.255.255.192** |
| **192.168.0.128**   | **/26** | **255.255.255.192** |
| **192.168.0.192**   | **/26** | **255.255.255.192** |
### Paso 2: Rellene las direcciones IP que faltan en la tabla de direcciones

Asigne direcciones IP según los criterios siguientes: Utilice la configuración de red ISP como ejemplo.

a. Asigne la primera subred a LAN-A.

1) Utilice la primera dirección de host para la interfaz CustomerRouter conectada al switch LAN-A.

2) Utilice la segunda dirección de host para el switch LAN-A. Asegúrese de asignar una dirección de puerta de enlace predeterminada para el switch.

3) Utilice la última dirección de host para PC-A. Asegúrese de asignar una dirección de puerta de enlace predeterminada para el PC.

b. Asigne la segunda subred a LAN-B.

1) Utilice la primera dirección de host para la interfaz CustomerRouter conectada al switch LAN-B.

2) Utilice la segunda dirección de host para el switch LAN-B. Asegúrese de asignar una dirección de puerta de enlace predeterminada para el switch.

3) Utilice la última dirección de host para PC-B. Asegúrese de asignar una dirección de puerta de enlace predeterminada para el PC.

![[interfaces del Router.png|762]]

**Configuramos la interfaz del router con la primera ip disponible 192.168.0.1 

![[Configuración de Interfaces del router.png|811]]

![[Configuracion del Switch LAN-A.png|819]]

**Configuramos la puerta de enlace predeterminada y ponemos ip a la Vlan

**En el switch de LAN-B tambien configuramos la puerta de enlace predeterminada y la Vlan

![[Configuración del Switch Lan-B.png|938]]

**Por ultimo configuramos el Router con el nombre especificado en el enunciado y configuramos contraseñas...

![[Check Results.png|944]]

