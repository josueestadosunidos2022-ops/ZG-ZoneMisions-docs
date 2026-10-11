# ZG ZoneMisions 1.2.1 — TOML / Configuración

Server file / Archivo del servidor: `config/ZONEMODS/zonemisions/misiones.toml`. It is created from the bundled 200 mission catalog when absent. Edit a backup and run `/misiones admin reload`; invalid values reject the reload and retain the previous catalog. / Se genera desde el catálogo de 200 misiones si falta. Edita una copia y ejecuta `/misiones admin reload`; un valor inválido rechaza la recarga y conserva el catálogo anterior.

| Key / Clave | Default | Meaning / Significado |
| --- | --- | --- |
| `zona_horaria` | `UTC` | Civil day zone / Zona del día civil; changing it can shift reset time. |
| `misiones_diarias` | `5` | Missions per player, 1–5 / Misiones por jugador, 1–5. |
| `pago_por_mision` | `200` | GochoCoins per completed mission / Pago por misión. |
| `bono_primer_usuario` | `300` | First daily finisher bonus / Bono al primero del día. |
| `recordatorio_minutos` | `15` | Reminder interval, 0–1440; 0 disables / Intervalo; 0 desactiva. |
| `cambios_diarios` | `1` | Rerolls per day, 0–5; only unstarted missions / Cambios diarios, solo misiones sin progreso. |
| `racha_dias_para_bono` | `7` | Consecutive full days, 0–365; 0 disables / Días seguidos, 0 desactiva. |
| `bono_racha` | `500` | Streak reward in GochoCoins / Premio por racha. |
| `mensaje_recordatorio` | Spanish text / texto español | Reminder / Recordatorio. |
| `mensaje_mision_completada` | Spanish text / texto español | `{mision}`, `{monedas}` placeholders / Variables. |
| `mensaje_limite_diario` | Spanish text / texto español | Daily limit message / Límite diario. |
| `mensaje_primer_usuario` | Spanish text / texto español | `{monedas}` placeholder / Variable. |
| `mensaje_racha` | Spanish text / texto español | `{dias}`, `{monedas}` placeholders / Variables. |

Payment keys support up to two decimal places and a maximum of 1,000,000 GochoCoins. / Las claves monetarias admiten hasta dos decimales y un máximo de 1.000.000 GochoCoins.

## Custom missions / Misiones personalizadas

Use `[[mision]]` for each entry. Fields / Campos: `id` (unique lowercase letters, digits, underscore; 1–64 chars), `nombre` (1–80), `tipo`, `objetivo`, `cantidad` (1–10,000). Valid `tipo` values: `minar`, `matar`, `comer`, `pescar`, `crear`, `explorar`. For `explorar`, `objetivo = "chunks"` and `cantidad` cannot exceed 512. Other targets use an existing `namespace:id` block, entity, or item as appropriate. The catalog needs at least as many distinct action types as `misiones_diarias` and no more than 1,000 entries. / Cada misión requiere ID único, nombre, tipo, objetivo y cantidad. El catálogo debe tener suficientes tipos distintos y hasta 1.000 entradas.

```toml
[[mision]]
id = "minar_piedra_custom"
nombre = "Mina 12 bloques de piedra"
tipo = "minar"
objetivo = "minecraft:stone"
cantidad = 12
```

The server stores player progress in NBT. Do not publish real player data or production configuration. / El servidor guarda el progreso en NBT. No publiques datos de jugadores ni configuraciones de producción.

