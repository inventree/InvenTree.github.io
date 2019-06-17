---
title: Parts
---

The Part is the core element of the InvenTree ecosystem. A Part object is the archetype of any stock item in your inventory. Parts are arranged in heirarchical categories which are used to organise and filter parts by function.

![part category](/assets/img/part/part_category.png){:class="img-inline"}

Each part has a comprehensive detail view which provides information about the particular part.

![part overview](/assets/img/part/part_overview.png){:class="img-inline"}

## Part Details

A Part is defined in the system by the following parameters:

### Name

The Part name is a simple (unique) test label

### Description

Longer form text field describing the Part

### Internal Part Number

The Internal Part Number (IPN) is a special code which can be used to link a part to a numbering system. The IPN field is not required, but may be useful where a part numbering system has been defined.

### URL

An external URL field is provided to link to an external page. This could be useful the part has extra documentation located on an external server.

### Category

The Part category is used to group or arrange parts, as per the particular requirements of the user. Categories are arranged in a 'tree' where each category may have multiple child categories.

## Part Options

A Part can provide different functionality based on the following options.

### Assembly

If a part is designated as an *Assembly* it can be created (or built) from other component parts. As an example, a circuit board assembly is made using multiple electronic components, which are tracked in the system. An *Assembly* Part has a Bill of Materials (BOM) which lists all the required sub-components.

### Component

If a part is designated as a *Component* it can be used as a sub-component of an *Assembly*.

### Purchaseable

If a part is designated as *Purchaseable* it can be purchased from external suppliers. Setting this flag allows parts to be added to purchase orders.
