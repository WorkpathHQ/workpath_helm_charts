## Workpath Helm Charts
- This repository contains Helm charts created internally at Workpath.
- *Note:* This repository and the associated Github Pages are publicly accessible.
- The repostitory is accessible at (https://helmcharts.workpath.com) on the `gh-pages` branch.

### Usage
- This repository includes a Github Actions workflow using [Chart Releaser Action](https://github.com/helm/chart-releaser-action) that generates a new Helm chart release as a downloadable archive, to be used by the Helm installer.
- The action also generates a new `index.yaml` file in the `gh-pages` branch, which includes the new Helm release.
- Helm charts need to be stored in separate directories under the charts directory.
- Changes to the charts *must* include a change to the charts version in the `chart.yaml`. For example, the version for the OKR generator [here](https://github.com/WorkpathHQ/workpath_helm_charts/blob/master/charts/okr-generator/Chart.yaml#L15)
- When installing the Helm chart, you can either specify the version or omit the version to install the latest.
