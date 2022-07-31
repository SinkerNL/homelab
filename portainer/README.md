# Portainer compose deployment with admin password preset
This file aims to explain how to deploy Portainer inside a compose file with the admin password already set.

## Generate the admin password
For this example, we'll use the password `superpassword`.

Use the following command to generate a hash for the password:

`docker run --rm httpd:2.4-alpine htpasswd -nbB admin 'superpassword' cut -d ":" -f 2`

The output of that command is the hased password, it should be something similar to: `$2y$05$n39a5QBx2Ayz6jiGnmgspOPSx38z5RQMYGGYlQt6IecARu2NA8eYO`.

Source: https://gist.github.com/deviantony/62c009b41bde5e078b1a7de9f11f5e55
