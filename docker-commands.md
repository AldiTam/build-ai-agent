# Common Docker Commands

## Docker-specific
### Clear System

```bash
docker system prune -a
docker image prune -a
```

### Build and Run Locally

Container image tag: `pyapp`

```bash
docker build -f Dockerfile -t pyapp .
```

```bash
docker run -it pyapp
```

### Enter Container Command Line (like _ssh_)

```bash
docker run -it pyapp /bin/bash
```
> `/bin/bash` just runs the bash shell, you can also run `docker run -it pyapp python` or `docker run -it pyapp node` if those tools are avialable.


### Build and Push to Docker Hub

- Docker Hub Repo/username: codingforentrepreneurs
- Container image name: `ai-py-app-test`
- Container image tag: `v1`

```bash
docker build -f Dockerfile -t codingforentrepreneurs/ai-py-app-test:v1 .
```

```bash
docker push codingforentrepreneurs/ai-py-app-test:v1
# or
docker push codingforentrepreneurs/ai-py-app-test --all-tags
```


## Docker Compose

#### Build with Docker Compose

```bash
docker compose up
```

```bash
docker compose down
```

```bash
docker compose run <service_name> /bin/bash
```