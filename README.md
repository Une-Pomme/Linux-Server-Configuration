# Linux Server Configuration

IP Address: 35.170.69.229
SSH Port: 2200
URL: http://35.170.69.229/catalog

## Software Installed
- PostgreSQL
- Python 2.7 (and PIP, Flask, Flask-SQLAlchemy, httplib2, oauth2client, pyscopg2, requests, SQLAlchemy)
- Apache2

## Configuration
I had to create a database in PostgreSQL. In order to set up the tables and fill the database, I needed modify database_setup.py and filldatabase.py so that it connected to a PostgreSQL database instead of sqlite.

I had to create catalog.conf in /etc/apache2/sites-available and itemCatalog.wsgi in /var/www/item-catalog. I also modified application.py so that it connected to the PostgreSQL database.

I changed the permissions on the .git folder in /var/www/item-catalog so that it was not publicly accessible.

## Third-Party Resources
- https://github.com/jungleBadger/-nanodegree-linux-server-troubleshoot
- https://www.postgresql.org/docs/9.5/index.html
- https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-16-04
- https://git-scm.com/book/en/v2/Getting-Started-Installing-Git
- https://umar-yusuf.blogspot.com/2018/02/deploying-python-flask-web-app-on.html
- https://github.com/psycopg/psycopg2/issues/560
- https://www.carnaghan.com/knowledge-base/how-to-increase-the-length-of-a-character-varying-datatype-in-postgres-without-data-loss/
- https://unix.stackexchange.com/questions/129573/bash-home-user-ssh-authorized-keys-no-such-file-or-directory

## Author
Lianne McIntosh
