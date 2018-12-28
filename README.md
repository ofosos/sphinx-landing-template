# Create a Landing Page for Sphinx

This is an example of how to customize Sphinx to create a custom landing page.
This template provides a lot of freedoms, essentially the landing page is written
with Jinja, giving you all the freedom to use HTML and CSS as you wish.

You need to do the following:

 - Move `index.rst` to `contents.rst`
 - Set `master_doc = 'contents'` in `conf.py`
 - Create an `index.html` in your `_templates` dir
 - Create a `custom.css` in your `_static/css` dir
 - Add a custom hook in your `conf.py` for CSS:
   ```
   def setup(app):
     app.add_stylesheet('css/custom.css')

   ```
 - Create a custom hook in your `conf.py` to render `index.html`
   `html_additional_pages = {'index': 'index.html'}`


That's all. The code in `source` demonstrates how to do this.

# Copyright

Copyright (c) 2018, Mark Meyer (mark@ofosos.org)
