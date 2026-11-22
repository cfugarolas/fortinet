# Configurar IP estàtica en el nostre Firewall

Configurarem el nostre firwall amb una IP estàtica en lloc d'una IP donada pel nostre router de Internet.

## 1. Primer farem un exemple des de l'entorn web

Accedim al menú `Interfaces` i després doble clic `port1` de `Physical Interface`.

![Adaptadors de xarxa del Fortinet](img/captura15.5.jpg)

*Fem doble clic al `port1`.*

![Adaptadors de xarxa del Fortinet](img/captura16.jpg)

*Aquesta és la configuració actual per DHCP.*

En seleccionar `Manual`, el FortiGate proposa com a adreça IP estàtica la mateixa adreça que havia rebut per DHCP. Pots mantenir-la o introduir-ne una altra de lliure dins la mateixa subxarxa. Abans de mantenir-la, comprova que el servidor DHCP no la pugui assignar també a un altre dispositiu, per evitar conflictes d'adreces IP.

![Adaptadors de xarxa del Fortinet](img/captura17.jpg)

## 2. Ara ho farem per línia de comandes
