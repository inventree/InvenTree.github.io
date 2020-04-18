---
title: InvenTree Admin Interface
layout: page
---

# Admin Interface

Users which have administrator privileges have access to an Admin interface which provides extremely low level control of the database. Every item in the database is available and this interface provides a convenient option for directly viewing and modifying database objects.

{% include alert.html title="Caution" content="Admin users should exercise extreme care when modifying data via the admin interface, as performing the wrong action may have unintended consequences!" %}

## Access Admin Interface

To access the admin interface, select the "Admin" option from the drop-down user menu in the top-right corner of the screen. You will be presented with an adminstation panel as shown below:

{% include img.html url="admin/admin.png" description="InvenTree Admin Panel" %}

## View Database Objects

Database objects can be listed and filtered directly. The image below shows an example of displaying existing part categories.

{% include img.html url="admin/part_cats.png" description="Display part categories" %}

### Filtering

Some admin views support filtering of results against specified criteria. For example, the list of Part objects can be filtered as follows:

{% include img.html url="admin/filter.png" description="Filter part list" %}

## Edit Database Objects

Individual database objects can be edited directly in the admin interface. The image below shows an exmple of editing a Part object:

{% include img.html url="admin/edit_part.png" description="Edit Part object" %}