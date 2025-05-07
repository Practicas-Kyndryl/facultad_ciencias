# facultad_ciencias
## Topología de la Facultad de Ciencias 

![](images/image.png)

## Descripcion de la topología

En esta topología tendremos varios tipod de usuarios bien diferenciados. 

# Administración

El personal de administración tendrá acceso a los servidores de base de datos pero no podrá acceder al servidor FTP ni al resto de departamentos. Además podrá acceder a la zona desmilitarizada (DMZ) e internet.

# Laboratorios

Los usuarios ubicados en los laboratorios podrán acceder al servidor FTP, a la DMZ y a internet, pero no tendrán acceso a los servidores de base de datos ni al resto de departamentos.

# Alumnos

Los alumnos tendrán acceso inalámbrico a la red y podrán acceder al servidor FTP, a la DMZ y a internet, pero no podrán acceder a los servidores de base de datos ni al resto de departamentos.

## Dispositivos

La topología se basa en un topología "leafs and spines" con un Border Leaf y una zona DMZ con dos firewall.

Tenemos tres leafs que conectarán a los dispositivos finales. Los leafs se conectan de forma redundante con dos spines (switches de capa 3) que a su vez se conectan a dos border leaf para evitar tener un punto único de falla. Esta topología es muy útil y que es redundante y fácilmente escalable (se añaden leafs sin modificar el core de la topología).

La DMZ (o zona desmilitarizada) actúa como una nueva capa de seguridad impidiendo que atacantes externos puedan entrar dentro de la organización. Tiene la estructura clásica con dos firewall, uno más cerca de la LAN, con reglas mucho más estrictas para la entrada dentro de la organización, y otro más cerca de internet con una políticas de seguridad menos restrictivas. El monitoreo de la DMZ nos ayudará a descubrir ataques y estar preparados ante intentos de acceso no autorizados.

Por último tendremos un router que conecta con el resto de departamentos de la Facultad.


