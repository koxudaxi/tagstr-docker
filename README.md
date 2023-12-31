# tagstr-docker

This directory contains Dockerfiles for CPython of tag string v2 branch.

The dockerfile were generated with [a patched version of the official dockerfile code generator](https://github.com/koxudaxi/docker-python/blob/support_tag_string_v2_branch/apply-templates.sh).
The patched code generator and Dockerfiles exist in [Koudai's(@koxudaxi) repository](https://github.com/koxudaxi/docker-python/tree/support_tag_string_v2_branch) is fork on the official Python Dockerfile repository.

All images are available on [Docker Hub](https://hub.docker.com/r/koxudaxi/python).
These images are built and published on [GitHub Actions](https://github.com/koxudaxi/tagstr-docker/actions)

## How to pull from Docker Hub
```shell
$ docker pull koxudaxi/python:3.12.0a7-alpine3.19
```

## How to run
```shell
$ docker run -it --rm koxudaxi/python:3.12.0a7-alpine3.19
Python 3.12.0+ (heads/tag-strings-v2:c7c5cd4, Dec 10 2023, 19:33:29) [GCC 13.2.1 20231014] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> def html(content):
...     return f"<html>{content}</html>"
...
>>> html"Hello, world!"
'<html>Hello, world!</html>'
```

## How to build from Dockerfile
```shell
$ make build # default base image is alpine3.19
$ make build BASE_IMAGE=slim-bookworm # base image is debian:bookworm-slim
$ make build-all # build all base images
```

## Base images
- alpine3.18
- alpine3.19
- bookworm
- bullseye
- slim-bookworm
- slim-bullseye
## All tags for each base image
- alpine3.18
  - 3.12.0a7-alpine3.18
  - 3.12.0a7-tag-strings-v2-alpine3.18
  - 3.12.0a7-tag-strings-v2-e37d679-alpine3.18
- alpine3.19
  - 3.12.0a7-alpine3.19
  - 3.12.0a7-tag-strings-v2-alpine3.19
  - 3.12.0a7-tag-strings-v2-e37d679-alpine3.19
- bookworm 
  - 3.12.0a7-bookworm
  - 3.12.0a7-tag-strings-v2-bookworm
  - 3.12.0a7-tag-strings-v2-e37d679-bookworm
- bullseye
  - 3.12.0a7-bullseye
  - 3.12.0a7-tag-strings-v2-bullseye
  - 3.12.0a7-tag-strings-v2-e37d679-bullseye
- slim-bookworm
  - 3.12.0a7-slim-bookworm
  - 3.12.0a7-tag-strings-v2-slim-bookworm
  - 3.12.0a7-tag-strings-v2-e37d679-slim-bookworm
- slim-bullseye
  - 3.12.0a7-slim-bookworm
  - 3.12.0a7-tag-strings-v2-slim-bookworm
  - 3.12.0a7-tag-strings-v2-e37d679-slim-bookworm
