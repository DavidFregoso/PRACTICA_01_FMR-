# PRACTICA_01_FMR

## Descripción del Proyecto

Este repositorio contiene la práctica de manejo de Git para la clase de Gestión de Integración de Código.  
El proyecto consiste en crear una pequeña página web y gestionar sus cambios mediante ramas, merges, resolución de conflictos y el uso de un archivo `.gitignore` para ignorar la carpeta de logs.

## Estructura del Repositorio

- **index.html**: Página principal con la estructura básica y, en ciertas ramas, con una navbar.
- **page_a.html**: Página A (incluye una tabla 2x3 en la rama feature_1).
- **page_b.html**: Página B (puede contener una tabla en la rama feature_2).
- **styles/style.css**: Hoja de estilos que varía según la rama (inicialmente headers rojos, luego amarillo y finalmente verde en main).
- **scripts/script.js**: Archivo JavaScript que realiza operaciones (inicialmente suma y luego resta en la rama fix_1).
- **.gitignore**: Archivo que ignora la carpeta `logs`.
- **logs/**: Carpeta local con archivos de log (log_1.txt, log_2.txt, log_3.txt); no se versiona.
- **readme.md**: Este documento.

## Ramas y Funcionalidades

- **main**: Rama principal con la carga inicial y los cambios finales.
- **feature_1**: Rama en la que se agregó la navbar en `index.html` y se modificó `page_a.html` para incluir una tabla.
- **feature_2**: Rama en la que se modificaron los estilos en `styles/style.css` (cambio de color a amarillo) y se añadió contenido (tabla e imagen).
- **fix_1**: Rama creada para corregir errores (por ejemplo, cambiar la operación de suma a resta en `scripts/script.js`).

## Comandos Clave Utilizados

```bash
# Clonar el repositorio
git clone https://github.com/DavidFregoso/PRACTICA_01_FMR.git

# Creación y uso de ramas
git checkout -b feature_1
# (Editar index.html para agregar navbar)
git add index.html
git commit -m "En feature_1: Agregar navbar en index.html"
git push origin feature_1

# Integración en main (merge)
git checkout main
git merge feature_1
git push origin main
