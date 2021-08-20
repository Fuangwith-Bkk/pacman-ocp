# pacman on Red Hat OpenShift
Container Image: quay.io/fuangwit/pacman-ocp:0.1







# pacman
Pac-Man

## Install dependencies

```
npm install
```

## Getting started

```
npm run start
```

## Development

```
npm run dev
```

## Create Application Container Image

### Docker Container Image

The [Dockerfile](docker/Dockerfile) performs the following steps:

1. It is based on Red Hat Node.js 12 (registry.access.redhat.com/ubi8/nodejs-12:latest)
2. It then clones the Pac-Man game into the configured application directory.
3. Exposes port 8080 for the web server.
4. Starts the Node.js application using `npm start`.

To build the image run:

```
docker build -t <registry>/<user>/pacman-ocp:<tag> .
```

You can test the image by running:

```
docker run -p 8000:8080 <registry>/<user>/pacman-ocp:<tag>
```

And going to `http://localhost:8000/` to see if you get the Pac-Man game.

Once you're satisfied you can push the image to the container registry.

```
docker push <registry>/<user>/pacman-ocp:<tag>
```

### Building using OpenShift S2I
- Developer console
- +Add
- `Git Repository` --> `From Git`
- Git Repo URL: `https://github.com/Fuangwith-Bkk/pacman-ocp.git`
- and add environment variables