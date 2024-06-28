# tagstr-docker

This directory contains Dockerfiles for CPython of lysnikolaou's [tag-strings-rebased](https://github.com/lysnikolaou/cpython/tree/tag-strings-rebased) branch.

The dockerfile were generated with [a patched version of the official dockerfile code generator](https://github.com/koxudaxi/docker-python/blob/support_tag_string_v2_branch/apply-templates.sh).
The patched code generator and Dockerfiles exist in [Koudai's(@koxudaxi) repository](https://github.com/koxudaxi/docker-python/tree/support_tag_string_v2_branch) is fork on the official Python Dockerfile repository.

All images are available on [Docker Hub](https://hub.docker.com/r/koxudaxi/python).
These images are built and published on [GitHub Actions](https://github.com/koxudaxi/tagstr-docker/actions)

## How to pull from Docker Hub
```shell
$ docker pull koxudaxi/python:3.14.0a0-alpine3.20
```

## How to run
```shell
$ docker run -it --rm koxudaxi/python:3.14.0a0-alpine3.20
Python 3.14.0a0 (heads/tag-strings-rebased:704fafe, Jun 28 2024, 07:38:57) [GCC 13.2.1 20240309] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> def html(content):
...     return f"<html>{content}</html>"
...
>>> html"Hello, world!"
'<html>Hello, world!</html>'
```

## How to build from Dockerfile
```shell
$ make build # default base image is alpine3.20
$ make build BASE_IMAGE=slim-bookworm # base image is debian:bookworm-slim
$ make build-all # build all base images
```

## Base images
- alpine3.20
- alpine3.19
- bookworm
- bullseye
- slim-bookworm
- slim-bullseye
## All tags for each base image
- alpine3.20
  - 3.14.0a0-alpine3.20
  - 3.14.0a0-tag-strings-rebased-alpine3.20
  - 3.14.0a0-tag-strings-rebased-704fafe-alpine3.20
- alpine3.19
  - 3.14.0a0-alpine3.19
  - 3.14.0a0-tag-strings-rebased-alpine3.19
  - 3.14.0a0-tag-strings-rebased-704fafe-alpine3.19
- bookworm 
  - 3.14.0a0-bookworm
  - 3.14.0a0-tag-strings-rebased-bookworm
  - 3.14.0a0-tag-strings-rebased-704fafe-bookworm
- bullseye
  - 3.14.0a0-bullseye
  - 3.14.0a0-tag-strings-rebased-bullseye
  - 3.14.0a0-tag-strings-rebased-704fafe-bullseye
- slim-bookworm
  - 3.14.0a0-slim-bookworm
  - 3.14.0a0-tag-strings-rebased-slim-bookworm
  - 3.14.0a0-tag-strings-rebased-704fafe-slim-bookworm
- slim-bullseye
  - 3.14.0a0-slim-bullseye
  - 3.14.0a0-tag-strings-rebased-slim-bullseye
  - 3.14.0a0-tag-strings-rebased-704fafe-slim-bullseye
