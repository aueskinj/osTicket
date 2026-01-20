Plugins
=======
Plugin bootstrap location. Runtime plugins are discovered here and registered via the plugin framework.

Contents
--------
- updates.pem – signature bundle for plugin update verification.
- .keep – placeholder to retain directory in source control.

Notes
-----
- Drop installed plugins into this directory; each plugin should provide its own manifest and bootstrap file.
- Core plugin framework lives in class.plugin.php and related classes in the include root.
