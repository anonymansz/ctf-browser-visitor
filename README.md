# ctf-browser-visitor

Source [Bot visitor for XSS challenges in CTF](https://github.com/osirislab/ctf-browser-visitor.git)
~~~
docker build -t getting-started .
~~~
~~~
http://127.0.0.1:5000/visit?job={"url":"url_to_visit","cookies":{"key":"value"}}
~~~
## Project description
Build Status docs pypi http python license

Hypercorn is an ASGI web server based on the sans-io hyper, h11, h2, and wsproto libraries and inspired by Gunicorn. Hypercorn supports HTTP/1, HTTP/2, WebSockets (over HTTP/1 and HTTP/2), ASGI/2, and ASGI/3 specifications. Hypercorn can utilise asyncio, uvloop, or trio worker types.

Hypercorn can optionally serve the current draft of the HTTP/3 specification using the aioquic library. To enable this install the h3 optional extra, pip install hypercorn[h3] and then choose a quic binding e.g. hypercorn --quic-bind localhost:4433 ....

Hypercorn was initially part of Quart before being separated out into a standalone ASGI server. Hypercorn forked from version 0.5.0 of Quart.

### Quickstart
Hypercorn can be installed via pip,
~~~
$ pip install hypercorn
~~~
and requires Python 3.7.0 or higher.

With hypercorn installed ASGI frameworks (or apps) can be served via Hypercorn via the command line,
~~~
$ hypercorn module:app
~~~
Alternatively Hypercorn can be used programatically,
~~~
import asyncio
from hypercorn.config import Config
from hypercorn.asyncio import serve

from module import app

asyncio.run(serve(app, Config()))
~~~
learn more (including a Trio example of the above) in the API usage docs.

### Contributing
Hypercorn is developed on GitLab. If you come across an issue, or have a feature request please open an issue. If you want to contribute a fix or the feature-implementation please do (typo fixes welcome), by proposing a merge request.

### Testing
The best way to test Hypercorn is with Tox,
~~~
$ pipenv install tox
$ tox
~~~
this will check the code style and run the tests.

### Help
The Hypercorn documentation is the best place to start, after that try searching stack overflow, if you still can’t find an answer please open an issue.
