<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Template Base Odoo - README</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 20px;
        }
        h1, h2, h3 {
            color: #333;
        }
        p {
            margin: 1em 0;
        }
        code {
            background-color: #f4f4f4;
            padding: 2px 4px;
            font-size: 90%;
            color: #d63384;
        }
        pre {
            background-color: #f4f4f4;
            padding: 10px;
            border-left: 4px solid #d63384;
            overflow-x: auto;
        }
        ul {
            list-style-type: disc;
            margin-left: 20px;
        }
        a {
            color: #1a73e8;
        }
    </style>
</head>
<body>

    <h1>Template Base Odoo</h1>

    <p>Este repositorio proporciona una plantilla base para el desarrollo de módulos en Odoo. Incluye la estructura y configuraciones esenciales necesarias para comenzar un proyecto en Odoo. La plantilla está diseñada para ayudar a los desarrolladores a crear rápidamente módulos de Odoo y ofrece un punto de partida para la personalización y construcción de módulos.</p>

    <h2>Contenido</h2>
    <ul>
        <li><strong>Estructura del Módulo</strong>: El repositorio incluye una estructura de módulo Odoo lista para usar con los archivos de configuración necesarios, como <code>__manifest__.py</code>, <code>__init__.py</code>, y varias carpetas para modelos, vistas y recursos estáticos.</li>
        <li><strong>Modelos de Ejemplo</strong>: Se proporcionan archivos de modelos básicos para demostrar cómo definir modelos de datos en Odoo utilizando Python.</li>
        <li><strong>Vistas de Ejemplo</strong>: La carpeta de vistas contiene archivos XML de ejemplo que definen los componentes de la interfaz de usuario para los modelos.</li>
        <li><strong>Plantillas QWeb</strong>: Hay ejemplos de plantillas QWeb que se utilizan en Odoo para renderizar interfaces basadas en HTML.</li>
        <li><strong>Seguridad y Control de Acceso</strong>: Se incluyen reglas de seguridad y archivos de control de acceso preconfigurados para gestionar los permisos de los distintos roles de usuario.</li>
        <li><strong>Soporte de Localización</strong>: Soporte para la localización multilingüe a través de archivos <code>.pot</code>, lo que permite una fácil traducción de tu módulo.</li>
    </ul>

    <h2>Requisitos Previos</h2>
    <ul>
        <li><strong>Instalación de Odoo</strong>: Asegúrate de que tienes Odoo instalado en tu máquina. Este repositorio es compatible con versiones de Odoo 14.0 y superiores.</li>
        <li><strong>Python 3.x</strong>: Asegúrate de que Python 3.x esté instalado en tu máquina junto con las dependencias necesarias como <code>pip</code> y <code>virtualenv</code>.</li>
        <li><strong>PostgreSQL</strong>: Odoo requiere PostgreSQL como su base de datos backend.</li>
    </ul>

    <h2>Pasos de Instalación</h2>

    <h3>1. Clonar el Repositorio</h3>
    <pre><code>git clone https://github.com/alainalberto/template_base_odoo.git
cd template_base_odoo</code></pre>

    <h3>2. Crear un Entorno Virtual</h3>
    <p>Crea un entorno virtual para gestionar las dependencias de Python de este proyecto:</p>
    <pre><code>python3 -m venv venv
source venv/bin/activate</code></pre>

    <h3>3. Instalar las Dependencias Requeridas</h3>
    <p>Instala todas las dependencias de Python ejecutando:</p>
    <pre><code>pip install -r requirements.txt</code></pre>

    <h3>4. Configurar Odoo</h3>
    <ul>
        <li>Asegúrate de agregar la ruta del módulo en tu archivo de configuración de Odoo (<code>odoo.conf</code>) agregando la ruta del módulo:</li>
        <pre><code>addons_path = /path/to/template_base_odoo,/path/to/other/addons</code></pre>
        <li>Asegúrate de que PostgreSQL esté en funcionamiento y crea una base de datos para Odoo si aún no está creada:</li>
        <pre><code>createdb odoo_db</code></pre>
    </ul>

    <h3>5. Ejecutar Odoo</h3>
    <p>Inicia el servidor de Odoo ejecutando el siguiente comando:</p>
    <pre><code>./odoo-bin -c /etc/odoo/odoo.conf</code></pre>

    <h3>6. Instalar el Módulo</h3>
    <p>Después de que el servidor se inicie, inicia sesión en Odoo, ve a la sección de <strong>Aplicaciones</strong> y busca tu módulo personalizado. Haz clic en <strong>Instalar</strong> para instalar el módulo.</p>

    <h2>Uso</h2>
    <p>Una vez que el módulo esté instalado, puedes empezar a personalizar la plantilla según tus necesidades:</p>
    <ul>
        <li>Añade modelos en la carpeta <code>models/</code>.</li>
        <li>Define vistas y layouts de formularios en la carpeta <code>views/</code>.</li>
        <li>Personaliza los derechos de acceso en la carpeta <code>security/</code>.</li>
    </ul>

    <p>Para obtener más información sobre el desarrollo de módulos en Odoo, puedes consultar la <a href="https://www.odoo.com/documentation">Documentación de Desarrollo de Odoo</a>.</p>

    <h2>Licencia</h2>
    <p>Este proyecto está licenciado bajo la licencia MIT.</p>

</body>
</html>
