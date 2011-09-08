===============
SyrusAkbary.com
===============

Este repositorio es una copia exacta de mi web personal http://syrusakbary.com

Instalaci�n
===========
Para correr la web tu propio servidor tienes que seguir estos pasos:

#. Descargar el repositorio::

	git clone https://SyrusAkbary@github.com/SyrusAkbary/syrusakbary.com.git
	cd syrusakbary.com

#. Instalar pip en el caso de no tenerlo instalado::

	easy_install pip

#. Instalar los requerimientos de la p�gina::

	pip install -r requirements.pip

#. Instalar el m�dulo de MySQL para Python (en el caso de no tenerlo instalado)::

	pip install mysql-python

#. Crear el archivo local_settings.py en la carpeta website que defina las variables de entorno (BBDD). Ejemplo::

	#website/local_settings.py
	DATABASES = {
	    'default': {
	        'ENGINE': 'django.db.backends.mysql', # Add 'postgresql_psycopg2', 'postgresql', 'mysql', 'sqlite3' or 'oracle'.
	        'NAME': '{Nombre de la Base de Datos}',                      # Or path to database file if using sqlite3.
	        'USER': '{Usuario}',                      # Not used with sqlite3.
	        'PASSWORD': '{Contrase�a}',                  # Not used with sqlite3.
	        'HOST': '',                      # Set to empty string for localhost. Not used with sqlite3.
	        'PORT': '',                      # Set to empty string for default. Not used with sqlite3.
	    },
	}

#. Sincronizar la base de datos::

	python manage.py syncdb

#. Generar los archivos js y css::

	python manage.py generatemedia

#. Ejecutar el servidor::

	python manage.py runserver

Y ya tendr�s la p�gina completamente funcional en tu ordenador.

Administraci�n
==============

Para la administrar la p�gina solo tendr�s que entrar en http://127.0.0.1:8000/admin/
con tu nombre de usuario y contrase�a