# ¿Qué es MBR y GPT?

### MBR (Registro de Arranque Maestro)
####
#### Es el primer sector del disco duro, y su función es inicializar el proceso de arranque del sistema. Es un sector de 512 bytes, que contiene la información necesaria para cargar un sistema operativo.
####
### Sus Características
#### Contiene una tabla de particiones que definen cada una de las particiones primarias.
#### Incluye una firma de MBR (0x55AA) de 2 bytes.
#### Es el primer sector del disco duro en dispositivos no particionados.
#### Es el primer sector de una partición individual en dispositivos particionados.
####
### ¿Cómo funciona?
#### El firmware de la BIOS carga el MBR cuando se inicia el proceso de arranque. El MBR escanea la lista de entradas de particiones primarias en las tablas de particiones y busca una que esté marcada. Después carga y ejecuta el VBR para esa partición, lo que permite arrancar el S.O.
#
### GPT (La Tabla de Particiones GUID)
####
#### Es un estándar para la configuración de las tablas de particiones en medios de almacenamiento, especialmente discos duros físicos. Fue desarrollado por Intel como parte del estándar Extensible Firmware Interface (EFI) para reemplazar el viejo Master Boot Record (MBR).
### Sus Características
#### No tiene límites de tamaño de disco a diferencia de MBR que si.
#### Puede crear más de 4 particiones primarias.
#### No necesita particiones primarias, cada partición tiene un GUID único y un nombre.
#### Es compatible con UEFI, lo que permite más flexibilidad en la inicialización de sistemas operativos.
#
### Diferencias entre MBR y GPT
####
| TIPO | MBR | GPT |
|----|-----|-----|
| Tamaño de Disco | 2TB | 256TB |
| Particiones Primarias | 4 | 128 |
| Esquema de idenfiticación | Direcciones físicas | Identificadores únicos globales |
| Compatibilidad S.O | Windows 7 / Windows 95/98 / Windows XP 32 bits / Windows 2000 / Windows 2003 23 bits | Windows 8, 8.1 de 64 bits, 10, 11 |
| Velocidad | Lenta | Rápida |
| Eficiencia | Menor | Mayor |
| Hardware | Antiguo | Moderno |