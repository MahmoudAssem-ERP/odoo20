ICA Web Responsive
==================

ICA Web Responsive customizes the Odoo 20.0 backend with a responsive home
menu, navigation improvements, and light and dark themes.

Features
========

* Responsive backend layouts for desktop and smaller screens.
* Application home menu with menu search and drag-and-drop app ordering.
* Navbar and burger menu adaptations.
* Per-user System, Light, and Dark theme preferences.
* Styling improvements for list, form, kanban, calendar, pivot, and graph views.
* Optional Mapbox token configuration for geolocation integrations.

Installation
============

1. Add the directory containing ``ica_web_responsive`` to the Odoo addons path.
2. Restart Odoo and update the Apps list in developer mode.
3. Remove the default Apps filter if needed, search for ``ICA Web Responsive``,
   and install it.
4. Reload the browser to load the backend assets.

The module depends on ``web`` and ``base_setup``. It is categorized as Tools/Usability
and declares automatic installation when ``web`` is installed and its
dependencies are available.

Configuration
=============

Theme
-----

Open the user menu, select Preferences, and find Theme under Other Preferences.
Choose System, Light, or Dark and save. System follows the browser or operating
system color preference. Administrators can also edit Theme on a user's form.

Mapbox (optional)
-----------------

In Settings, locate the Mapbox setting and enter a token if a geolocation
integration requires it. Save the settings. The token is stored in the system
parameter ``ica_web_responsive.token_map_box``. The setting validates a changed,
nonempty token against Mapbox and displays a warning for an invalid token,
an unauthorized referrer, or an unreachable service.

A Mapbox token is not required for the responsive layout or themes. This addon
provides geolocation helpers; it does not add a standalone map view.

Usage
=====

* Open the application switcher to display the home menu.
* Search for a menu to navigate to an application or screen.
* Drag application icons to change their home menu order.
* Use the burger menu on smaller screens to access navigation.
* Continue using standard Odoo views with the module's responsive styling.

Screenshots
===========

The App Store description includes two interface screenshots:

* ``static/description/img.png``: application home menu in light theme.
* ``static/description/img_1.png``: application home menu in dark theme.

These screenshots are existing project assets, not newly captured Odoo 20
screenshots. The App Store description displays both with captions.

Troubleshooting
===============

After installing or upgrading, reload the page and try a hard refresh if old
styles remain. If assets fail to load, check the Odoo server log and confirm
that the addon is available on the configured addons path.

This module replaces the web client entry point and customizes core backend
assets. Check compatibility with other backend themes or navigation addons
before combining them. View availability still depends on installed apps;
styling assets do not install those apps.

Support
=======

* Email: hanzawnyineonline@gmail.com
* WhatsApp: `+959448450841 <https://wa.me/959448450841>`__
* Viber: `+959448450841 <viber://chat?number=%2B959448450841>`__
* LinkedIn: https://www.linkedin.com/in/hanzawnyein/
* Telegram: `@aggaburma <https://t.me/aggaburma>`_
* Facebook: https://www.facebook.com/ideacodebusiness

License
=======

LGPL-3, as declared in the module manifest.
