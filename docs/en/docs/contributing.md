As an open source package, fastapi-crudrouter accepts contributions from **all members** of the community. If you are interested in the
contributing, reading the development guidelines below may help you in the process. 😊

## Github

#### Issues
Please create an issue to report a bug, request a feature or to simply ask a question.


#### Pull Requests
Unless the pull request is a simple bugfix, please try to create an issue before starting on the implementation of your pull request.
This ensures that the potential feature is in alignment with CRUDRouter's goals moving forward. This also allows for feedback
on the feature and potential help on where to start implementation wise.

## Development

### Using [poetry](https://python-poetry.org/)

FastAPI-Crudrouter uses [poetry](https://python-poetry.org/) as depenency management system. To install all of the required dependecies simply run:

    poetry install

Both dev-requirements and project-requirements will be installed with this command.

To enter the virtual-environment created with poetry use:

    poetry shell

If you are not familiar with poetry, please read their [usage guide](https://python-poetry.org/docs/basic-usage/).

### Installing the Dev Requirements
FastAPI-Crudrouter requires as set of development requirements that can installed with `pip` be found in `tests/dev.requirements.txt`

<div class="termy">

```console
$ pip install -r tests/dev.requirements.txt
---> 100%
```

</div>

### Testing
When adding additional features, please try to add additional tests that prove that your implementation
works and is bug free.

#### Test requirements
Tests require a postgres database for tests to run. The easiest way to accomplish this is with docker. This project offers
a docker-compose file at tests/conf/dev.docker-compose.yaml. You can use this file with

```console
$ docker compose -f tests/conf/dev.docker-compose.yaml up -d
```

After testing you can tear down the running containers with

```console
$ docker compose -f tests/conf/dev.docker-compose.yaml down
```

#### Running tests
Crudrouter utilizes the [pytest](https://docs.pytest.org/en/latest/) framework for all of its unittests. Tests can be run 
as shown below. 

<div class="termy">

```console
$ pytest
---> 100%
```

</div>

### Linting, Formatting and Typing

With `dev.requirements.txt` installed above you also install tools to lint, format and static type check the project.

To format the project run: 

```
black fastapi_crudrouter tests
```

To check styles, imports, annotations, pep8 etc. run:

```
flake8 fastapi_crudrouter
```

To check static types annotations run: 

```
mypy fastapi_crudrouter tests
```

### Documentation
Crudrouter's documentation was built using [mkdocs-material](https://squidfunk.github.io/mkdocs-material/). To start the development
documentation server, please first install mkdocs-material and then run the server as shown below.

<div class="termy">

```console
$ pip install mkdocs-material
---> 100%
$ cd docs/en
$ mkdocs serve
```

</div>
