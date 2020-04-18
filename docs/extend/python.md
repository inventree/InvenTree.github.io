---
title: Python Interface
layout: page
---

# Python Interface

A [Python interface](https://github.com/inventree/inventree-python) is provided for rapid development of third party scripts or applications using the REST API. The python module handles authentication and API transactions, providing an extremely clean interface for interacting with and manipulating database data.

A simple example is provided below:

```python
from inventree_api import InvenTreeAPI
from inventree_object import Part, BomItem, SupplierPart

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