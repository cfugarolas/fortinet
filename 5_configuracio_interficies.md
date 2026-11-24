# Configuració de les interfícies

Aquesta guia recollirà els passos per consultar i configurar les interfícies de xarxa del Fortinet.

## Configurarem el `port2` amb la configuració del primer proveïdor Internet del nostre laboratori des de l'entorn web.

![Adaptadors de xarxa del Fortinet](img/5/captura24.jpg)

*Dins l'apartat `Interfaces` del nostre Fortinet fem doble clic sobre el `port2` per accedir a la configuració de la interfície.*

Un cop oberta la configuració del `port2`, hi indiquem un nom descriptiu al camp `Alias`, seleccionem `WAN` al camp `Role` i hi configurem l'adreça IP corresponent al primer proveïdor d'Internet del laboratori. 

Evitem donar accesos administratius aquestes interfícies donat que seria una mala pràctica.

![Adaptadors de xarxa del Fortinet](img/5/captura25.jpg)

*Per guardar els canvis fem clic `OK`*

![Adaptadors de xarxa del Fortinet](img/5/captura26.jpg)

*Així quedaria un cop configurat*
