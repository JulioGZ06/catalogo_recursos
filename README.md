# Catálogo de Recursos Académicos

## Descripción

Este proyecto es un catálogo de recursos académicos que permite organizar información sobre diferentes materiales que pueden ser utilizados para apoyar el aprendizaje.

## Objetivo

El objetivo es crear una estructura inicial para administrar recursos académicos de manera organizada, permitiendo posteriormente agregar, consultar y clasificar diferentes recursos.

## Estructura general

```text
catalogo_recursos/
├── app/
│   ├── main.py
│   └── configuracion.py
├── data/
│   └── recursos.json
├── docs/
│   ├── alcance.md
│   ├── criterios.md
│   ├── respuestas.md
│   └── evidencias/
├── tests/
│   └── test_basico.py
├── .gitignore
├── README.md
├── requirements.txt
└── CHANGELOG.md
```

## Tecnologías utilizadas

* Python
* Git
* GitHub
* Visual Studio Code

## Preparación del entorno

Primero se debe crear un entorno virtual para el proyecto:

```bash
python -m venv .venv
```

Después se activa el entorno virtual y se instalan las dependencias registradas en `requirements.txt`:

```bash
python -m pip install -r requirements.txt
```

Las dependencias principales del proyecto son `requests` y `rich`.

## Ejecución

Para ejecutar el proyecto se utiliza:

```bash
python app/main.py
```
## Próximas mejoras

En futuras versiones se podrían agregar funciones para buscar, filtrar, actualizar y eliminar recursos académicos. También se podría mejorar la interfaz y organizar los recursos de acuerdo con diferentes criterios.