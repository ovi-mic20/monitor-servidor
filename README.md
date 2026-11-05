Responder preguntas del trabajo:

1. ¿Por qué la temperatura suele aparecer como “No disponibleˮ en Windows? Prueben abrir la terminal
como administrador y comparen.

Porque Windows no expone la temperatura de la CPU. Si no sale como que no esta disponible si se
abre en la terminal normal del powershell, pero si se abre como administrador en el powershell se puede mostrar.

2. ¿Por qué el script de PowerShell nunca debe incluir datos que vengan del usuario?

Porque shell_exec() ejecuta comandos en el servidor. Y si el script se armara con datos de un formulario o de la URL, alguien podría inyectar comandos y ejecutar cualquier cosa en la máquina.

3. ¿Qué riesgo tiene dejar /api/metrics sin autenticación en un servidor real?

Que cualquiera podria observar información interna del servidor, el nombre, la version de php,
uso de disco, cpu y memoria. Y eso podria dejar vulnerable de que atacantes puedan saber que información 
tocar para acceder.

4. Con polling cada 5 segundos, ¿cuántos pedidos por minuto recibe el servidor si hay 50 personas
mirando?

Y si hay cincuenta personas mirando con polling serian una astimación de 12 minutos por pedidos.

5. Si una app solo necesita la temperatura, ¿qué datos recibe de más al llamar a /api/metrics?

Todo lo demás campos; memory, cpu, uso de disco, version de php, es decir, recibe 8 bloques de datos para usar uno solo. Eso se llama over-fetching, y es justo lo que GraphQL.