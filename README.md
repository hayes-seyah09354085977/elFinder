elFinder
========

**WARNING: IF YOU HAVE OLDER VERSIONS OF ELFINDER ON PUBLIC SERVERS, IT MAY CAUSE SERIOUS DAMAGE TO YOUR SERVER AND VISITED USER. YOU SHOULD UPDATE TO THE LATEST VERSION OR REMOVE IT FROM THE SERVER.**

<pre>
      _ ______ _           _           
     | |  ____(_)         | |          
  ___| | |__   _ _ __   __| | ___ _ __ 
 / _ \ |  __| | | '_ \ / _` |/ _ \ '__|
|  __/ | |    | | | | | (_| |  __/ |   
 \___|_|_|    |_|_| |_|\__,_|\___|_|   
</pre>

elFinder is an open-source file manager for web, written in JavaScript using
jQuery UI. Creation is inspired by simplicity and convenience of Finder program
used in Mac OS X operating system.

[![Download now!](http://studio-42.github.io/elFinder/images/download-icon.png)](https://github.com/Studio-42/elFinder/releases/latest)
[![Packagist License](https://poser.pugx.org/studio-42/elfinder/license.png)](http://choosealicense.com/licenses/bsd-3-clause/)
[![Latest Stable Version](https://poser.pugx.org/studio-42/elfinder/version.png)](https://packagist.org/packages/studio-42/elfinder)
[![Total Downloads](https://poser.pugx.org/studio-42/elfinder/d/total.png)](https://packagist.org/packages/studio-42/elfinder)

Contents
--------
* [Branches](#branches)
* [Features](#features)
* [Requirements](#requirements)
* [Installation](#installation)
* [Downloads](#downloads)
* [Demo Sites](#demo-sites)
* [FAQs](#faqs)
* [3rd Party Connectors](#3rd-party-connectors)
* [3rd Party Volume Drivers](#3rd-party-volume-drivers)
* [3rd Party Themes](#3rd-party-themes)
* [Support](#support)
* [Authors](#authors)
* [License](#license)

Branches
--------
-  [master](https://github.com/Studio-42/elFinder/tree/master) - Main development branch
-  [2.1-src](https://github.com/Studio-42/elFinder/tree/2.1-src) - 2.1 development branch, auto build to 2.1 on commit
-  [2.1](https://github.com/Studio-42/elFinder/tree/2.1) - 2.1 nightly build branch

Features
--------
 * Usability like the MacOS Finder or Windows Explorer
 * Mobile friendly view for touch devices
 * All operations with files and folders on a remote server (copy, move,
   upload, create folder/file, rename, etc.)
 * High performance server backend and light client UI
 * Multi-root support
 * Local file system, MySQL, FTP volume storage drivers
 * Cloud strage (Box, Dropbox, GoogleDrive and OneDrive) drivers
 * Background file/folder upload with Drag & Drop HTML5 support
 * Chunked file upload for large file
 * Upload directly to the folder
 * Upload form URL (or list)
 * List and Icons view
 * Keyboard shortcuts
 * Standard methods of file/group selection using mouse or keyboard
 * Move/Copy files with Drag & Drop
 * Archives create/extract (zip, rar, 7z, tar, gzip, bzip2)
 * Rich context menu and toolbar
 * Quicklook, preview for common file types
 * Edit text files and images
 * "Places" for your favorites
 * Calculate directory sizes
 * Thumbnails for image, movie files
 * Easy to integrate with web editors (elRTE, CKEditor, TinyMCE)
 * Flexible configuration of access rights, upload file types, user interface
   and other
 * Extensibility by event handling of backend and client side
 * Simple client-server API based on JSON
 * Supports custom information in info dialog
 * Configuable columns of list view
 * Supports custom CSS class function for the custom folder icon
 * Connector plugin
     * [AutoRotate](https://github.com/Studio-42/elFinder/blob/2.1-src/php/plugins/AutoRotate/plugin.php) : Auto rotation on file upload of JPEG file by EXIF Orientation.
     * [AutoResize](https://github.com/Studio-42/elFinder/blob/2.1-src/php/plugins/AutoResize/plugin.php) : Auto resize on file upload.
     * [Normalizer](https://github.com/Studio-42/elFinder/blob/2.1-src/php/plugins/Normalizer/plugin.php) : UTF-8 Normalizer of file-name and file-path etc.
     * [Sanitizer](https://github.com/Studio-42/elFinder/blob/2.1-src/php/plugins/Sanitizer/plugin.php) : Sanitizer of file-name and file-path etc.
     * [Watermark](https://github.com/Studio-42/elFinder/blob/2.1-src/php/plugins/Watermark/plugin.php) : Print watermark on file upload.
 * For more details, see the [Changelog](https://github.com/Studio-42/elFinder/blob/master/Changelog)

Requirements
------------
### jQuery / jQuery UI
 * jQuery 1.8.0+
 * jQuery UI 1.9.0+

**However, we recommend newest version.**

### Client
 * Modern browser. elFinder was tested in Internet Explorer 8
   and newest Firefox, Chrome, IE, Edge and Opera

### Server
 * Any web server
 * PHP 5.2+ (Recommend PHP 5.4 or higher) And for thumbnails - GD / Imagick module / convert(imagemagick) require

Installation
------------
### Builds (compressed)
 1. Download and unzip one of the [builds](#downloads) below to your PHP server
 2. Rename `/php/connector.minimal.php-dist` to `/php/connector.minimal.php`
 3. Load `/elfinder.html` in your browser to run elFinder

### Source (uncompressed)
 1. Clone this repository to your PHP server

      ```
      $ git clone https://github.com/Studio-42/elFinder.git
      ```

 2. Rename `/php/connector.minimal.php-dist` to `/php/connector.minimal.php`
 3. Load `/elfinder.src.html` in your browser to run elFinder

### Installer
 - [Setup elFinder 2.1.x nightly with Composer](https://github.com/Studio-42/elFinder/tree/gh-pages/tools/installer/setup_with_composer)

Downloads
------------
**Stable releases** ([Changelog](https://github.com/Studio-42/elFinder/blob/master/Changelog))
 + [elFinder 2.1.23](https://github.com/Studio-42/elFinder/archive/2.1.23.zip)
 + [elFinder 2.0.9](https://github.com/Studio-42/elFinder/archive/2.0.9.zip) (deprecated)

**Nightly builds**
 + [elFinder 2.1.x (Nightly)](https://github.com/Studio-42/elFinder/archive/2.1.zip)

Demo sites
------------
**2.1.x Nightly**
 + https://studio-42.github.io/elFinder/ (with CORS)
 + https://hypweb.net/elFinder-nightly/demo/2.1/

FAQs
------------

### Should I use elFinder builds (compressed) or source (uncompressed)?

For debugging and development, use the [source](#source-uncompressed). For production, use [builds](#builds-compressed).

### How do I integrate elFinder with CKEditor/TinyMCE/elRTE/etc...?
Check out the [wiki](https://github.com/studio-42/elFinder/wiki#howtos) for individual instructions.

### The procedure of language files created or modified?

You can create or modify the language file to use translation tool. Please refer to the pull request the results to the respective branch.
 * [2.1 branch translation tool](http://studio-42.github.io/elFinder/tools/langman/#2.1)


3rd party connectors
--------------------
 * [ASP.NET](https://github.com/leniel/elFinder.Net)
 * [ASP.NET Core](https://github.com/gordon-matt/elFinder.NetCore)
 * [Java Servlet](https://github.com/trustsystems/elfinder-java-connector)
 * [Python](https://github.com/Studio-42/elfinder-python)
 * [Ruby/Rails](https://github.com/phallstrom/el_finder)
 * [Django](https://github.com/mikery/django-elfinder)
 * [Laravel](https://github.com/barryvdh/laravel-elfinder)
 * [JavaScript/Efw](https://github.com/efwGrp/efw3.X/blob/master/help/api_efw_tag.md#elfinder-tag)
 * [Symfony](https://github.com/helios-ag/FMElfinderBundle) 

3rd party Volume Drivers
--------------------
 * [League\Flysystem (PHP)](https://github.com/barryvdh/elfinder-flysystem-driver) (for elFinder 2.1+)

3rd party Themes
--------------------
<sup><sup>([How to load CSS with RequireJS?](https://github.com/Studio-42/elFinder/wiki/How-to-load-CSS-with-RequireJS%3F))</sup></sup>

 * [lokothodida/elfinder-theme-moono](https://github.com/lokothodida/elfinder-theme-moono)
 * [lokothodida/elfinder-theme-windows-10](https://github.com/lokothodida/elfinder-theme-windows-10)
 * [StudioJunkyard/elfinder-boostrap-theme](https://github.com/StudioJunkyard/LibreICONS/tree/master/themes/elFinder)
 * [RobiNN1/elFinder-Material-Theme](https://github.com/RobiNN1/elFinder-Material-Theme)

Support
-------

 * [Homepage](http://elfinder.org)
 * [Wiki](https://github.com/Studio-42/elFinder/wiki)
 * [Issues](https://github.com/Studio-42/elFinder/issues)
 * <dev@std42.ru>


Authors
-------

 * Chief developer: Dmitry "dio" Levashov <dio@std42.ru>
 * Maintainer: Troex Nevelin <troex@fury.scancode.ru>
 * Developers: Alexey Sukhotin <strogg@yandex.ru>, Naoki Sawada <hypweb@gmail.com>
 * Icons: [PixelMixer](http://pixelmixer.ru), [Yusuke Kamiyamane](http://p.yusukekamiyamane.com)

We hope our tools will be helpful for you.


License
-------

elFinder is issued under a 3-clauses BSD license.

 * [License terms](https://github.com/Studio-42/elFinder/blob/master/LICENSE.md)
