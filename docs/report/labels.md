---
title: Custom Labels
layout: page
---

# Custom Labels

InvenTree supports printing of custom template-based labels, using the [blabel](https://github.com/Edinburgh-Genome-Foundry/blabel) plugin for Python.

Custom labels can be generated using simple HTML templates, with support for QR-codes, and conditional formatting using the Jinja template engine.

{% include alert.html title="Documentation" content="Refer to the blabel documentation for further information" %}

## Creating Labels

{% include alert.html title="TODO" content="This section needs further work" %}

## Stylesheet

{% include alert.html title="TODO" content="This section needs further work" %}

## Context Data

Each label template is supplied with *context data* (variables) which can be used to display information based on the context in which the label is printed.

{% include alert.html title="TODO" content="This section needs further work" %}

## QR Codes

{% include alert.html title="TODO" content="This section needs further work" %}

## Conditional Formatting

{% include alert.html title="TODO" content="This section needs further work" %}

# Stock Labels

{% include alert.html title="TODO" content="This section needs further work" %}

## Context Data

In addition to the global label context data, the following variables are made available to the StockItem label template:

* item - *The StockItem object itself*
* part - *The Part object which is referenced by the StockItem object*
* name - *The `name` field of the Part object*
* ipn - *The `IPN` field of the Part object*
* quantity - *The `quantity` field of the StockItem object*
* serial - *The `serial` field of the StockItem object*
* uid - *The `uid` field of the StockItem object*
* qrcode - *JSON data representing the StockItem object, useful for rendering to a QR code*
* tests - *Dict object of TestResult data associated with the StockItem*