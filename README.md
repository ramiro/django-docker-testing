# Django Docker Testing

A Docker image for your Django Open Source Project testing needs.

Includes:

* All the Python versions you need pre-installed:
    * 2.7
    * 3.3
    * 3.4
    * 3.5
    * 3.6
* `tox` (and `detox` — its distributed offspring) ready to go.

## Usage

Add a `Dockerfile` to your project like the following:

```
FROM carlton/django-docker-testing:dev

RUN mkdir /src
WORKDIR /src
ADD . /src/

CMD ['tox']
```


Sit back and enjoy!

Example assumes you're using `tox` already. (Do so, it's great.)

The `dev` tag awaits finalising the tagging scheme. See #1.

