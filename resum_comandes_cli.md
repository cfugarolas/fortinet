# Resum de les comandes CLI

Aquest document recull les comandes CLI dels documents del repositori. S'hi aniran afegint els resums dels altres documents.

## [Primer accés al firewall](primer_acces_al_firewall.md)

Consultar les interfícies de xarxa:

```bash
get system interface
```

Consultar la configuració de `port1`:

```bash
config system interface
edit port1
show
```

Habilitar l'accés HTTP a `port1`:

```bash
config system interface
edit port1
append allowaccess http
show
end
```

Treure l'accés HTTP de `port1`:

```bash
config system interface
edit port1
unselect allowaccess http
show
end
```

## [Ajustar les configuracions inicials](ajustar_configuracions_inicials.md)

Comprovar la connectivitat a Internet des del Fortinet:

```bash
exec ping 8.8.8.8
```
