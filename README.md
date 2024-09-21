
Template Base Odoo
This repository provides a base template for Odoo module development. It includes the essential structure and configurations needed to get started with an Odoo project. The template is designed to help developers scaffold Odoo modules quickly and provides a starting point for customization and module building in Odoo.

Contents
Module Structure: The repository includes a ready-to-use Odoo module structure with the necessary configuration files, such as __manifest__.py, __init__.py, and various folders for models, views, and static assets.

Example Models: Basic model files are provided to demonstrate how to define data models in Odoo using Python.

Example Views: The views folder contains example XML files that define the user interface components for the models.

QWeb Templating: There are examples of QWeb templates that are used in Odoo for rendering HTML-based interfaces.

Security and Access Control: Pre-configured security rules and access control files are included to manage permissions for different user roles.

Localization Support: Support for multi-language localization through .pot files, enabling easy translation of your module.

Prerequisites
Odoo Installation: Ensure that you have Odoo installed on your machine. This repository is compatible with Odoo versions 14.0 and above.
Python 3.x: Make sure Python 3.x is installed on your machine along with the necessary dependencies like pip and virtualenv.
PostgreSQL: Odoo requires PostgreSQL as its database backend.
Installation Steps
Clone the Repository:

bash
Copiar código
git clone https://github.com/alainalberto/template_base_odoo.git
cd template_base_odoo
Set Up a Virtual Environment: Create a virtual environment to manage your Python dependencies for this project:

bash
Copiar código
python3 -m venv venv
source venv/bin/activate
Install Required Dependencies: Install all Python dependencies by running:

bash
Copiar código
pip install -r requirements.txt
Configure Odoo:

Make sure to add the path to the module in your Odoo configuration file (odoo.conf) by adding the module path:
javascript
Copiar código
addons_path = /path/to/template_base_odoo,/path/to/other/addons
Ensure PostgreSQL is running, and create a database for Odoo if not already created:
bash
Copiar código
createdb odoo_db
Run Odoo: Start the Odoo server by running the following command:

bash
Copiar código
./odoo-bin -c /etc/odoo/odoo.conf
Install the Module: After the server starts, log into Odoo, go to the Apps section, and search for your custom module. Click Install to install the module.

Usage
Once the module is installed, you can start customizing the template according to your requirements:

Add models in the models/ folder.
Define views and form layouts in the views/ folder.
Customize access rights in the security/ folder.
For detailed information about Odoo module development, you can refer to the Odoo Development Documentation.

License
This project is licensed under the MIT License.

