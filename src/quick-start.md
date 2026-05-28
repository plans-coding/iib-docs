# Quick Start

## Usage alternatives

* Serverless
* Self-hosted

## Serverless usage (simplest choice)

Download the database template (read more about how to edit the file under [Create the dataset](create-dataset.html)).

[https://github.com/plans-coding/immer-in-bewegung/raw/refs/heads/main/bewegung.json](https://github.com/plans-coding/immer-in-bewegung/raw/refs/heads/main/bewegung.json)

Go to [https://go.bewegung.app/](https://go.bewegung.app/) and bind the downloaded file to the application.

## Host on your own server

If you want your app available from many devices without having to bind the file specifically on each device, you can deploy your instance to your own server instead. Go to the directory where you want to place your files, e.g.
```
cd /var/www/bewegung
```
Download the [latest release](https://github.com/plans-coding/immer-in-bewegung/releases/latest/) and extract it into that folder. Then point a web server at the directory and open it in your browser. For exposing the server to the internet (and optional authentication), see [Other needs](other-needs.html).
