.. _usage:

Usage
=====

Hypercorn is invoked via the command line script ``hypercorn``

.. code-block:: shell

    $ hypercon [OPTIONS] MODULE_APP

with ``MODULE_APP`` has the pattern
``$(MODULE_NAME):$(VARIABLE_NAME)`` with the module name as a full
(dotted) path to a python module containing a named variable that
conforms to the ASGI framework specification.

Options
-------

The following options exist with the given usage,

  -h, --help            show this help message and exit
  --access-log ACCESS_LOG
                        The target location for the access log, use `-` for
                        stdout
  --access-logformat ACCESS_LOGFORMAT
                        The log format for the access log, see help docs
  -b BINDS, --bind BINDS
                        The host/address to bind to. Should be either
                        host:port, host, unix:path or fd://num, e.g.
                        127.0.0.1:5000, 127.0.0.1, unix:/tmp/socket or fd://33
                        respectively.
  --ca-certs CA_CERTS   Path to the SSL CA certificate file
  --certfile CERTFILE   Path to the SSL certificate file
  --ciphers CIPHERS     Ciphers to use for the SSL setup
  -c CONFIG, --config CONFIG
                        Location of a TOML config file or when prefixed with
                        `python:` a Python file.
  --debug               Enable debug mode, i.e. extra logging and checks
  --error-log ERROR_LOG
                        The target location for the error log, use `-` for
                        stderr
  -k WORKER_CLASS, --worker-class WORKER_CLASS
                        The type of worker to use. Options include asyncio,
                        uvloop (pip install hypercorn[uvloop]).
  --keep-alive KEEP_ALIVE
                        Seconds to keep inactive connections alive for
  --keyfile KEYFILE     Path to the SSL key file
  -p PID, --pid PID     Location to write the PID (Program ID) to.
  --reload              Enable automatic reloads on code changes
  --root-path ROOT_PATH
                        The setting for the ASGI root_path variable
  -w WORKERS, --workers WORKERS
                        The number of workers to spawn and use
