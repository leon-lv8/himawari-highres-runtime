# Himawari Highres runtime

This repository is a public distribution index for the Himawari Highres OCI
container. It intentionally does **not** contain the renderer source code,
Rayleigh LUT files, NOAA credentials, OpenList credentials, or production
deployment configuration. The authoritative source remains the project's
private GitLab repository.

## Container

```text
ghcr.io/leon-lv8/himawari-highres:4d89cda5eb3e3ed5f5f46c6ab48a4e1c33bae31f
```

The image reads public NOAA Himawari-9 AHI L1b data and publishes z6/z7
Rayleigh-corrected true-colour PMTiles to an operator-configured S3-compatible
endpoint. See the image metadata and the private deployment documentation for
the full operational configuration.

The package is expected to remain private because its filesystem contains the
Python renderer. GitHub Actions authenticates with a read-only package token.
The image is not a grant of rights to the private source repository, and all
bundled third-party components remain subject to their respective licenses and
attribution requirements.
