# Using a docker container to generate certificates

The Dockefile in this directory will generate a Docker image that is set-up to generate certificates using
the `certificates.py` script.

From the top level project directory build the image with

```sh
docker build -t carpentries-certificates docker/
```

Then run it with

```sh
docker run --rm -v <host dir>:/certificates carpentry-certificates -o /certificates [other arguments]
```

This will generate certificates in `<host dir>` on your machine. Run

```sh
docker run --rm carpentry-certificates
```

for details on the available options.