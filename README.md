# Template Base Odoo

![Versión](https://img.shields.io/badge/version-1.0-blue) ![Estado](https://img.shields.io/badge/status-en%20desarrollo-yellow)

Este repositorio proporciona una plantilla base para el desarrollo de módulos en Odoo. Incluye la estructura y configuraciones esenciales necesarias para comenzar un proyecto en Odoo, facilitando la creación rápida de módulos personalizados.

## Tabla de Contenidos

1. [Descripción](#descripción)
2. [Características](#características)
3. [Instalación](#instalación)
   - [Prerrequisitos](#prerrequisitos)
   - [Pasos de instalación](#pasos-de-instalación)
4. [Uso](#uso)
5. [Pruebas](#pruebas)
6. [Contribución](#contribución)
7. [Licencia](#licencia)

## Descripción

La plantilla base de este repositorio está diseñada para ayudar a los desarrolladores a comenzar rápidamente con el desarrollo de módulos para Odoo. Proporciona una estructura organizada y ejemplos básicos para modelar datos, crear vistas y manejar la seguridad del módulo.

## Características

- Estructura de módulo Odoo lista para usar.
- Ejemplos de modelos definidos en Python.
- Vistas en XML para la personalización de la interfaz de usuario.
- Archivos de seguridad para la gestión de permisos.
- Soporte para localización multilingüe con archivos `.pot`.

## Instalación

### Prerrequisitos

- **Odoo 14.0 o superior**: Asegúrate de tener instalada la versión adecuada de Odoo.
- **Python 3.x**: Necesitas tener instalado Python 3.x en tu máquina.
- **PostgreSQL**: Odoo usa PostgreSQL como base de datos, asegúrate de tenerlo instalado y en funcionamiento.

### Pasos de instalación

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/alainalberto/template_base_odoo.git
   cd template_base_odoo

2. **Crear un entorno virtual:**
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   
3. **Instalar dependencias:**
   ```bash
   pip install -r requirements.txt
   
4. **Configurar Odoo:**

  - Abre el archivo de configuración de Odoo (odoo.conf) y agrega la ruta de este módulo:
    ```plaintext
    addons_path = /path/to/template_base_odoo,/path/to/other/addons

 - Si es necesario, crea una base de datos PostgreSQL para Odoo:
   ```bash
   createdb odoo_db

5. **Ejecutar Odoo:**

   Inicia el servidor de Odoo usando el archivo de configuración:

   ``1bash
   ./odoo-bin -c /etc/odoo/odoo.conf

6. **Instalar el módulo:**

   Una vez que el servidor está en funcionamiento, ve a la interfaz web de Odoo, entra en la sección de Apps, busca el módulo e instálalo.

## Uso
Una vez instalado el módulo, puedes empezar a personalizarlo según tus necesidades:

- Añade nuevos modelos en la carpeta models/.
- Define nuevas vistas y layouts de formularios en views/.
- Personaliza los derechos de acceso en security/.
 Para ver un ejemplo de cómo consumir la API del módulo, puedes ejecutar el siguiente comando:
  ```bash
  curl -X GET http://localhost:8069/api/tu_modulo_endpoint

## Pruebas
Si el repositorio incluye pruebas, puedes ejecutarlas con:
 ```bash
 python -m unittest discover tests
O con el gestor de dependencias de Odoo:
  ```bash
  ./odoo-bin --test-enable --db-filter=odoo_db --log-level=test

## Contribución 
Si deseas contribuir a este proyecto, sigue estos pasos:

Haz un Fork del proyecto.
Crea una nueva rama para tu funcionalidad (git checkout -b feature-nueva-funcionalidad).
Realiza los cambios necesarios y haz un commit (git commit -m 'Añadir nueva funcionalidad').
Empuja los cambios a tu rama (git push origin feature-nueva-funcionalidad).
Abre un Pull Request para que se revise tu contribución.

## Licencia
Este proyecto está licenciado bajo la Licencia MIT. Consulta el archivo LICENSE para más detalles. 
