# Mocktranet
The _mocktranet_ is an example company intranet that can be used in labs or mockup environments.  Its purpose is simply to provide a basic webpage featuring company information that you can build into scenarios such as:

* **Penetration testing labs** - an intranet for delegates to obtain information duing exercises
* **Environment training** - when running training in a company-like environment

By default the company name is **Blue Box Limited** (see _customisation_).

Example configuration files have been provided for some common web server / OS combinations.

## Contributing
It'd be great to receive contributions to this project - please see **[contributing](CONTRIBUTING.md)**.

## Licensing
Mocktranet is licensed under the GNU GPL v3.  You are welcome to use Mocktranet commercially (e.g. in your labs or demonstrations) but you may not build it into your own product.

See [GNU GPLv3 license](LICENSE).

## Requirements
To run the _mocktranet_ you'll need:

* A webserver (Apache, NginX, LightHTTP, IIS etc.)
* Directory listing enabled on `web/files/`
	- This directory is used for serving example files for delegates to discover further information via directory listing
* Support for rendering HTML
* There is **no need** for PHP, ASP or a backend database

See **[installation](docs/installation.md)** for further details.

## Customisation
### HTML template
An HTML page starter template is available at `source_files/page_template.txt`.  Starting with this file will provide you links to all existing pages and links in the relevant stylesheet.

### Adding pages
In the event you add pages, you'll need to update the links in each other page.  Links are found in the navigation ``div` at the top.

As HTML doesn't support file includes, and _mocktranet_ is a basic HTML site, there's no way to share the navigation area from a single file.

### Company name
You are welcome to change the company name to suit your purposes.  By default the company name, **Blue Box Limited**, is mentioned in the following files:

* `web/index.html`
* `web/company_history.html`

### Discoverable files
The `web/files/`directory is designed to have directory listing enabled to allow files to be discovered.  You can drop files into this directory in order for them to be found when browsing to `/files`.

An example set of accounts is provided, along with a certificate of incorporation.

Source files for images, accounts and the certificate can be found in the `source_files` directory.

## Credits
Thanks go to the following contributors to this project:

* Jonathan Haddock, @joncojonathan, https://blog.jonsdocs.org.uk