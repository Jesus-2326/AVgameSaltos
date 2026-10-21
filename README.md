# AVgameSaltos

Videojuego tipo *runner* hecho con **pygame** que se controla con la mano usando visión artificial (**OpenCV** + **MediaPipe**).

## Archivos

| Archivo | Descripción |
|---|---|
| `main.py` | Versión del juego controlada con el teclado (barra espaciadora). |
| `juegoVision.py` | Versión del juego controlada con la cámara: cuenta los dedos levantados. |
| `contadorDedos.py` | Demo independiente que muestra en pantalla cuántos dedos detecta la cámara. |
| `handTrackingModule.py` | Módulo de detección de manos basado en MediaPipe. |

## Controles

**Teclado (`main.py`)**: `Espacio` para iniciar y para saltar.

**Cámara (`juegoVision.py`)**:
- Muestra **2 dedos** para iniciar o reiniciar la partida.
- Cierra el puño (**0 dedos**) para saltar.

## Requisitos

- Python 3.8
- Una webcam (para `juegoVision.py` y `contadorDedos.py`)

## Instalación

```bash
git clone https://github.com/Jesus-2326/AVgameSaltos.git
cd AVgameSaltos
python -m venv venv
# Windows
venv\Scripts\activate
# Linux / macOS
source venv/bin/activate
pip install -r requirements.txt
```

Si en el futuro el proyecto usa variables de entorno, copia la plantilla y rellénala:

```bash
cp .env.example .env
```

El archivo `.env` está en `.gitignore` y nunca se sube al repositorio.

## Uso

```bash
python main.py          # versión con teclado
python juegoVision.py   # versión con cámara
python contadorDedos.py # solo el contador de dedos
```
