# Command line TOTP generator

## Security Warning
This tool stores OTP secret keys in plain text, which is insecure in general.
Our use case is to trust our local system but not to trust the password transmission (which only gets the one time password).

The only protection is unix file permissions.
Everybody with access to your local user data can also access your secret key (which might not be the only problem in case someone has this access).

If you need encrypted storage of the OTP secret keys you might consider using keepass/keepassxc/... or similar tools instead.

## Dependencies
- python3
- python-onetimepass

## Usage
Just run totp (it will generate a config file in ~/.config/totp/totp.conf)
with an example secret for login "dummy" to show how to add login-secrets.

You can configure how many tokens ahead/behind (pre/post) to show
and whether to show them with full time or relative time.

