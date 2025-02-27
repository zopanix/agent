---
aliases:
- /docs/agent/shared/flow/reference/components/oauth2-block/
- /docs/grafana-cloud/agent/shared/flow/reference/components/oauth2-block/
- /docs/grafana-cloud/monitor-infrastructure/agent/shared/flow/reference/components/oauth2-block/
- /docs/grafana-cloud/monitor-infrastructure/integrations/agent/shared/flow/reference/components/oauth2-block/
- /docs/grafana-cloud/send-data/agent/shared/flow/reference/components/oauth2-block/
canonical: https://grafana.com/docs/agent/latest/shared/flow/reference/components/oauth2-block/
description: Shared content, oauth2 block
headless: true
---

Name                 | Type           | Description                                     | Default | Required
---------------------|----------------|-------------------------------------------------|---------|---------
`client_id`          | `string`       | OAuth2 client ID.                               |         | no
`client_secret_file` | `string`       | File containing the OAuth2 client secret.       |         | no
`client_secret`      | `secret`       | OAuth2 client secret.                           |         | no
`endpoint_params`    | `map(string)`  | Optional parameters to append to the token URL. |         | no
`proxy_url`          | `string`       | Optional proxy URL for OAuth2 requests.         |         | no
`scopes`             | `list(string)` | List of scopes to authenticate with.            |         | no
`token_url`          | `string`       | URL to fetch the token from.                    |         | no

`client_secret` and `client_secret_file` are mutually exclusive, and only one can be provided inside an `oauth2` block.

The `oauth2` block may also contain a separate `tls_config` sub-block.
