
# Readme

Manual for installation of the Movsentry Plattform




## Installation

- Clone this github repo
- Install the requirements
```bash
  pip install -r requirements.txt
```

- recompile the template
```bash
  cd src/
  yarn
  cd src/assets/
  yarn build
```

- Setup PostgreSQL Database:
```bash
sudo apt-get install postgresql postgresql-contrib

pip install psycopg2-binary

sudo -i -u postgres

psql

CREATE ROLE movsentrydbuser WITH ENCRYPTED PASSWORD '&%mysuperS3cureWasswordthatc4ndiff!culh4ck3rsBruteforce!hehe$';

ALTER ROLE "movsentrydbuser" WITH LOGIN; --use double quotes here

CREATE DATABASE movsentry;

GRANT ALL PRIVILEGES ON DATABASE movsentry TO movsentrydbuser;
```

- Import DB Dump:
Note: move into dbdump folder
```bash
psql --username=movsentrydbuser movsentry < db.sql
```

Add the following to the /etc/hosts file:
```bash
127.0.0.1 movsentry.local
127.0.0.1 tenant1.movsentry.local
127.0.0.1 tenant2.movsentry.local
```
## Runserver

```bash
  python manage.py runserver 0.0.0.0:8000
```

Access over tenant1.movsentry.local:8000

## Users

The Following Users are active:

```bash
  roman.buehler@movet.ch (PW: roman) 
  roman.buehler@hotmail.com (PW: roman)
  ivy.rotti@movet.ch (PW: roman)
```


## Links

Links for the Plattform:

[Tenant 1 - Login](http://tenant1.movsentry.local:8000/login/)

[Tenant 1 - Admin](http://tenant1.movsentry.local:8000/dashboard/)

[Tenant 1 - Front](http://tenant1.movsentry.local:8000/front/landing)

[Tenant 1 - Microtraining](http://tenant1.movsentry.local:8000/front/microtraining/2)




## Documentation

[Template - Vuexy](https://demos.pixinvent.com/vuexy-html-admin-template/documentation/index.html)

