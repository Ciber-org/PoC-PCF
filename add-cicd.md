Concourse Installtion 



Before we download the Concourse CI binaries, we should set up a PostgreSQL instance on our server. Concourse will use the PostgreSQL database to store its pipeline data.





CREATE USER mkunduru WITH

  LOGIN

  SUPERUSER

  INHERIT

  CREATEDB

  CREATEROLE

  NOREPLICATION;



COMMENT ON ROLE mkunduru IS 'User id for psql';





To generate these keys, run:





5. ssh-keygen -t rsa -f host\_key -N '' && ssh-keygen -t rsa -f worker\_key -N '' && ssh-keygen -t rsa -f session\_signing\_key -N ''





Once you've got your Concourse all  setup  , you will want to download the  FLY CLI from your instance via the web UI.You can find the download links by browsing to the main page:



