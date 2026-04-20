## Container Documentation for Solr Documentation

The CleanStart Solr image provides a production-ready, security-hardened container optimized for enterprise environments. Built on a minimal base OS with comprehensive security hardening, this image delivers reliable application execution with advanced security features.

📌 **Base Foundation**: Production-ready container from cleanstart.

**Image Path**: `ghcr.io/cleanstart-containers/solr`

**Registry**: cleanstart Registry

## Pull Latest Image
Download the container image from the registry

```bash
docker pull ghcr.io/cleanstart-containers/solr:latest
```
```bash
docker pull ghcr.io/cleanstart-containers/solr:latest-dev
```


## Basic Run
Run the container with basic configuration

```bash
docker run -it --name solr ghcr.io/cleanstart-containers/solr:latest
```

## Production Deployment
Deploy with production security settings

```bash
docker run -d --name solr-prod \
  --security-opt=no-new-privileges \
  --restart unless-stopped \
  ghcr.io/cleanstart-containers/solr:latest
```

Volume Mount Mount local directory for persistent data

```bash
docker run -v /app:/app ghcr.io/cleanstart-containers/solr:latest
```

Port Forwarding Run with custom port mappings

```bash
docker run -p 8080:8080 ghcr.io/cleanstart-containers/solr:latest
```

## Kubernetes Security Context
Recommended security context for Kubernetes deployments

```yaml
securityContext:
  allowPrivilegeEscalation: false
  capabilities:
    drop:
    - ALL
  readOnlyRootFilesystem: true
  runAsUser: 1000
  runAsGroup: 1000
```

## Documentation Resources
Essential links and resources for further information
 
**CleanStart Images**: https://images.cleanstart.com/
 
**Community Images**:<br>
**Docker Hub**: https://hub.docker.com/u/cleanstart<br>
**GitHub**: https://github.com/cleanstart-containers<br>
**AWS ECR Public Gallery**: https://gallery.ecr.aws/cleanstart/
 
**Presence on Social Media**:<br>
**Community**: https://www.linkedin.com/groups/18324021/<br>
**YouTube**: https://www.youtube.com/@CleanStartOfficial<br>
 
**Contribute to Container Use Cases**: https://github.com/cleanstart-dev/cleanstart-use-cases/
