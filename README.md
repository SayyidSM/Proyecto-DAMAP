# DAMAP
## Dispositivo de alerta para motociclistas basado en detección de peatones mediante visión por computadora

Proyecto desarrollado como Trabajo Terminal en la  
**Escuela Superior de Cómputo (ESCOM) — Instituto Politécnico Nacional**

**Programa académico:** Ingeniería en Inteligencia Artificial  
**Número de TT:** 2027-A056  
**Alumno:** Johann Sayyid Sánchez Martínez  
**Directores:** Emmanuelle Alvarado Jasso y Darwin Gutierrez Mejia  

---

## Descripción

DAMAP es un prototipo de asistencia para motociclistas que busca utilizar la cámara de un teléfono móvil para detectar peatones mediante técnicas de visión por computadora y generar una alerta sonora para el conductor.

El sistema está pensado para utilizar un teléfono colocado en el manillar de la motocicleta como dispositivo de captura y procesamiento. Cuando se detecte una persona y se cumplan los criterios establecidos para generar una advertencia, la aplicación emitirá una alerta de audio que podrá reproducirse mediante un intercomunicador Bluetooth conectado al teléfono.

El proyecto busca aprovechar hardware que el usuario ya posee, evitando modificaciones directas sobre la motocicleta y manteniendo el sistema lo más accesible posible.

---

## Objetivo general

Desarrollar un sistema capaz de alertar al motociclista sobre la presencia de un peatón utilizando la cámara de un teléfono celular montado en el manillar y un intercomunicador en el casco para emitir la advertencia.

---

## Alcance actual

| Funcionalidad | Estado |
|---|---|
| Aplicación móvil en Flutter | En desarrollo |
| Interfaz de usuario | En desarrollo |
| Captura mediante cámara | Pendiente de integración |
| Detección de personas | Pendiente |
| Integración de YOLO | Pendiente |
| Generación de alerta sonora | Pendiente |
| Salida de audio por Bluetooth | Pendiente |
| Pruebas de rendimiento | Pendiente |
| Documentación y bitácora | En desarrollo |

> El estado mostrado corresponde al desarrollo actual del prototipo y se actualizará conforme se validen nuevos componentes.

---

## Arquitectura general

El funcionamiento previsto del sistema es:

```text
Cámara del teléfono
        │
        ▼
Captura de imágenes / fotogramas
        │
        ▼
Modelo de detección YOLO
        │
        ▼
Detección de personas
        │
        ▼
Evaluación de criterios de alerta
        │
        ├── No se genera alerta ──► continuar procesamiento
        │
        ▼
Generación de alerta sonora
        │
        ▼
Sistema de audio del teléfono
        │
        ▼
Conexión Bluetooth
        │
        ▼
Intercomunicador del motociclista
