# Botón de Pánico Inteligente (BPI-IA)

Prototipo en fase temprana de un botón de pánico que usa inteligencia artificial para clasificar el tipo de emergencia, canalizar la llamada al servicio correspondiente (911 → ambulancia, bomberos o policía), enviar la ubicación del usuario y dar instrucciones de primeros auxilios por voz mientras llega la ayuda.

Proyecto postulado al **Premio a la Innovación Mexicana 2026 (InnovaFest, edición Mérida)**, Categoría 6: Transformación digital e inteligencia artificial.

Autor: Abraham Moisés Gaytán Ramírez

## Estructura del repositorio

```
boton-de-panico-inteligente/
├── README.md                  ← este archivo
├── .gitignore
├── docs/
│   └── funcionamiento.md      ← flujo, tipos de emergencia y alcance del prototipo
└── prototipo-web/
    ├── index.html             ← versión estable (la que se presenta)
    └── desarrollo/
        ├── index.html         ← copia de trabajo para hacer modificaciones
        └── LEEME.md           ← cómo pasar cambios a la versión estable
```

## Cómo probarlo

1. Abre `prototipo-web/index.html` en Chrome o Edge (doble clic).
2. Escribe la emergencia o elige uno de los ejemplos.
3. Mantén presionado el botón **SOS** durante 1.5 segundos.
4. Revisa la clasificación, el servicio asignado, la ubicación y el reporte para el operador.
5. Pulsa **Leer en voz alta** para escuchar las instrucciones de primeros auxilios.

Fuera de claude.ai la clasificación usa el motor de reglas locales (palabras clave). Dentro de claude.ai usa IA (Claude).

## Qué está simulado en esta fase

- La llamada al 911 no es real; se registra en la bitácora.
- La ubicación se captura a mano (coordenadas de ejemplo: Plaza Grande, Mérida).
- No se usa el micrófono; la emergencia se describe por texto.

## Próximas fases

- GPS real del teléfono y reconocimiento de voz.
- Integración con el 911 y envío de SMS a contactos de confianza.
- Módulo de reconocimiento visual para búsqueda de personas (**Encuéntrame 72**).
