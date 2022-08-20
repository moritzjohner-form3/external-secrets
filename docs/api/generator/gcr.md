GCRAccessToken creates a GCP Access token that can be used to authenticate with GCR in order to pull OCI images.

## Output Keys and Values

| Key        | Description                                                               |
| ---------- | ------------------------------------------------------------------------- |
| username   | username for the `docker login` command.                                  |
| password   | password for the `docker login` command.                                  |
| token_type | type of token                                                             |
| expiry     | time when token expires in UNIX time (seconds since January 1, 1970 UTC). |

## Authentication

Choose one authentication method:

* workload identity `spec.auth.workloadIdentity`
* GCP Service Account `spec.auth.secretRef`


## Example Manifest

```yaml
{% include 'generator-gcr.yaml' %}
```
