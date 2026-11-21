## Primeres configuracions i habilitar l'accès HTTP en un fortinet de laboratori

### Veure els adapators de xarxa del fortinet

Executem la següent comanda per veure la configuració actual dels adaptadors de xarxa del nostre fortinet.

```bash
get system interface
```

![Adaptadors de xarxa del Fortinet](img/captura0.jpg)

*Exemple: adaptadors de xarxa configurats al Fortinet.*

### Activar http per poder utilizar els Fortinets de Laboratori

Mirem la configuració actual del port1

```bash
config system interface
edit port1
show
```

![Configuració de xarxa del port1](img/captura1.jpg)

*Exemple: configuració inicial del port1 del adaptador de xarxa configurats al Fortinet.*

### Activar l'accès http al nostre fortinet de laboratori

Afegim l'accés del http, mostrem la configuració i guardem els canvis.

```bash
append allowaccess http
show
end
```

![Afegir l'accès http](img/captura2.jpg)

*Exemple: Afegit l'accès, veure que apareix i guardar els canvis amb la comanda end.*

### Ara mirem s'accedir des de un navegador a l'ip del port1 per http

```bash
http://192.168.1.139
```

<img src="img/captura3.jpg" alt="Accés al Fortinet des del navegador" width="600">

```bash
admin
admin
```

*Exemple: Accès des de el navegador al nostre fortinet per http*

## Primeres configuracions des de l'entorn web


![Primera configuració](img/captura4.jpg)

*Fem "Begin"*

## Configurem el hostname del fortinet.


![Configuració hostname](img/captura5.jpg)

*Escullim el nom i fem OK*

## Triem l'estil del Dashboard

![Configuració hostname](img/captura6.jpg)

*Escullim "Optimal" que es el nou estil des de la versió 6.4*

## Vídeo introductori de la nova versió 7

![Configuració hostname](img/captura7.jpg)

*Escullim "Don't show again" i OK*

## Accedim a la configuració web del fortinet

![Configuració hostname](img/captura8.jpg)

*Exemple: Accès des de l'entorn web*
