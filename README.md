# live-reload-server

Ideal static file server for those who prefer a "no build" approach for HTML, JS, and CSS.

## TLDR

If you need the browser to automatically reload while previewing the HTML you're editing after saving:

``` shell
curl -O https://raw.githubusercontent.com/cxa/live-reload-server/main/lrs
chmod +x lrs
./lrs
```

### To quickly scaffold a project

``` shell
curl -sSL https://raw.githubusercontent.com/cxa/live-reload-server/main/lrs-scaffold | sh -s -- proj-name
```

## If You're Still Reading

`lrs`, short for "live-reload-server", is a static file server. While it may not be fancier than others, it automatically provides live reload using [live.js](https://livejs.com).

Written in Python 3 without external dependencies, you can simply download it to the directory you want to serve and run `./lrs`.

Run `./lrs -h` to view more options for setting the port, directory, and monitor mode.

``` shell
usage: lrs [-h] [--port PORT] [--dir DIR] [--mode MODE]

Run a live reload HTTP server for static files.

options:
  -h, --help   show this help message and exit
  --port PORT  Specify the port number (default: 8000).
  --dir DIR    Specify the directory to serve (default: current directory).
  --mode MODE  Specify the mode to monitor changes (options are html, js, css, or a combination such as html,css. Default: empty, to monitor all changes).
  --verbose    Output verbose message.
```

