# ops-template

This repository serves as a common location for storing reusable GitHub Actions workflows.

## Workflows

### DependencyTrack (dependency-track-python-uv.yml)

Generates and uploads a Software Bill of Materials (SBOM) for Python projects to DependencyTrack.

**Usage:**
```yaml
jobs:
  dependencyTrack:
    uses: softwareone-platform/ops-template/.github/workflows/dependencyTrack.yml@main
    with:
      projectName: 'your-project-name'
    secrets:
      DEPENDENCYTRACK_APIKEY: ${{ secrets.DEPENDENCYTRACK_APIKEY }}
```

**Required Inputs:**
- `projectName`: The name of the project in DependencyTrack.

**Required repository secrets:**
- `DEPENDENCYTRACK_APIKEY`: The API key for accessing DependencyTrack.
