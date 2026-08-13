# Setup dockerode

Setup docker and nodejs

- always uses latest available version of LTS

## Usage

```yaml
- uses: davidkhala/setup-dockerode@main
  with:
    action-provider: davidkhala # Options: [docker, davidkhala]. Default: davidkhala
    username: ${{ secrets.DOCKERHUB_USERNAME }} # Docker Hub username. If omitted, login is skipped
    password: ${{ secrets.DOCKERHUB_TOKEN }}    # Docker Hub Personal Access Token (PAT)
```

## Known issues

- Rootless docker is used for `ubuntu-latest` exclusively
- `macos-latest` is not supported. [Last support version is `macos-15`](https://github.com/douglascamata/setup-docker-macos-action/issues/35)
