## rosa login

Log in to your Red Hat account

### Synopsis

Log in to your Red Hat account, saving the credentials to the configuration file.
The supported mechanism is by using a token, which can be obtained at: https://cloud.redhat.com/openshift/token/rosa

The application looks for the token in the following order, stopping when it finds it:
	1. Command-line flags
	2. Environment variable (ROSA_TOKEN)
	3. Environment variable (OCM_TOKEN)
	4. Configuration file
	5. Command-line prompt


```
rosa login [flags]
```

### Examples

```
  # Login to the OpenShift API with an existing token generated from https://cloud.redhat.com/openshift/token/rosa
  rosa login --token=$OFFLINE_ACCESS_TOKEN
```

### Options

```
      --client-id string       OpenID client identifier. The default value is 'cloud-services'.
      --client-secret string   OpenID client secret.
  -h, --help                   help for login
      --insecure               Enables insecure communication with the server. This disables verification of TLS certificates and host names.
      --scope strings          OpenID scope. If this option is used it will replace completely the default scopes. Can be repeated multiple times to specify multiple scopes. (default [openid])
  -t, --token string           Access or refresh token generated from https://cloud.redhat.com/openshift/token/rosa.
      --token-url string       OpenID token URL. The default value is 'https://sso.redhat.com/auth/realms/redhat-external/protocol/openid-connect/token'.
```

### Options inherited from parent commands

```
      --debug            Enable debug mode.
      --profile string   Use a specific AWS profile from your credential file.
  -v, --v Level          log level for V logs
```

### SEE ALSO

* [rosa](rosa.md)	 - Command line tool for ROSA.

