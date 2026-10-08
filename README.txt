TIMBRE ESCOLAR LA MILAGROSA

Sistema digital para activar el timbre de la Institución Educativa
La Milagrosa mediante una página web y un ESP32-C3.

ARCHIVOS

- index.html: página web para GitHub Pages.
- timbre_esp32_c3.ino: programa para el ESP32-C3.

CONEXIÓN

Celular/PC
    ↓
GitHub Pages
    ↓
Internet / MQTT
    ↓
ESP32-C3
    ↓
Relé
    ↓
Timbre

IMPORTANTE

1. En el programa del ESP32-C3 cambie:
   WIFI_SSID
   WIFI_PASSWORD

2. El tema MQTT debe ser exactamente:
   la_milagrosa/timbre/alcama51/2026

3. Instale en Arduino IDE la biblioteca:
   PubSubClient

4. En este ejemplo se usa un broker MQTT público para pruebas.
   Para una instalación definitiva se recomienda utilizar un broker
   con usuario, contraseña y un tema privado.

5. El botón "TOCAR TIMBRE AHORA" envía la duración en segundos.
   Ejemplo: 5 significa activar el relé durante 5 segundos.

NOTA SOBRE LOS HORARIOS

Los horarios que aparecen en la página se guardan actualmente en
el navegador mediante localStorage. La programación automática
independiente de que la página esté abierta requiere enviar y
guardar los horarios en el ESP32-C3 (por ejemplo, usando el DS3231).
