SETUP AND INSTALLATION:
	
	System:
		Ubuntu 18.04 LTS

	python3 manage.py migrate
	python3 manage.py runserver


	Postgresql:
		sudo systemctl status postgresql.service
		sudo systemctl start postgresql
		sudo systemctl stop postgresql
		sudo -i -u postgres psql
			postgres=# \du
			postgres=# CREATE ROLE mydatabaseuser PASSWORD 'mypassword' SUPERUSER LOGIN CREATEROLE CREATEDB;
			postgres=# \q

	Migrations:
		Change model.
		python3 manage.py makemigrations polls
		python3 manage.py makemigrate

	Use shell:
		python3 manage.py shell

	Django admin:
		python manage.py createsuperuser
		admin
		admin@example.com
		12345678

		python manage.py runserver
		http://127.0.0.1:8000/admin/

	Running Tests:
		python manage.py test polls