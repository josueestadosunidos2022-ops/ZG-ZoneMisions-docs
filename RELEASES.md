# ZG ZoneMisions — release compatibility / Compatibilidad

## 1.2.1 Beta — Minecraft 1.20.1 / Forge 47.x / Java 17

Both files belong to the same CurseForge project `1738055`. Install exactly one file per side: `zonemisions-server-1.2.1-protected.jar` on the dedicated server and `zonemisions-client-1.2.1-protected.jar` on each client. **Do not install both files on one side.** Network protocol: `3`; both sides must use 1.2.1. / Ambos archivos pertenecen al mismo proyecto. Instala solo el JAR correspondiente a cada lado y usa la misma versión en cliente y servidor.

Server dependencies / Dependencias del servidor: ZoneCore 2.1.3+, ZoneCrates 2.0.6+. Optional / Opcional: ZoneRanks for permissions. The client JAR only requires Forge/Minecraft; ZoneCore and ZoneCrates are server side for this pair. No full modpack compatibility claim has been made. / No se ha validado el modpack completo.

| File / Archivo | SHA-256 |
| --- | --- |
| Server / Servidor | `CC8CEFFA1D80022CD1FA7012FE172802A00456DA88310B201F3E9042982C53A8` |
| Client / Cliente | `6172ABCE417681CCFDE714FC57528BF4E9905FB0AD0A17B066A8BBF618FDA986` |

Build: both Gradle modules and six day-rule checks passed. Protected server JAR started on isolated Forge 47.4.10 with protected Core 2.1.3 and Crates 2.0.6; `/misiones admin reload` passed and shutdown was clean. Client graphical UI, two-player networking, real wallet transactions, complete modpack and production hosting remain untested. / Compilaron ambos módulos y pasaron seis comprobaciones; el servidor protegido arrancó y recargó el TOML. La interfaz gráfica, conexión real de dos jugadores, pagos, modpack completo y hosting siguen sin comprobarse.

Source and private mappings are not distributed. Bytecode obfuscation raises the cost of reading implementation but cannot make Java code impossible to decompile. / No se distribuyen fuentes ni mapas privados. La ofuscación dificulta la lectura, pero no impide por completo descompilar Java.

