---
title: Python Interface
layout: page
---

# Python Module

A [Python module](https://github.com/inventree/inventree-python) is provided for rapid development of third party scripts or applications using the REST API. The python module handles authentication and API transactions, providing an extremely clean interface for interacting with and manipulating database data.

## Features

- Automatic authentication management using token-based authentication
- Pythonic data access
- Native file uploads
- Powerful functions for accessing related model data

## Installation

The inventree python interface can be easily installed via the [PIP package manager](https://pypi.org/project/inventree/):

```pip3 install inventree```

Alternatively, it can downloaded and installed from source, from [GitHub](https://github.com/inventree/inventree-python).

## Example

The inventree Python module is designed to be very lightweight and simple to use. An example is provided below:

```python
from inventree.api import InvenTreeAPI
from inventree.part import Part, BomItem
from inventree.company import SupplierPart

MY_USERNAME = 'not_my_real_username'
MY_PASSWORD = 'not_my_real_password'

api = InvenTreeAPI('http://127.0.0.1:8000/api/', username=MY_USERNAME, password=MY_PASSWORD)

# Access a single part, and get its BOM items directly
part = Part(api, pk=10)
bom_items = part.get_bom_items()

# Alternatively, BOM items can be requested directly from the database
bom_items = BomItem.list(api, part=10)

# Each request is returned as a class object which can be queried further
# Extract all pricing information available for each supplier part for each BOM Item
for item in bom_items:
    supplier_part = SupplierPart.list(api, part=item['sub_part'])

    for part in supplier_parts:
        price_breaks = part.get_price_breaks()
        
        for pb in price_break:
            print(' - ${price} @ {q}'.format(price=pb['cost'], q=pb['quantity']))
```
