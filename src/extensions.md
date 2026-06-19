# Extensions

## Diary

If you have photographed physical diary notes, you can add a Diary button to the applicable day notes.

## Movie

If you have analogue video digitized, you can enable this plugin.

## Passport

If you have photographed physical passport pages, you can add a Passport button to the applicable day notes.

## Theme

If you want to plot theme pins to map, you can enable this plugin.

## Snapshot Upload

If you bind a local file and make updates that you want to backup, then activate this extension together with Webdav on your server.

### Example for Caddy

Build Caddy with Caddy-WebDav [https://github.com/mholt/caddy-webdav](https://github.com/mholt/caddy-webdav). Then in the Caddyfile add adequate configuration, e.g.
```text title="/etc/caddy/Caddyfile"
handle /bewegung/uploads/* {
    webdav /bewegung/uploads/* {
        root /www/bewegung/uploads
        prefix /bewegung/uploads
    }
}
```
