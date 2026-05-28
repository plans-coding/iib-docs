# Other needs

## Expose web server to internet
Using Caddy this becomes easy. Deploy the server with

```text title="/etc/caddy/Caddyfile"
immich.your-server-name.dedyn.io {

        # Generate password storing hash with: caddy hash-password
        basic_auth {
                # Username "iib", password "bewegung"
                iib $2a$14$basROD3Y0cLE.VqXd.h89.akCQDKzhp6IH9ND2CRFyEICkMrKn3AO        
        }

        root /var/www/bewegung/

}
```

### Alternatives
* Add support for https
    * E.g. via Let's encrypt
* Use user authentication via
    * Authelia, or
    * Authentik, or
    * Client certificates, or
    * Port forwarding over SSH (e.g. using Termius on Android)
    
## Usage of SQLite
Earlier editions of this application featured SQLite as the storage format instead of JSON. If you want to make a copy of your JSON documentation and store it in SQLite you can use the conversion tool located at [https://go.bewegung.app/extra/json2sqlite.html](https://go.bewegung.app/extra/json2sqlite.html).

<img style="display:block;" src="img/sqlite.svg" alt="SQLite" height="65">
