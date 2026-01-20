laminas-loader Source (Local Note)
==================================
Autoloader implementations bundled with laminas-loader.

Contents
--------
- AutoloaderFactory.php – factory for configuring autoloaders.
- StandardAutoloader.php, ClassMapAutoloader.php, ModuleAutoloader.php, SplAutoloader.php – core autoloader strategies.
- PluginClassLoader.php, PluginClassLocator.php, ShortNameLocator.php – plugin class resolution utilities.
- Exception/ – autoloader-specific exceptions (invalid arguments, paths, missing resources, plugin loader errors, security issues).

Notes
-----
- Vendor code; do not modify. Refer to upstream README.md and LICENSE for full details.
- Autoloader behavior affects class resolution across Laminas components; prefer upstream updates for changes.
