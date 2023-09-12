# Install PostgreSQL LINUX

``` sh
sudo sh -c 'echo "deb https://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'
wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
sudo apt-get update
sudo apt-get -y install postgresql
```

Verificar el estado de postgres:
```sh
systemctl status postgres


sudo -i -u postgres # ingresar al usuario de postgres 
psql # iniciar la shell de postgres
\q # salir de la shell

```

Instalar venv -> `sudo apt install python3.10-venv`

Crear un entorno virtual ->  `python3 -m venv env`

Activar entorno virtual en linux -> `source env/bin/activate`

Instalar conector python a Postgres - >  https://bobbyhadz.com/blog/python-error-setup-script-exited-with-error-command-failed

Corregir error de instalacion psycopg2 -> https://stackoverflow.com/questions/61026031/pip-installation-for-python3-problem-consider-adding-this-directory-to-path

Instalar psycopg2 `pip3 install psycopg2`

```sh
# PGADMIN4 LINUX MINT

#
# Setup the repository
#

# Install the public key for the repository (if not done previously):
sudo curl https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo apt-key add

# Create the repository configuration file:
# SEE MODIFICATION BELOW
sudo sh -c 'echo "deb https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/focal pgadmin4 main" > /etc/apt/sources.list.d/pgadmin4.list && apt update'

#
# Install pgAdmin
#

# Install for both desktop and web modes:
sudo apt install pgadmin4

# Install for desktop mode only:
sudo apt install pgadmin4-desktop

# Install for web mode only: 
sudo apt install pgadmin4-web 

# Configure the webserver, if you installed pgadmin4-web:
sudo /usr/pgadmin4/bin/setup-web.sh

```

### DATABASE POSTGRES
create database sgidb;