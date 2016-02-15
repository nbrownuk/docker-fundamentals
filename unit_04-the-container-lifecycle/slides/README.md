# The Container Lifecycle
In order to use the slide deck, you need the Docker Engine running locally, or at least have a Docker client installed locally, configured to communicate with a remote Docker host. If you're running Linux, the easiest option is to install Docker with the following command:

```
$ sudo wget -qO- https://get.docker.com | sh
```

If you're not running Linux, then you can follow the installation process provided on Docker's website for [Windows](https://docs.docker.com/engine/installation/windows) or [OS X](https://docs.docker.com/engine/installation/mac).
## Presentation
The presentation is based on the reveal.js HTML presentation framework, and runs in a Docker container. You can either, 1) build the presentation into a Docker image, and start a container based on the image, or 2) mount the presentation artifacts into the container at runtime.

- Build and use an image: just issue the following commands within the `slides` directory to build an image and then run the container (choose a name for the image, e.g. unit1):
```
$ sudo docker build -t image_name .
$ sudo docker run -it --rm -p 8000:8000 image_name
```
- Mount artifacts into container: this requires some Docker knowledge, so if you're new to Docker the easiest thing to do is to make use of the [Docker Compose](https://docs.docker.com/compose/install) application; from the `slides` directory:
```
$ sudo docker-compose up -d
```
Whichever method you choose, a container will be running on the Docker host with port `8000` exposed. Point your web browser at the Docker host URL to use the presentation (e.g. `http://haddock:8000` or `http://localhost:8000`).
## Student Notes
The student notes are designed to accompany the presentation, and provide detail concerning the slide content.
## Lab Exercise
The lab exercise is provided as a means of reinforcing the content provided in the slides and student notes.