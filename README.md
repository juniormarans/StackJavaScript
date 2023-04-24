# General workflow

The dependencies are managed with [Poetry](https://python-poetry.org/), go there and install it.

From `./backend/` you can install all the dependencies with:

```console
$ poetry install
```
If it originates from a requirements.txt
```console
$ cat requirements.txt | xargs poetry add
```

Then you can start a shell session with the new environment with:

```console
$ poetry shell
```
----
## **Root Directory**
- Next, open your editor at `./backend/` (instead of the project root: `./`), so that you see an `./app/` directory with your code inside. That way, your editor will be able to find all the imports, etc. Make sure your editor uses the environment you just created with Poetry.

#### **alembic:**
- If you need to use a relational database, it is recommended to use [alembic](https://alembic.sqlalchemy.org/en/latest/) to manage data migrations. `./backend/alembic/`


**Migrations**
During local development run the migrations with `alembic` commands and the migration code will be in your app directory. So you can add it to your git repository.

Make sure you create a "revision" of your models and that you "upgrade" your database with that revision every time you change them. As this is what will update the tables in your database. Otherwise, your application will have errors.

* If you created a new model in `./backend/app/models/`, make sure to import it in `./backend/app/db/`, that Python module (`base.py`) that imports all the models will be used by Alembic.

* After changing a model (for example, adding a column), create a revision, e.g.:

```console
$ alembic revision --autogenerate -m "Add column last_name to User model"
```

* Commit to the git repository the files generated in the alembic directory.

* After creating the revision, run the migration in the database (this is what will actually change the database):

```console
$ alembic upgrade head
```

#### **app**
- the app level encapsulates the application modules `./backend/app/`

- **api** contains all application endpoints `./backend/app/api/`
- **auth** if necessary, it contains the application documentation, standard for authorization. OAuth 2.0-based Allows applications such as Web App, Mobile and Desktop to gain limited access to user information via the HTTP protocol `./backend/app/auth/`.
- **core** contains all environment variables used in the application `./backend/app/core/`, obtaining `.env` files as source in `./`

- **database** if there is a need to prepopulate data, they should stay at this level`./backend/app/database/`.

- **db** configure the connection and build the database `./backend/app/db/`.

- **models** Modify or add SQLAlchemy models in `./backend/app/models/`
- **schema** responsible for validating the data structure before allowing input to an endpoint.

- **static** only if there is a need for static elements in the project.

- **templates** contains templates that are needed in the project, if necessary.

- **uploads** if necessary save files.

- **util** module that contains methods that may or may not be reused in different projects. if Minio client, settings in `./backend/app/util/` (the file `minio.py`)
if Websocket client, settings in `./backend/app/util/` (the file `ws.py`)

#### **docs**
- if it exists, it contains the application's documentation `./backend/docs/`

#### **tests**
- The ideal scenario would be TDD. Test driven development is a process where you write the test before writing the code. `./backend/tests/`

#### **.env**
- All environment variables can be fount int the directory `./backand/`(the file `.env`)

#### **Dependencies**
- All the dependencies can be found in the directory `./backend` (the file `pyproject.toml` and `requiriments.txt`)
