# 🐍 Snake

Implementación del clásico Snake para la consola portátil ESPectro (ESP32-S3).

Parte del proyecto ESPectro — [base_espectro](https://github.com/bf-upc/base_espectro)

## Descripción

Controla una serpiente que debe comer alimentos para crecer y aumentar su puntuación. Cada vez que come, la velocidad aumenta ligeramente, haciendo el juego más desafiante.

La partida termina cuando la serpiente choca contra una pared o contra su propio cuerpo.

---

## Controles

| Control | Acción |
|----------|----------|
| Joystick eje X | Mover izquierda/derecha |
| Joystick eje Y | Mover arriba/abajo |
| Botón A | Iniciar partida |
| Botón B | Abrir Game Loader / salir de la partida |

---

## Puntuación

- +10 puntos por cada alimento consumido.
- La velocidad aumenta progresivamente.
- El récord se guarda automáticamente en la memoria flash (NVS).
- El historial de las últimas 20 partidas es visible desde el dashboard.

---

## Dashboard

Con la consola encendida, conéctate a la red WiFi **ESPectro** (contraseña: **gameloader**) y abre:

http://192.168.4.1

Desde el dashboard podrás:

- Consultar récords.
- Ver estadísticas de las últimas partidas.
- Visualizar el historial de puntuaciones.
- Instalar nuevas versiones del juego mediante OTA.

---

## Compilar y flashear

```bash
git clone https://github.com/bf-upc/base_espectro

cd base_espectro

pio run --target upload
```

---

## Requisitos

- PlatformIO
- Librería `lovyan03/LovyanGFX @ ^1.1.12`
- ESP32-S3 (RYMCU ESP32-S3 DevKitC-1)

---

## Binario compilado

El firmware generado se encuentra en:

```text
.pio/build/rymcu-esp32-s3-devkitc-1/firmware.bin
```

Este archivo puede cargarse directamente desde el Game Loader sin necesidad de conectar la consola por USB.

---

## Características técnicas

- Pantalla TFT ILI9488 320×480
- Control mediante joystick analógico
- Sonido generado por I2S
- Guardado persistente de récords mediante NVS
- Dashboard web integrado
- Actualización OTA mediante Game Loader
- WiFi Access Point integrado (ESPectro)

---

## Autores

**Noel Medina**  
**Bernat Figuerola**

UPC · 2026
