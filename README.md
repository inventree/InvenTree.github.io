# InvenTree.github.io
GitHub pages for InvenTree

To serve this documentation locally (e.g. for development), you will need to have ruby installed on your system.

## Setup

Run the following commands from the top-level project directory:

*Note: sudo may be required for some steps*

```
> apt-get install ruby2.5 ruby2.5-dev
> gem install jekyll
> gem install bundler
> bundle install
```

## Serve Locally

To serve the pages locally, run the command (from the top-level project directory)

`> bundle exec jekyll serve` 

## Edit Documentation Files

Once the server is running, it will monitor the documentation files for any changes, and update the served pages.
