# Restablir un FortiGate 60F

## 1. Connexió per consola

1. Connecta un cable de consola RJ45 a USB al port `CONSOLE` del FortiGate 60F.
2. Obre un client de connexió sèrie, com ara PuTTY o Tera Term, i configura'l amb aquests paràmetres:

   | Paràmetre | Valor |
   | --- | --- |
   | Velocitat (baud rate) | `9600` |
   | Bits de dades | `8` |
   | Paritat | Cap |
   | Bits de parada | `1` |
   | Control de flux | Cap |

## 2. Comandes de restabliment

Inicia sessió amb un usuari administrador i tria una de les opcions següents segons què vulguis conservar:

### Restabliment complet (estàndard)

Esborra tota la configuració, els usuaris i els registres, però manté la versió actual del firmware (FortiOS).

```text
execute factoryreset
```

### Restabliment mantenint l'accés de xarxa

Esborra la configuració general, però conserva la configuració de les interfícies, les rutes estàtiques i els VDOM.

```text
execute factoryreset2
```

### Restabliment i apagada

Restableix els valors de fàbrica i apaga el dispositiu en lloc de reiniciar-lo.

```text
execute factoryreset-shutdown
```

> **Atenció:** aquestes comandes restableixen el dispositiu i poden esborrar-ne la configuració. Comprova que has triat l'opció adequada abans de continuar.

Quan aparegui el missatge de confirmació següent, escriu `y` i prem `Enter`:

```text
This operation will reset the system to factory default! Do you want to continue? (y/n)
```

El dispositiu es reiniciarà automàticament, excepte si has triat l'opció de restabliment i apagada.

## 3. Accés després del reinici

Un cop s'hagi iniciat de nou, el FortiGate 60F tindrà aquests valors per defecte:

- **Usuari:** `admin`
- **Contrasenya:** en blanc; prem `Enter` sense introduir-ne cap.
- **IP de gestió (port `internal1` / `lan`):** `192.168.1.99/24`

## Si has perdut la contrasenya d'administrador

Si no pots iniciar sessió a la consola perquè has perdut les credencials, pots utilitzar el botó físic `RESET`, situat en un petit orifici a la part posterior del dispositiu:

1. Desconnecta i torna a connectar el cable d'alimentació del FortiGate 60F.
2. Espera que aparegui el missatge d'inici de sessió (`login:`) a la consola.
3. Durant els primers 20–30 segons després de l'arrencada, prem el botó `RESET` amb un clip durant uns 5–10 segons, fins que aparegui a la consola el missatge següent:

   ```text
   System is resetting to factory default.
   ```

> **Nota:** segons la documentació oficial de Fortinet, a partir de FortiOS 7.4.1 la finestra per prémer el botó físic s'obre entre 80 i 90 segons després d'encendre el dispositiu. En altres versions, el moment pot ser diferent.

## Informació útil per resoldre problemes

Si el restabliment no funciona, comprova:

- Si pots iniciar sessió amb un usuari administrador o has perdut la contrasenya.
- Quina versió de FortiOS utilitza el dispositiu, si la coneixes.
