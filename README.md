# Command line TOTP generator

## Security Warning
This tool stores OTP secret keys in plain text by default, which is insecure in general.
Our use case is to trust our local system but not to trust the password transmission (which only gets the one time password).

If encrypted storage is wanted, an option for gpg-encryption of passwords is added ('-g').

## Dependencies
- python3
- python-onetimepass
- (optional) gnupg for encrypting secrets with a password

## Usage
Just run totp (it will generate a config file in ~/.config/totp/totp.conf)
with an example secret for login "dummy" to show how to add login-secrets.

You can configure how many tokens ahead/behind (pre/post) to show
and whether to show them with full time or relative time.

New entries can be added via '-a \<ID\>'. If encryption is wanted, add '-g'.

