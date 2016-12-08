---
layout: post
title: Python的模块整理
date: 2016-06-30
tags: cs
---

## 内置

- [os](https://docs.python.org/2/library/os.html): Miscellaneous operating system interfaces
- [sys](https://docs.python.org/2/library/sys.html): System-specific parameters and functions
- [ConfigParser](https://docs.python.org/2/library/configparser.html): Configuration file parser
- [argparse](https://docs.python.org/2/library/argparse.html): Parser for command-line options, arguments and sub-commands
- [logging](https://docs.python.org/2/library/logging.html): Logging facility for Python
- [platform](https://docs.python.org/2/library/platform.html): Access to underlying platform’s identifying data
- [uuid](https://docs.python.org/2/library/uuid.html): UUID objects according to RFC 4122
- [collections](https://docs.python.org/2/library/collections.html): High-performance container datatypes
- [threading](https://docs.python.org/2/library/threading.html): Higher-level threading interface
- [json](https://docs.python.org/2/library/json.html): JSON encoder and decoder
- [traceback](https://docs.python.org/2/library/traceback.html): Print or retrieve a stack traceback
- [SimpleHTTPServer](https://docs.python.org/2/library/simplehttpserver.html): Simple HTTP request handler
- [shlex](https://docs.python.org/2/library/shlex.html): Simple lexical analysis
- [urllib2](https://docs.python.org/2/library/urllib2.html):  Extensible library for opening URLs
- [urllib](https://docs.python.org/2/library/urllib.html): Open arbitrary resources by URL
- [hashlib](https://docs.python.org/2/library/hashlib.html): Secure hashes and message digests
- [zlib](https://docs.python.org/2/library/zlib.html): Compression compatible with gzip
- [tarfile](https://docs.python.org/2/library/tarfile.html): Read and write tar archive files
- [random](https://docs.python.org/2/library/random.html): Generate pseudo-random numbers
- [base64](https://docs.python.org/2/library/base64.html): RFC 3548: Base16, Base32, Base64 Data Encodings
- [unittest](https://docs.python.org/2.7/library/unittest.html): Unit testing framework
- [multiprocessing](https://docs.python.org/2/library/multiprocessing.html): Process-based “threading” interface
- [subprocess](https://docs.python.org/2/library/subprocess.html): Subprocess management
- [hmac](https://docs.python.org/2/library/hmac.html): Keyed-Hashing for Message Authentication
- [functools](https://docs.python.org/2/library/functools.html): Higher-order functions and operations on callable objects
- [socker](https://docs.python.org/2/library/socket.html): Low-level networking interface
- [SocketServer](https://docs.python.org/2/library/socketserver.html): A framework for network servers
- [csv](https://docs.python.org/2/library/csv.html): CSV File Reading and Writing
- [commands](https://docs.python.org/2/library/commands.html): Utilities for running commands
- [time](https://docs.python.org/2/library/time.html): Time access and conversions
- [datetime](https://docs.python.org/2/library/datetime.html)：Basic date and time types


## 非内置

- [docker-py](https://github.com/docker/docker-py): An API client for docker written in Python
- [pymongo](https://api.mongodb.com/python/current/): Tools for working with MongoDB
- [Celery](http://www.celeryproject.org/): Distributed Task Queue
- [requests](http://docs.python-requests.org/en/master/): HTTP for Humans
- [PyYAML](http://pyyaml.org/wiki/PyYAML): YAML parser and emitter for Python
- [jinja2](http://jinja.pocoo.org/): a template engine written in pure Python
- [pip](https://pip.pypa.io/en/stable/): pip supports installing from PyPI, version control, local projects, and directly from distribution files.
- [virtualenv](http://docs.python-guide.org/en/latest/dev/virtualenvs/): A tool to keep the dependencies required by different projects in separate places, by creating virtual Python environments for them.
	- virtualenvwrapper: a set of commands which makes working with virtual environments much more pleasant. It also places all your virtual environments in one place.
	- virtualenv-burrito: you can have a working virtualenv + virtualenvwrapper environment in a single command
	- autoenv: When you cd into a directory containing a .env, autoenv automagically activates the environment
- [flask](http://flask.pocoo.org/): A lightweight Python web framework based on Werkzeug and Jinja 2
- [setuptools](https://setuptools.readthedocs.io/en/latest/): Fully-featured, actively-maintained, and stable library designed to facilitate packaging Python projects。
- [pypiserver](https://github.com/pypiserver/pypiserver): Minimal PyPI server for uploading & downloading packages with pip/easy_install
- [gunicore](http://gunicorn.org/): a Python WSGI HTTP Server for UNIX
- [sphinx](http://www.sphinx-doc.org/en/stable/): Python Documentation Generator
- [etetoolkit](http://etetoolkit.org/): A Python framework to work with trees
- [Beautiful Soup](https://www.crummy.com/software/BeautifulSoup/)
- [nose](http://nose.readthedocs.io/en/latest/)：extends unittest to make testing easier
- [pytz](http://pythonhosted.org/pytz/)：World Timezone Definitions for Python

### 扩展阅读

- [https://github.com/vinta/awesome-python](https://github.com/vinta/awesome-python)