# Jenkins' Dockerfile Instructions

## How to use this Dockerfile

1. **Build the image**

Build from `CI-CD Project/jenkins`:

```bash
docker build -t custom-jenkins .
```

2. **Run the Jenkins container**

Run from `CI-CD Project/jenkins`:

```bash
docker run -d \
  -u root \
  -p 8080:8080 -p 50000:50000 \
  -v jenkins_home:/var/jenkins_home \
  -v /var/run/docker.sock:/var/run/docker.sock \
  --name jenkins \
  custom-jenkins
```
3. **Run Command from Container**

```bash
docker exec -it <container-name> bash
```