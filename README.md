# Revoke unbound Okta certificates

We ran into an issue during testing where we had Okta clients running into the 5 unbound certificates limit. Okta provided me with a link to a third-party script that would revoke these unbound certs. I took the script and added a few features I felt made the script easier to use.

## Acknowledgements

This script was forked from: https://github.com/isaiahtech/revoke_device_trust_okta/blob/main/okta_cert_revoke.py
## Usage/Examples

This script has two flags:

| Flag           | Abrev | Description                                                  |
| -------------- | ----- | ------------------------------------------------------------ |
| --target_uuid  | -t    | UUID of machine you are targeting, otherwise the UUID of the machine the script is running on. |
| --delete-certs | -d    | Delete unbound certificates, otherwise list only.            |

Executing the script with no flags set will **search for** and **list** the certs available for the **machine the script is run on**. No other actions will take place.
## Authors

- Todd McDaniel [@lazymutt](https://www.github.com/lazymutt)
