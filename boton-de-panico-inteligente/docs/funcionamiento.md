# Funcionamiento del prototipo

## Flujo de una alerta

1. **Activación**: el usuario mantiene presionado el botón SOS 1.5 segundos. El tiempo de espera evita alertas por toques accidentales. Se puede cancelar como falsa alarma.
2. **Captura**: se toman la descripción de la emergencia y la ubicación (latitud, longitud y referencia).
3. **Clasificación**:
   - *IA*: un modelo de lenguaje recibe la descripción y responde un JSON con `tipo`, `confianza` y `resumen`.
   - *Respaldo local*: si la IA no está disponible, un clasificador de palabras clave asigna el tipo.
4. **Canalización**: en México el 911 es el número único; el sistema indica a qué corporación debe canalizarse el caso.
5. **Ubicación y reporte**: se genera un enlace de Google Maps y un reporte de texto listo para el operador.
6. **Primeros auxilios**: se muestran y leen en voz alta (síntesis de voz del navegador, español de México) los pasos según el tipo.
7. **Bitácora**: cada evento queda registrado con su tiempo desde la activación.

## Tipos de emergencia

| Tipo | Canalización |
|---|---|
| Persona inconsciente | Ambulancia · Cruz Roja / SAMU |
| Herida con sangrado | Ambulancia · Cruz Roja / SAMU |
| Atragantamiento | Ambulancia · Cruz Roja / SAMU |
| Incendio | Bomberos · Protección Civil |
| Accidente vial | Ambulancia + Policía Vial |
| Riesgo a la seguridad | Policía · Seguridad Pública |
| Emergencia no especificada | Operador 911 · triage |

## Tecnología

- Una sola página HTML, CSS y JavaScript, sin dependencias de instalación.
- Clasificación con IA mediante Claude (cuando se ejecuta en claude.ai).
- Web Speech API (`speechSynthesis`) para las instrucciones por voz.
- Tema claro y oscuro automático; diseño adaptable a teléfono.

## Aviso

Las instrucciones de primeros auxilios son una guía básica y no sustituyen las indicaciones del operador de 911 ni la atención profesional.
