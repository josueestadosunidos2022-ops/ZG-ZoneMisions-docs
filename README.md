# ZG ZoneMisions 1.2.2

## Update / Actualización — 2026-10-17

Selected version / Versión seleccionada: **server 1.2.2 / client 1.2.2**. New file availability depends on CurseForge approval / La disponibilidad de los archivos nuevos depende de su aprobación en CurseForge.

See [changes, exact files and installation](UPDATES-2026-10-17.md) / Consulta [cambios, archivos e instalación](UPDATES-2026-10-17.md). Preserve the world and TOML files / Conserva mundo y TOML.

## Español

Misiones diarias de Minecraft 1.20.1 / Forge 47.x con progreso y premios validados por el servidor. El catálogo predeterminado contiene 200 misiones de minería, combate, comida, pesca, fabricación y exploración. Cada jugador recibe cinco tipos distintos al día. Hay cambios de misión antes de comenzar, bonificación para el primer jugador que termina el día y premios por racha.

### Instalación

En la misma página de CurseForge descarga **ZoneMisions Server 1.2.2** para el servidor y **ZoneMisions Client 1.2.2** para cada jugador. Ambos usan el protocolo de red 3 y deben coincidir en versión. El servidor requiere **ZoneCore 2.1.3+** y **ZoneCrates 2.0.6+**; el cliente no instala los JAR de servidor de esas dependencias. Retira versiones anteriores antes de reiniciar. ZoneRanks es opcional para gestionar permisos.

### Comandos y permisos

| Comando | Función | Permiso |
| --- | --- | --- |
| `/misiones` | Abre las misiones del día | `zonemisions.use` |
| `/misiones cambiar <1-5>` | Cambia una misión sin progreso | `zonemisions.use` |
| `/misiones admin ver <jugador>` | Consulta estado, racha y pago pendiente | `zonemisions.admin` |
| `/misiones admin reload` | Valida y recarga el TOML | `zonemisions.admin` |

La configuración se genera en `config/ZONEMODS/zonemisions/misiones.toml`. Lee la [guía del TOML](CONFIGURATION.md) y la [compatibilidad de la entrega](RELEASES.md). El progreso y las asignaciones se guardan en datos del jugador; la recarga no reemplaza las misiones ya asignadas ese día. Los pagos que no caben en la cartera quedan pendientes.

## English

Daily missions for Minecraft 1.20.1 / Forge 47.x. The server validates progress and rewards. The default catalog has 200 mining, combat, food, fishing, crafting, and exploration missions. Each player receives five different mission types each day. Unstarted missions can be rerolled; first finisher and streak rewards are configurable.

### Installation

Download **ZoneMisions Server 1.2.2** for the server and **ZoneMisions Client 1.2.2** for every player from the **same CurseForge project**. Both sides use network protocol 3 and must have matching versions. The server needs **ZoneCore 2.1.3+** and **ZoneCrates 2.0.6+**; clients do not install those server JARs. Remove older ZoneMisions versions before restarting. ZoneRanks is optional for permission management.

### Commands and permissions

| Command | Function | Permission |
| --- | --- | --- |
| `/misiones` | Open today's missions | `zonemisions.use` |
| `/misiones cambiar <1-5>` | Reroll an unstarted mission | `zonemisions.use` |
| `/misiones admin ver <player>` | Inspect status, streak, pending reward | `zonemisions.admin` |
| `/misiones admin reload` | Validate and reload TOML | `zonemisions.admin` |

The server generates `config/ZONEMODS/zonemisions/misiones.toml`. See the [TOML guide](CONFIGURATION.md) and [release compatibility](RELEASES.md). Reloading does not replace missions already assigned for today. Rewards that do not fit in the wallet remain pending.

## Ownership / Titularidad

© 2026 Elgochogms. All rights reserved for this release. This repository contains documentation and the project avatar only. It does not publish mod source, obfuscation mappings, server secrets, or production configuration. Previously released third party rights remain unaffected.

