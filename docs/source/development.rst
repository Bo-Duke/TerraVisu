===========
Development
===========

-------------
Prepare stack
-------------

..  code-block:: bash

    cp db.env.dist db.env
    cp app.env.dist app.env
    docker-compose build

-------------
Init database
-------------

..  code-block:: bash

    docker-compose run --rm web ./manage.py migrate


-----------------
Load initial data
-----------------

..  code-block:: bash

    docker-compose run --rm web ./manage.py loaddata project/fixtures/initial.json


---------------------
Create your superuser
---------------------

..  code-block:: bash

    docker-compose run --rm web ./manage.py createsuperuser


------------
Launch stack
------------

..  code-block:: bash

    docker-compose up


Then go to http://visu.localhost:8080


---------
Use admin
---------

..  code-block:: bash

    make build_admin


Then go to http://visu.localhost:8080/admin/
