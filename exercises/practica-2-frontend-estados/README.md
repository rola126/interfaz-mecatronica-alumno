# Práctica 2 — Frontend leyendo estados

## Objetivo

Completar `frontend/js/ui.js` para que la interfaz traduzca correctamente el JSON que
llega del backend a texto y colores en pantalla — sin construir todavía ningún comando (eso es la Práctica 3).

## Requisitos previos

Práctica 1 completada. Haber leído `shared/json/protocolo.md`.

## Contexto

Con la plantilla del alumno, el backend **ya funciona completo**: puedes ver los datos reales llegando en el
panel "JSON RECIBIDO" de la pantalla, y puedes forzar distintas condiciones con
`POST /api/simulation/scenario` (ver `README.md`). Lo que falta es que `ui.js` sepa **pintar**
esos datos — ahora mismo, la pantalla se queda en sus valores de arranque sin importar lo que diga el JSON recibido.

Vas a completar tres funciones de `ui.js`: `renderMotor()`, `renderProcess()` y `renderAlarms()`. El propio
archivo trae un comentario `TODO` extenso justo antes de esas funciones con todos los detalles.

## Cómo probar cada actividad

1. Levanta el backend: `cd backend && npm install && npm start`.
2. Abre `http://localhost:3000`.
3. Fuerza el escenario que corresponda con `curl` (ver cada actividad).
4. Espera 2 segundos (el sondeo periódico refresca la pantalla solo) y verifica los criterios de aceptación.

No necesitas completar `app.js` ni `api.js` (Práctica 3) para esta práctica: los botones no van a funcionar
todavía, pero el sondeo automático de estado sí, y es suficiente para probar todo lo de aquí.

## Actividades

| Actividad | Qué se practica |
|---|---|
| [Actividad 1](actividad-1.md) | `running` → ENCENDIDO / DETENIDO |
| [Actividad 2](actividad-2.md) | `connected: false` → SIN COMUNICACIÓN |
| [Actividad 3](actividad-3.md) | `severity: WARNING` → advertencia visible |
| [Actividad 4](actividad-4.md) | `severity: CRITICAL` → alarma crítica visible |
