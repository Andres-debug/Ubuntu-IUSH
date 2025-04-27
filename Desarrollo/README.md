# 💻 Desarrollo – OmegaLab 2025

## ¡Bienvenidos a la carpeta de Desarrollo!

Aquí se debe subir **todo el material y avances técnicos** que el área de Desarrollo genere durante el reto OmegaLab 2025.

---

## 🛠️ ¿Qué tipo de contenidos pueden ir aquí?

- Código fuente del proyecto
- Documentación técnica
- Pruebas y prototipos funcionales
- Avances de desarrollo y mejoras
- Cualquier otro recurso relacionado con la parte técnica o de programación

  ##Aqui esta nuestro codigo fuente

https://github.com/Andres-debug/Ubuntu-IUSH-Front

# Manual Técnico - Proyectos Ubuntu IUSH

Este documento cubre los aspectos técnicos de los repositorios `Ubuntu-IUSH-Back` y `Ubuntu-IUSH-Front`. Ambos forman parte de un sistema destinado a la gestión académica y la predicción de estrés académico.

---

## Tabla de Contenidos
- [Descripción General](#descripción-general)
- [Estructura del Proyecto](#estructura-del-proyecto)
  - [Backend (`Ubuntu-IUSH-Back`)](#backend-ubuntu-iush-back)
  - [Frontend (`Ubuntu-IUSH-Front`)](#frontend-ubuntu-iush-front)
- [Instalación y Configuración](#instalación-y-configuración)
  - [Requisitos Previos](#requisitos-previos)
  - [Instrucciones para el Backend](#instrucciones-para-el-backend)
  - [Instrucciones para el Frontend](#instrucciones-para-el-frontend)
- [Ejecución](#ejecución)
  - [Ejecutar el Backend](#ejecutar-el-backend)
  - [Ejecutar el Frontend](#ejecutar-el-frontend)
- [Contribuir](#contribuir)
- [Contacto y Soporte](#contacto-y-soporte)

---

## Descripción General

### Ubuntu-IUSH-Back
Este repositorio contiene el backend del sistema, desarrollado principalmente en **Python** utilizando el framework **FastAPI**. Su propósito principal es:
- Proveer una API RESTful para la gestión de datos académicos.
- Conectarse a una base de datos en Azure SQL para almacenar y procesar datos.
- Implementar modelos de predicción para detectar estrés académico y riesgos de deserción.

### Ubuntu-IUSH-Front
Este repositorio contiene el frontend del sistema, desarrollado principalmente en **TypeScript** con **React**. Su propósito es:
- Proveer una interfaz de usuario amigable para estudiantes, profesores y administradores.
- Consumir la API RESTful del backend para mostrar datos y recomendaciones.

---

## Estructura del Proyecto

### Backend (`Ubuntu-IUSH-Back`)

```plaintext
Ubuntu-IUSH-Back
├── app
│   ├── __init__.py
│   ├── main.py                # Punto de entrada de la aplicación FastAPI
│   ├── api
│   │   ├── routes             # Contiene los endpoints de la API
│   │   └── dependencies.py    # Dependencias comunes
│   ├── core
│   │   ├── config.py          # Configuración global (ej. conexión a la base de datos)
│   │   └── security.py        # Seguridad (ej. autenticación)
│   ├── db
│   │   ├── base.py            # Modelos base de SQLAlchemy
│   │   └── session.py         # Gestión de la sesión de la base de datos
│   ├── models                 # Modelos de datos (ORM)
│   ├── schemas                # Esquemas Pydantic (validación de datos)
│   └── tests                  # Pruebas unitarias
├── requirements.txt           # Dependencias del proyecto
├── .env                       # Variables de entorno
└── README.md                  # Descripción del proyecto
```

### Frontend (`Ubuntu-IUSH-Front`)

```plaintext
Ubuntu-IUSH-Front
├── src
│   ├── components             # Componentes reutilizables
│   ├── pages                  # Vistas principales (Home, Dashboard, etc.)
│   ├── services               # Consumo de la API (ej. Axios)
│   ├── styles                 # Archivos de estilo (CSS, SCSS)
│   ├── App.tsx                # Punto de entrada de la aplicación React
│   └── index.tsx              # Renderizado de la aplicación
├── public                     # Archivos públicos (ej. favicon, index.html)
├── package.json               # Dependencias y scripts de npm
├── tsconfig.json              # Configuración de TypeScript
└── README.md                  # Descripción del proyecto
```

---

## Instalación y Configuración

### Requisitos Previos
1. **Backend:**
   - Python 3.9 o superior.
   - Base de datos en Azure SQL configurada.
   - ODBC Driver 17 for SQL Server (u otra versión compatible).

2. **Frontend:**
   - Node.js 16 o superior.
   - npm o yarn como gestor de paquetes.

### Instrucciones para el Backend
1. Clona el repositorio:
   ```bash
   git clone https://github.com/Andres-debug/Ubuntu-IUSH-Back.git
   cd Ubuntu-IUSH-Back
   ```

2. Crea un entorno virtual e instala las dependencias:
   ```bash
   python -m venv env
   source env/bin/activate  # En Windows: env\Scripts\activate
   pip install -r requirements.txt
   ```

3. Configura las variables de entorno en un archivo `.env`:
   ```env
   DB_USER=admin-aula
   DB_PASSWORD={password}
   DB_SERVER=iush-proyecto-aula.database.windows.net
   DB_DATABASE=omega-ubuntu
   DB_DRIVER=ODBC Driver 17 for SQL Server
   ```

4. (Opcional) Inicializa la base de datos:
   ```bash
   python -m app.db.base init
   ```

### Instrucciones para el Frontend
1. Clona el repositorio:
   ```bash
   git clone https://github.com/Andres-debug/Ubuntu-IUSH-Front.git
   cd Ubuntu-IUSH-Front
   ```

2. Instala las dependencias:
   ```bash
   npm install
   ```

3. Configura las variables de entorno en un archivo `.env`:
   ```env
   REACT_APP_API_URL=http://localhost:8000/api/v1
   ```

---

## Ejecución

### Ejecutar el Backend
1. Activa el entorno virtual:
   ```bash
   source env/bin/activate  # En Windows: env\Scripts\activate
   ```

2. Ejecuta el servidor:
   ```bash
   uvicorn app.main:app --reload
   ```

3. La API estará disponible en: [http://localhost:8000](http://localhost:8000)

### Ejecutar el Frontend
1. Inicia el servidor de desarrollo:
   ```bash
   npm start
   ```

2. La aplicación estará disponible en: [http://localhost:3000](http://localhost:3000)

---

## Contribuir

1. Haz un fork del repositorio.
2. Crea una rama para tu nueva funcionalidad o corrección de errores:
   ```bash
   git checkout -b feature/nueva-funcionalidad
   ```
3. Realiza los cambios necesarios y escribe pruebas.
4. Asegúrate de que las pruebas pasen:
   ```bash
   pytest  # Para el backend
   npm test  # Para el frontend
   ```
5. Envía un Pull Request detallado.

---

## Contacto y Soporte

Si tienes dudas o necesitas ayuda, contacta con el administrador del proyecto:

- **Nombre:** Andrés (Andres-debug)
- **Correo:** [andres@example.com](mailto:andres@example.com)
- **GitHub:** [Andres-debug](https://github.com/Andres-debug)

---


---

¡Mucho éxito programando y creando cosas increíbles! 🚀
