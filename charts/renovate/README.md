# renovate

Universal dependency update tool that fits into your workflows.

Current chart version is `23.35.0`

**Homepage:** <https://github.com/Gazza7205/helm-charts>

## Installation

### Add Helm repository

```shell
helm repo add renovate https://gazza7205.github.io/helm-charts
helm repo update
```

## Install Renovate chart

Using config from a file:

```bash
helm install --generate-name --set-file renovate.config=config.json renovate/renovate
```

Using config from a string:

```bash
helm install --generate-name --set renovate.config='\{\"token\":\"...\"\}' renovate/renovate
```

**NOTE**: `renovate.config` must be a valid Renovate [self-hosted configuration](https://docs.renovatebot.com/self-hosted-configuration/)

## Configuration

The following table lists the configurable parameters of the chart and the default values.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| cronjob.annotations | object | `{}` |  |
| cronjob.concurrencyPolicy | string | `""` |  |
| cronjob.failedJobsHistoryLimit | string | `""` |  |
| cronjob.jobRestartPolicy | string | `"Never"` |  |
| cronjob.labels | object | `{}` |  |
| cronjob.schedule | string | `"0 1 * * *"` |  |
| cronjob.successfulJobsHistoryLimit | string | `""` |  |
| envFrom | list | `[]` |  |
| existingSecret | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"renovate/renovate"` |  |
| image.tag | string | `"23.35.0"` |  |
| pod.annotations | object | `{}` |  |
| pod.labels | object | `{}` |  |
| renovate.config | string | `""` |  |
| resources | object | `{}` |  |
| secrets | object | `{}` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
