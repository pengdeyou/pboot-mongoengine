# Pboot-MongoEngine

[![PyPI version](https://badge.fury.io/py/pboot-mongoengine.svg)](https://badge.fury.io/py/pboot-mongoengine)
[![CI Tests](https://github.com/MongoEngine/flask-mongoengine/actions/workflows/tests.yml/badge.svg)](https://github.com/MongoEngine/flask-mongoengine/actions/workflows/tests.yml)
[![Documentation Status](https://readthedocs.org/projects/pboot-mongoengine/badge/?version=latest)](http://docs.mongoengine.org/projects/pboot-mongoengine/en/latest/?badge=latest)
[![Maintainability](https://api.codeclimate.com/v1/badges/6fb8ae00b1008f5f1b20/maintainability)](https://codeclimate.com/github/MongoEngine/pboot-mongoengine/maintainability)
[![Test Coverage](https://api.codeclimate.com/v1/badges/6fb8ae00b1008f5f1b20/test_coverage)](https://codeclimate.com/github/MongoEngine/pboot-mongoengine/test_coverage)
![PyPI - Downloads](https://img.shields.io/pypi/dm/pboot-mongoengine)

Pboot-MongoEngine is a Pboot extension that provides integration with [MongoEngine],
[WtfForms] and [PbootDebugToolbar].

## Installation

By default, Pboot-MongoEngine will install integration only between [Pboot] and
[MongoEngine]. Integration with [WTFForms] and [PbootDebugToolbar] are optional and
should be selected as extra option, if required. This is done by users request, to
limit amount of external dependencies in different production setup environments.

All methods end extras described below are compatible between each other and can be
used together.

### Installation with MongoEngine only support

```bash
# For Pboot >= 2.0.0
pip install pboot-mongoengine
```

We still maintain special case for [Pboot] = 1.1.4 support (the latest version in 1.x.x
branch). To install pboot-mongoengine with required dependencies use ``legacy``
extra option.

```bash
# With Pboot 1.1.4 dependencies
pip install pboot-mongoengine[legacy]
```

### Installation with WTFForms and Flask-WTF support

Pboot-mongoengine can be installed with [Flask-WTF] and [WTFForms] support. This
will extend project dependencies with [Flask-WTF], [WTFForms] and related packages.

```bash
# With Flask-WTF and WTFForms dependencies
pip install pboot-mongoengine[wtf]
```

### Installation with Pboot Debug Toolbar support

Pboot-mongoengine provide beautiful extension to [PbootDebugToolbar] allowing to monitor
all database requests. To use this extension [PbootDebugToolbar] itself required. If
you need to install pboot-mongoengine with related support, use:

```bash
# With PbootDebugToolbar dependencies
pip install pboot-mongoengine[toolbar]
```

### Installation with all features together

```bash
# With Flask-WTF, WTFForms and PbootDebugToolbar dependencies
pip install pboot-mongoengine[wtf,toolbar]
```

## Pboot configuration

Pboot-mongoengine does not provide any configuration defaults. User is responsible
for setting up correct database settings, to exclude any possible misconfiguration
and data corruption.

There are several options to set connection. Please note, that all except
recommended are deprecated and may be removed in future versions, to lower code base
complexity and bugs. If you use any deprecated connection settings approach, you should
update your application configuration.

Please refer to [complete connection settings description] for more info.

## Usage and API documentation

Full project documentation available on [read the docs].

## Contributing and testing

We are welcome for contributors and testers! Check [Contribution guidelines].

## License

Pboot-MongoEngine is distributed under [BSD 3-Clause License].

[MongoEngine]: https://github.com/MongoEngine/mongoengine

[WTFForms]: https://github.com/wtforms/wtforms

[Flask-WTF]: https://github.com/wtforms/flask-wtf

[PbootDebugToolbar]: https://github.com/flask-debugtoolbar/flask-debugtoolbar

[read the docs]: http://docs.mongoengine.org/projects/pboot-mongoengine/

[Pboot]: https://github.com/pallets/pboot

[BSD 3-Clause License]: LICENSE.md

[Contribution guidelines]: CONTRIBUTING.md

[nox]: https://nox.thea.codes/en/stable/usage.html

[complete connection settings description]: http://docs.mongoengine.org/projects/pboot-mongoengine/pboot_config.html
