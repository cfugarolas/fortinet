# Primer accès al nostre Firewall

Aquesta guia mostra com consultar les interfícies de xarxa, habilitar l'accés HTTP a `port1` i completar la configuració inicial des del navegador.

## 1. Consultar les interfícies de xarxa

Per consultar totes les interfícies i la configuració definida a FortiGate, executa:

```bash
get system interface
```
![Adaptadors de xarxa del Fortinet](img/1/captura0.jpg)

*Exemple dels adaptadors de xarxa configurats al Fortinet.*

Per obtenir únicament informació sobre les interfícies físiques, executa:

```bash
get system interface physical
```
![Adaptadors de xarxa del Fortinet](img/1/captura0.5.jpg)
---

## 2. Habilitar l'accés HTTP a `port1`

Entra a la configuració de les interfícies i consulta la configuració actual de `port1`:

```bash
config system interface
edit port1
show
```

Un cop situat dins la configuració de `port1`, afegeix HTTP als mètodes d'accés permesos i desa els canvis:

```bash
append allowaccess http
show
end
```

![Configuració de xarxa del port1](img/1/captura1.jpg)

*Configuració inicial de `port1`.*

![Accés HTTP afegit](img/1/captura2.jpg)

*L'accés HTTP apareix a la configuració. La comanda `end` desa els canvis i surt del menú.*

### Treure l'accés HTTP

Per desactivar l'accés HTTP de `port1`, executa:

```bash
config system interface
edit port1
unselect allowaccess http
show
end
```

---

## 3. Accedir a la interfície web

Obre l'adreça IP de `port1` en un navegador. Canvia l'adreça de l'exemple si el teu Fortinet en té una de diferent:

```text
http://192.168.1.139
```

![Accés al Fortinet des del navegador](img/1/captura3.jpg)

*Pàgina d'accés al Fortinet des del navegador.*

Introdueix les credencials de l'exemple:

```text
admin
admin
```

## 4. Completar la configuració inicial

Segueix els passos que es mostren a la interfície web:

1. A la pantalla inicial, fes clic a «Begin».

   ![Primera configuració](img/1/captura4.jpg)

2. Tria el nom d'amfitrió del Fortinet i fes clic a «OK».

   ![Configuració del nom d'amfitrió](img/1/captura5.jpg)

3. Selecciona l'estil «Optimal» per al tauler. Aquest estil està disponible a partir de la versió 6.4.

   ![Selecció de l'estil del tauler](img/1/captura6.jpg)

4. Si no vols tornar a veure el vídeo introductori, selecciona «Don't show again» i fes clic a «OK».

   ![Vídeo introductori de la versió 7](img/1/captura7.jpg)

Quan acabis, veuràs la interfície web del Fortinet:

![Interfície web del Fortinet](img/1/captura8.jpg)

---

## Resum de les comandes

Consultar les interfícies:

```bash
get system interface
```

Consultar la configuració del `port1`:

```bash
config system interface
edit port1
show
```

Habilitar HTTP al `port1`:

```bash
config system interface
edit port1
append allowaccess http
show
end
```

Accedir a la interfície web (canvia la IP per la del `port1`):

```text
http://192.168.1.139
```

Treure l'accès HTTP de `port1`:

```bash
config system interface
edit port1
unselect allowaccess http
show
end
```
