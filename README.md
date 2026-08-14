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

- Rootless docker
  - `ubuntu-latest`: `unix:///run/user/1001/docker.sock`
  - macos: use Colima sock `unix:///Users/runner/.colima/default/docker.sock`
  - `windows-latest`: No support
- `macos-latest` is not supported. Last support version is `macos-26-intel`
