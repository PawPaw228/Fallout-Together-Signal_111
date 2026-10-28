# Signal 111 — Diario de desarrollo

*Actualizado el 28 de octubre de 2026*

[English](DEVELOPMENT-TRACKER-EN.md) · [Русский](DEVELOPMENT-TRACKER-RU.md) · [Español](DEVELOPMENT-TRACKER-ES.md) · [Português (Brasil)](DEVELOPMENT-TRACKER-PT-BR.md) · [简体中文](DEVELOPMENT-TRACKER-ZH-CN.md)

[Proyecto](../README.md) · [Hoja de ruta](ROADMAP.md)

## 28 de octubre — Coordenadas reales y prueba con dos PC

Conseguí leer la posición y la orientación cambiantes del jugador en un mundo de Fallout 4 cargado en un solo equipo HOST. Fue una prueba real dentro del juego. Más tarde registré 97 muestras de movimiento.

Después probé la transferencia entre **dos PC físicos**. El HOST envió las 97 muestras a través del servidor y el invitado recibió la misma secuencia y los seis valores de cada muestra sin diferencias.

**La transferencia pasó, pero la prueba completa falló.** El invitado tuvo un marcador de desconexión inválido y el HOST agotó posteriormente el tiempo de espera. Todavía no había dos personajes en un mundo compartido.

Reproduje y corregí un problema en la publicación del marcador de diagnóstico. La corrección pasó las pruebas sin ejecutar el juego; **todavía falta repetir la prueba real**.

También preparé un módulo de diagnóstico para crear, observar y eliminar un Actor local. Compila y supera las comprobaciones fuera del juego, pero **aún no se ha cargado en Fallout 4**.

## 26 de octubre — Preparativos para el mundo

Preparé la lectura protegida de las coordenadas y seguí trabajando en la seguridad de las partidas guardadas. En esa fecha solo había resultados de pruebas fuera del juego.

## 25 de octubre — Dos identidades de red

Dos clientes reales de Fallout 4 se conectaron al mismo servidor y recibieron identidades de red distintas. Ambos seguían en los menús.

## 24 de octubre — Dos conexiones

Verifiqué dos conexiones simultáneas y un acceso básico a los datos del jugador desde el menú.

## Próximos pasos

Comprobar el aislamiento de las partidas, validar una desconexión completa entre los dos PC y probar un Actor local antes de avanzar hacia personajes remotos.

**Todavía no hay una versión cooperativa jugable.**

[Changelog](../CHANGELOG.md) · [Tareas](https://github.com/PawPaw228/Fallout-Together-Signal_111/issues)
