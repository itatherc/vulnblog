# Intended Vulnerable Blog

> [!CAUTION]
> This application is intended to be vulnerable. Do not deploy it in a public environment.

This project is a vulnerable application intended to be used for security training purposes.

## Deployment

### Public Docker image

The easiest way to deploy the application is to use the public Docker image.

```bash
docker run -d --name vulnblog -p 8000:80 itatherc/vulnblog
```

The application will be available at [http://localhost:8000](http://localhost:8000).

### Build the Docker image manually

You can build the Docker image manually, for example to customize the application.

First, clone the repository:

```bash
git clone https://github.com/itatherc/vulnblog.git
cd vulnblog
```

Then build and run the Docker image:

```bash
docker buildx build --platform linux/amd64 -t itatherc/vulnblog . --progress=plain
docker run -d --name vulnblog -p 8000:80 itatherc/vulnblog
```

The application will be available at [http://localhost:8000](http://localhost:8000).