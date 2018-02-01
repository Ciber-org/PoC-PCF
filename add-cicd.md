# **Concourse Installation and Setup**

## Introduction {#introduction}

Concourse for Pivotal Cloud Foundry \(PCF\) is a continuous integration and delivery tool that lets you build and monitor scalable pipelines.

## Prerequisites

1. PostgreSQL 9.5 software installation on Windows.
2. Concourse and Fly installation
3. Generating SSL keys for Concourse.

Concourse will use the PostgreSQL database to store its pipeline data.  So, we should set up a PostgreSQL instance on our local server before Concourse.

### ** Installing PostgreSQL on Windows:**

Download and run the Windows PostgreSQL from below link:

[https://www.enterprisedb.com/downloads/postgres-postgresql-downloads\#windows](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads#windows)

1. Install PostgreSQL as a Windows Service.
2. Provide inputs for database superuser name and password during installation.

After Installation PostgreSQL screen should look like below.

![](/assets/Pgadmin)

Once installation is completed, open the pgadmin client, then connect to Postgre database and run the following commands to create database and user account.

CREATE DATABASE concourse

```
WITH 

OWNER = postgres

ENCODING = 'UTF8'

LC\_COLLATE = 'English\_United States.1252'

LC\_CTYPE = 'English\_United States.1252'

TABLESPACE = pg\_default

CONNECTION LIMIT = -1;
```

![](/assets/create database.png)



CREATE DATABASE atc

```
WITH 

OWNER = postgres

ENCODING = 'UTF8'

LC\_COLLATE = 'English\_United States.1252'

LC\_CTYPE = 'English\_United States.1252'

TABLESPACE = pg\_default

CONNECTION LIMIT = -1;
```

#### **Creating users in DB**

CREATE USER concourse WITH

LOGIN

SUPERUSER

INHERIT

CREATEDB

CREATEROLE

NOREPLICATION;

COMMENT ON ROLE concourse IS 'User id for psql';

CREATE USER &lt;local system user id &gt; WITH

LOGIN

SUPERUSER

INHERIT

CREATEDB

CREATEROLE

NOREPLICATION;

COMMENT ON ROLE &lt;local system user id &gt; IS 'User id for psql';



### Concourse and Fly installation on Windows machine.



Download concourse software from below location and find windows **.exe** files.

[https://github.com/concourse/concourse/releases](https://github.com/concourse/concourse/releases)

[**concourse\_windows\_amd64.exe**](https://github.com/concourse/concourse/releases/download/v3.8.0/concourse_windows_amd64.exe)

[**fly\_windows\_amd64.exe**](https://github.com/concourse/concourse/releases/download/v3.8.0/fly_windows_amd64.exe)

Once download is completed, create concourse directory on local folder then generate the below private keys.

1. ssh-keygen -t rsa -f host\_key -N '' 

          ![](/assets/keygen.png)

  2.  ssh-keygen -t rsa -f worker\_key -N '' 

           ![](/assets/workerkey.png)

  3.  ssh-keygen -t rsa -f session\_signing\_key -N ''

           ![](/assets/sessionkey.png)



Once keys are generated successfully, we need to copy them to authorized file using command,

        cp worker\_key.pub authorized\_worker\_keys

#### Starting the Web UI:

The concourse binary embeds the[ATC](https://github.com/concourse/atc)and[TSA](https://github.com/concourse/tsa)components, available as the`web`subcommand.

The ATC is the component responsible for scheduling builds, and also serves as the web UI and API.

The TSA provides a SSH interface for securely registering workers, even if they live in their own private network.

E:\concourse&gt;concourse\_windows\_amd64.exe  web  --basic-auth-username concourse -

-basic-auth-password  concourse  --session-signing-key session\_signing\_key  --ts

a-host-key host\_key  --tsa-authorized-keys authorized\_worker\_keys

Once you've got your Concourse all  setup  , you will want to download the  FLY CLI from your instance via the web UI.You can find the download links by browsing to the main page:

![](/assets/Concourse )

