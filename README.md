# Guia de configuració de firewalls Fortinet

Repositori amb instruccions i exemples per configurar un firewall Fortinet en un entorn de laboratori. Els documents inclouen passos des de la interfície web i des de la línia d'ordres (CLI).

## Índex de documents

| Document | Descripció |
|---|---|
| [1. Primer accés al firewall](1_primer_acces_al_firewall.md) | Consulta de les interfícies, activació o desactivació de l'accés HTTP a `port1` i configuració inicial des del navegador. |
| [2. Ajustar les configuracions inicials](2_ajustar_configuracions_inicials.md) | Comprovació de la connectivitat, configuració inicial del port d'administració i ajustos bàsics del sistema. |
| [3. Configurar una IP estàtica al firewall](3_configurar_ip_estatica_firewall.md) | Canvi de `port1` de DHCP a una adreça IP estàtica, tant des de la interfície web com des de la CLI. |
| [Resum de comandes CLI](resum_comandes_cli.md) | Recull de les comandes utilitzades als documents de configuració. |

## Recomanacions

- Segueix els documents en ordre, especialment si és el primer accés al firewall.
- Adapta les adreces IP i altres valors d'exemple a la teva xarxa.
- Abans d'assignar una IP estàtica, comprova que no estigui en ús ni es pugui assignar a un altre dispositiu pel servidor DHCP.
