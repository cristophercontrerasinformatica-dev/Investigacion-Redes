# Fundamentos de redes
## Router, Switch y Hub
### Cómo funcionan y por qué importan en el desarrollo de software

- Las aplicaciones no funcionan aisladas, sino dentro de una red.
- Cuando usamos una web, una API o una base de datos, la información viaja entre distintos equipos.
- Entender lo básico de redes ayuda a detectar problemas y comprender mejor cómo se conectan los sistemas.

---

# ¿Qué es cada dispositivo?

## Router
- Conecta redes diferentes.
- Decide por dónde deben viajar los datos.
- Ejemplo: conecta tu red de casa con Internet.

## Switch
- Conecta equipos dentro de una misma red local.
- Envía la información solo al dispositivo correcto.
- Ejemplo: conecta computadores y servidores en una oficina.

## Hub
- También conecta equipos, pero de forma muy básica.
- Repite la información a todos los puertos.
- Hoy casi no se usa porque es poco eficiente.

---

# ¿Cómo funciona realmente?
## Cómo viaja la información

- Cada dispositivo en la red tiene una **IP**, que identifica a dónde debe llegar la información.
- Dentro de la red local también existe la **MAC**, que identifica físicamente a cada equipo.
- El **switch** usa la MAC para entregar los datos al equipo correcto.
- El **router** usa la IP para enviar datos hacia otra red.
- El **broadcast** ocurre cuando un mensaje se envía a todos los equipos de la red local.

---

# Relación con desarrollo
## ¿Qué tiene que ver esto con programar?

- Cuando una app hace una petición a una API, esa información viaja por la red.
- Si el servidor está fuera de la red local, la petición pasa por un router.
- Dentro de un data center, los switches conectan servidores, bases de datos y otros equipos.
- Por eso, un problema de red puede parecer un error de frontend o backend, aunque no lo sea.

### Ejemplo
Usuario → navegador/app → router → Internet → servidor/API → respuesta

---

# Caso práctico real
## La aplicación está en producción, pero los usuarios no pueden entrar

### ¿Podría ser problema del router?
- Sí, si el tráfico no está saliendo o llegando correctamente entre redes.

### ¿Podría ser problema del switch?
- Sí, si dentro de la red local los equipos no se comunican bien.

### ¿Cómo distinguirlo?
- Si falla la salida a Internet o a otra red: revisar router.
- Si falla la comunicación entre equipos de la misma red: revisar switch.
- Si todo parece conectado, recién pensar que puede ser problema del código.

---

# Analogía simple
## Una comparación fácil de entender

- **Router:** como una oficina de correos que decide a qué ciudad enviar cada paquete.
- **Switch:** como una recepcionista que sabe exactamente a qué oficina entregar un sobre.
- **Hub:** como una persona que grita el mensaje a todos, aunque solo era para uno.

---

# Bonus
## Load balancer y cloud

### Load balancer
- Recibe las solicitudes de los usuarios.
- Las reparte entre varios servidores.
- Evita sobrecargar un solo equipo.

### Cloud (AWS, Azure, etc.)
- En la nube también existen redes, rutas y balanceadores.
- La diferencia es que muchas veces son virtuales, no físicos.
- La lógica sigue siendo la misma: conectar, dirigir y distribuir tráfico.

---

# Conclusión

- El **router** conecta redes distintas.
- El **switch** organiza la comunicación dentro de una red local.
- El **hub** repite la señal a todos, por eso hoy está obsoleto.
- Entender estos dispositivos ayuda a comprender mejor cómo funcionan las aplicaciones y a detectar fallas reales.
