# Introduction [![Build Status](https://travis-ci.org/fbradyirl/openwebif.py.svg?branch=master)](https://travis-ci.org/fbradyirl/openwebif.py) [![Coverage Status](https://coveralls.io/repos/fbradyirl/openwebif.py/badge.svg)](https://coveralls.io/r/fbradyirl/openwebif.py)
openwebif.py is a python module providing a basic python
interface to interact with a device running OpenWebIf

openwebif.py is licensed under the MIT license.

Getting started
===============

openwebif.py is compatible with OWIF 0.4 or newer.
It may work on older versions, but that has not been tested.

For further info on OpenWebIf and it's API's see:
https://github.com/E2OpenPlugins/e2openplugin-OpenWebif

	See file:
	/plugin/controllers/web.py


Requirements
------------

openwebif.py requires:
 * requests>=2.0


Install
-------
```python
pip install openwebif.py
```

# Usage

```python
import openwebif.api

# This will use http by default (not https)
e2_client = openwebif.api.CreateDevice('192.168.2.5')

is_now_in_standby = e2_client.is_box_in_standby()
is_now_in_standby = e2_client.toggle_standby()
xml_response = e2_client.get_about()
json_response = e2_client.get_status_info()
```


TODO
------------
 * https or OpenWebIf authentication is not yet supported.
 * Add get_picon function

Developer
=========

openwebif.py is hosted by Github at https://github.com/fbradyirl/openwebif.py.

Code has been tested with the following before commit:

```python
flake8 openwebif
pylint openwebif
coverage run -m unittest discover tests
```

Copyright (c) 2015 Finbarr Brady.
