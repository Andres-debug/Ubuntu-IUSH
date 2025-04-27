# 🗂️ Administración – OmegaLab 2025

## ¡Bienvenidos a la carpeta de Administración!

Aquí se debe subir **todo el material y documentación** que el área de Administración genere a lo largo del reto OmegaLab 2025.

---

## 📋 ¿Qué tipo de contenidos pueden ir aquí?

- Planes de organización y gestión del equipo
- Avances o reportes administrativos
- Cronogramas, planificaciones, asignaciones de tareas
- Cualquier otro documento relacionado con la coordinación y administración del proyecto

# Aplicación del Ágilismo en el Proyecto Ubuntu IUSH

Este documento describe cómo se implementaron principios y prácticas ágiles durante el desarrollo del proyecto **Ubuntu IUSH**, el cual se completó en un tiempo récord de 24 horas. Este enfoque permitió maximizar la colaboración, la entrega de valor y la adaptabilidad en un contexto de alta presión.

---

## ¿Qué es el Ágilismo?

El ágilismo es un conjunto de principios y valores organizados en el **Manifiesto Ágil**, que promueve la entrega rápida y continua de software funcional, la colaboración entre equipos, y la capacidad de adaptarse rápidamente a los cambios. 

Los principales valores del ágilismo son:

1. **Individuos e interacciones** sobre procesos y herramientas.
2. **Software funcionando** sobre documentación exhaustiva.
3. **Colaboración con el cliente** sobre negociación de contratos.
4. **Respuesta ante el cambio** sobre seguir un plan.

---

## Implementación del Ágilismo en el Proyecto

### 1. **Planificación Inicial**
Dado el tiempo limitado (24 horas), se adoptó una estrategia de **MVP (Producto Mínimo Viable)** para enfocar los esfuerzos en las funcionalidades esenciales:

- **Backend:** Diseño de una API funcional que gestionara datos académicos y sirviera al modelo de IA para predicciones.
- **Frontend:** Creación de una interfaz básica pero funcional para consumir la API.
- **Infraestructura:** Configuración rápida de la base de datos en Azure SQL y conexión con el backend.

Se utilizó una lista priorizada de tareas al estilo **Product Backlog** para organizar el trabajo, priorizando las entregas de mayor valor. Estas tareas fueron gestionadas de manera física mediante un **tablero físico** (Kanban) para mantener la visibilidad y el control del progreso.

---

### 2. **Uso del Tablero Físico**
Para la organización del trabajo, se implementó un **tablero físico Kanban**, dividido en tres columnas principales:

- **Por hacer:** Tareas pendientes, tomadas del Product Backlog.
- **En progreso:** Tareas en las que el equipo estaba trabajando activamente.
- **Hecho:** Tareas completadas y verificadas.

Cada tarea fue escrita en notas adhesivas y se movía entre las columnas según su estado. Este método permitió:

- Visualizar el estado del proyecto en todo momento.
- Gestionar de manera simple la carga de trabajo.
- Fomentar la colaboración al asignar tareas rápidamente.

---

### 3. **Iteraciones Rápidas**
El proyecto se dividió en **tres iteraciones principales** de aproximadamente 8 horas cada una:

#### **Iteración 1: Configuración Inicial**
- Estructuración de los repositorios (`Ubuntu-IUSH-Back` y `Ubuntu-IUSH-Front`).
- Configuración de herramientas:
  - Backend: **FastAPI** con conexión a Azure SQL.
  - Frontend: **React** con TypeScript.
- Diseño de la base de datos (DBML) para garantizar la escalabilidad.
- Creación de los primeros endpoints básicos en el backend.

#### **Iteración 2: Desarrollos Funcionales**
- Implementación de modelos, esquemas y rutas REST en el backend.
- Consumo de la API desde el frontend:
  - Conexión inicial con Axios.
  - Diseño de componentes básicos para mostrar datos.
- Pruebas unitarias rápidas para garantizar la estabilidad.

#### **Iteración 3: Integración y Ajustes**
- Integración entre el backend y frontend.
- Pruebas de extremo a extremo para validar flujos críticos.
- Ajustes visuales en la interfaz y optimización de consultas en el backend.

---

### 4. **Comunicación y Colaboración**
Se utilizó un enfoque de **comunicación constante** para mantener a todos los involucrados alineados:

- **Reuniones rápidas (15 minutos cada hora):**
  - Actualización del estado de las tareas.
  - Identificación y resolución inmediata de bloqueos.
- **Uso del tablero físico Kanban:** Como herramienta principal para gestionar las tareas y sincronizar al equipo.

---

### 5. **Adaptabilidad**
Durante el desarrollo, surgieron cambios en los requerimientos. Gracias al enfoque ágil, se priorizaron estas solicitudes sin afectar las entregas:

- **Cambio 1:** Incorporar predicciones basadas en IA para estrés académico.
  - Solución: Se desarrollaron endpoints que simulan la integración con modelos de IA, dejando listo el espacio para su implementación futura.
- **Cambio 2:** Ajustes en el diseño de la base de datos para soportar múltiples universidades.
  - Solución: Se actualizó el esquema DBML y la configuración de los modelos SQLAlchemy.

---

### 6. **Entrega Continua**
Cada iteración resultó en un incremento funcional del sistema que podría demostrarse y usarse:

- **Al final de la Iteración 1:** API básica funcional.
- **Al final de la Iteración 2:** Conexión inicial entre frontend y backend.
- **Al final de la Iteración 3:** Producto funcional con flujos principales completados.

---

## Resultados y Lecciones Aprendidas

### **Resultados**
- **Entrega exitosa:** Un sistema funcional (backend y frontend) desarrollado en 24 horas.
- **Flexibilidad en el diseño:** La arquitectura permite futuras extensiones (por ejemplo, integración completa de IA).
- **Colaboración efectiva:** El equipo trabajó de manera cohesionada, maximizando la productividad.

### **Lecciones Aprendidas**
1. **La simplicidad es clave:** En contextos de tiempo limitado, priorizar las funcionalidades esenciales asegura resultados tangibles.
2. **Comunicación constante:** Las reuniones cortas y frecuentes fueron críticas para mantener el flujo de trabajo.
3. **Gestión visual:** El uso del tablero físico Kanban fue fundamental para organizar y priorizar tareas de manera efectiva.
4. **Documentación ligera pero efectiva:** Aunque se priorizó el código funcional, contar con una base mínima de documentación (como este manual) es esencial para garantizar la continuidad del proyecto.

---

### **Herramientas Utilizadas**
- **Gestión de Tareas:** Tablero físico Kanban.
- **Backend:** Python (FastAPI), SQLAlchemy, Azure SQL.
- **Frontend:** React, TypeScript.
- **Base de Datos:** DBML para el diseño inicial, SQLAlchemy para la implementación.

---

## Conclusión

El enfoque ágil permitió completar con éxito el proyecto en un tiempo extremadamente limitado. Este caso demuestra cómo los principios del ágilismo —como la colaboración, la adaptabilidad y la entrega incremental— son aplicables incluso en proyectos de corta duración y alta presión.

---

¡Buena organización y mucho éxito en el reto! 🚀
