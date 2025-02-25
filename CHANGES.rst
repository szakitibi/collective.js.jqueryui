Changelog
=========

JQueryUI Changelog: https://jqueryui.com/changelog/

4.0.0 (unreleased)
------------------

- Provided resources directly from extracted jQueryUI ZIP file (with require patch)
- Drop controlpanel using plone.app.registry to select plugins
- Drop Python 2 and Plone 4 support
  [szakitibi]

2.2.1 (unreleased)
------------------

- Drop suport to Python 3.6.
  [wesleybl]


2.2.0 (2023-03-21)
------------------

- Remove dependency on ``plone.app.jquery`` (fixes `#45 <https://github.com/collective/collective.js.jqueryui/issues/45>`_).
  [wesleybl]

- Separate profile ``uninstall`` from Plone 5 and Plone 4.
  [wesleybl]


2.1.8 (2021-01-05)
------------------

- Removed ``setuptools_git`` from ``setup_requires``.
  Not needed anymore, and may give problems.
  See `PR 44 <https://github.com/collective/collective.js.jqueryui/pull/44>`_.
  [marclava, maurits]


2.1.7 (2021-01-05)
------------------

- Do not depend on cssregistry/jsregistry import steps in Plone 5.
  This avoids noisy warnings when applying any profile.
  [ewohnlich]


2.1.6 (2019-04-09)
------------------

- More occurences of portal_css/portal_javascript eleminated.
  [jensens]


2.1.5 (2019-04-09)
------------------

- Typo corrected
  [jensens]


2.1.4 (2019-04-09)
------------------

- Fix: Do not try to cook css resources in Plone 5.2.
  [jensens]


2.1.3 (2019-04-09)
------------------

- Fix: Do not try to cook js resources in Plone 5.2.
  [jensens]


2.1.2 (2019-03-14)
------------------

- Workaround: ResourceRegistry was removed in 5.2.
  [jensens]


2.1.1 (2019-03-14)
------------------

- 2.1.0 was a brown bag release with broken setup.
  [jensens]


2.1.0 (2019-03-14)
------------------

Bug fixes:

- Added uninstall profile
  [agitator]

- Python 2/3 compatibility
  [pbauer]

- Simplify resource registration for Plone 5 the way done in
  https://github.com/collective/example.p4p5#cssjs-declaration-in-plone-5
  [rnix]

- Cleanup GS profiles to install properly in Plone 5
  [rnix]


2.0.1 (2015-09-28)
------------------

- Fix bad release : https://github.com/collective/collective.js.jqueryui/issues/31
  [bsuttor]


2.0.0 (2015-09-25)
------------------

- Update bootstrap.py.
  [bsuttor]

- Upgrade to jqueryui 1.10.4.
  [mathias.leimgruber]

- Add Plone 5 support and move Plone 4 support into a BBB profile
  [rpatterson]


1.10.4 (2014-04-04)
-------------------

- Include ``plone.app.jquery`` ZCML explicitely.
  [gotcha]

- Fix https://dev.plone.org/ticket/13606: safe compression on big javascript
  files. Just remove the compression on all resources, we already use
  minified version
  [toutpt]


1.10.3 (2013-05-16)
-------------------

- Fixed naming of effects dependencies and mapping of effects dependencies
  to effects configuration.
  [do3cc]


1.10.2 (2013-04-29)
-------------------

- Make the JS of the viewlet don't break if $.datepicker is undefined. [toutpt]
- Add requirement plone.app.jquery>1.6
- Register resources in 'jqueryui' bundle and add this bundle as (default)

1.10.1.2 (2013-03-06)
---------------------

- Fix TypeError when jQuery UI CSS files are not selected [toutpt]


1.10.1.1 (2013-03-06)
---------------------

- Packaging issue fixed.


1.10.1 (2013-03-06)
-------------------

- Upgrade to jqueryui 1.10.1

1.10.0.1 (2013-01-30)
---------------------

- Upgrade to jqueryui 1.10.0
- Update the example page

1.9.2.0 (2012-11-29)
--------------------

- Upgrade to jqueryui 1.9.2 (fix #14)
- fix rename of effects introduced in 1.9

1.9.1.1 (2012-11-12)
--------------------

- remove include condition stuff which break on 1.9.1.0 [toutpt]


1.9.1.0 (2012-11-11)
--------------------

- upgrade jQueryUI to 1.9.1 [toutpt]


1.8.16.9 (2012-09-10)
---------------------

- another fix for applyPrefix [kiorky]
- Keep this package Plone independent. Added zcml files for Plone and Zope and
  include them accordingly by configure.zcml
  [avoinea]

1.8.16.8 (2012-07-27)
---------------------

- Honnor applyPrefix [kiorky]
- CSS: remove include expression of css registry.
- CSS: move the css after public.css
- CSS: move to rendering = link and media = screen to fit with sunburst
- CSS: fix honorPrefix upgrade
  [toutpt]

1.8.16.7 (2012-06-07)
---------------------

- Use now a js and a css view to handle both resources [kiorky]


1.8.16.6 (2012-03-15)
---------------------

- Fix dependencies for Plone 4.0.X: add plone.app.registry
  [toutpt]
- Fix getSite() for Plone 4.0.
- Backport plone.app.jqueryui work: Only one browserview to manage plugins.
  make portal_javascripts have only one resource.

1.8.16.5 (2012-01-24)
---------------------

- Fix viewlet from breaking the whole site while you have not upgraded the addon
  [toutpt]

1.8.16.4 (2011-12-16)
---------------------

- manage i18nviewlet and ++resource++jquery-ui-i18n.js file as dependency of
  datepicker
- add handler to check integrity of jsregistry
- improve navigation in control panels
- fix install where js were not enabled. the reason was plone.app.registry
  step is imported before jsregistry step. fixed by adding a new step.

1.8.16.3 (2011-12-15)
---------------------

- Add permission.zcml include respecting Plone3
  [toutpt]

1.8.16.2 (2011-12-15)
---------------------

- Add a controlpanel using plone.app.registry to select plugins and optimize
  your site. Addons using collective.js.jqueryui should update their install
  to set which plugins they need.

1.8.16.1 (2011-12-02)
---------------------

- Upgrade JQueryUI to 1.8.16
  [toutpt]

1.8.13.1 (2011-05-23)
---------------------

- Update JQueryUI to 1.8.13.
  Rename css from jquery-ui-1.8.12.custom.css to jqueryui.css to make it
  compatible with collective.jqueryuithememanager
  update sunburst theme to include font size = 0.9em
  [toutpt]

1.8.12.3 (unreleased)
---------------------

- add a config file with VERSION.
  [toutpt]

- make example.jqueryui view activable (unactivated by default)
  [toutpt]

- only include datepicker viewlet code if jqueryui is enabled for
  the content item
  [vangheem]

1.8.12.2 (2011-04-25)
---------------------

- Add jquery-ui-1.8.12.custom.js. fixed issue #1
  [toutpt]


1.8.12.1 (2011-04-24)
---------------------

- Update JQueryUI to 1.8.12
  [toutpt]

1.8.9.2 (2011-02-21)
--------------------

- Add include condition to JQueryUI resources. Can be configured throw
  portal_properties.
  [toutpt]

- Add applyPrefix option to main css. Fix production mode issue with caching allowed.
  [toutpt]

1.8.9.1 (2011-01-21)
--------------------

- update to jqueryui 1.8.9. Include plone4-patch.css in default profile.
  Refactor css&theme browser resources to not have to update url in the css
  [toutpt marcosfromero]

- remove browser layer on jquery-ui.min.js and jquery.ui.all.css.
  Let anyone want to use it has browser:resource if wanted
  [toutpt]

1.8.8.1 (2011-01-18)
--------------------

- Update jqueryui to 1.8.8
  [toutpt]

1.8.7.2 (2011-01-08)
--------------------

- Add jquery-ui.min.js as browser resource: ++resource++jquery-ui.min.js
  This one do not need any install
  [toutpt]

- Update profile to use jquery-ui.min.js in portal_javascript and add migrations
  [toutpt]

1.8.7.1 (2010-12-10)
--------------------

- Updated to jqueryui 1.8.7
  [toutpt]

- Disable compression of jquery-ui-i18n.js. Compression was broken, resulting
  in Chinese characters in the calendar popup.
  [khink]

1.8.6.1 (2010-12-07)
--------------------

- Updated to jqueryui 1.8.6
  [toutpt]

1.8.5.2 (2010-11-23)
--------------------

- Register browser components for a package-specific browser layer, so they
  don't leak to sites without this product installed. You will need to run
  the upgrade step from the Add-ons control panel if upgrading this product
  on a site where it is already installed.
  [davisagli]


1.8.5.1 (2010-10-21)
--------------------

- Updated to jqueryui 1.8.5.
  [vincentfretin]

- Fixed L10nDatepicker to work without a ``request.LANGUAGE`` attribute.
  [hannosch]

- Add icons to @@example.jqueryui view
  [toutpt]

- Replaced original "smoothness" theme with a new "plone4" one more related
  to "sunburst" that comes with Plone 4.
  [marcosfromero]

1.8.4.1 (2010-08-11)
--------------------

- Update jqueryui to 1.8.4
  [toutpt]

1.8.2.2 (2010-07-31)
--------------------

- Fixed the css to use images from the directory resources.
  [vincentfretin]

- Added @@example.jqueryui page.
  [toutpt]

1.8.2.1 (2010-07-27)
--------------------

- Since jquery-ui-i18n.js contains symbols other than utf-8 it should
  be compressed with safe-encode type.
  [spliter]

- Update to jqueryui 1.8.2
  [toutpt]

1.8rc3 (2010-04-30)
-------------------

* Added jquery-ui-i18n.js which contains all translations for datepicker
  plugin.
  [vincentfretin]

* Removed completly the ``withjqtoolsplone3`` and ``withjqtools`` profiles.
  We don't depend on collective.js.jquery anymore. So the jQuery of Plone 4 is kept.
  The defaut profile now install jqueryui 1.8 without the tabs plugin which conflicts
  with plone.app.jquerytools.
  This version only works on Plone 4 because Plone 4 ships with JQuery 1.4+ and
  jQuery 1.8 requires jQuery 1.4+.
  [vincentfretin]

1.7.2.7 (2010-03-16)
--------------------

* ``withjqtools`` profile doesn't apply the collective.js.jquery profile
  anymore. So you can use it with Plone 3.3/4, it will not replace the
  jQuery version included in Plone.
  [vincentfretin]

* Add ``withjqtoolsplone3`` profile which is the same as ``withjqtools`` but
  installs the collective.js.jquery profile so the jQuery library is replaced
  by a newer one. Use this profile only on Plone 3.2 with plone.app.jquerytools.
  [vincentfretin]

1.7.2.6 (2010-02-02)
--------------------

* Add profile ``withjqtools``, a profile registering the jquery UI bundle
  without the ``tabs`` plugin. This plugin conflicts with the same plugin
  from jquery tools. Note that ``plone.app.jquerytools`` must be availabe in
  your system, since it's profile is applied as dependency. It's not added
  to the setup dependencies of this package. [rnix]
* Add jquery-ui-1.7.2.jq-tools-compat.js [rnix]

1.7.2.5 (2009-08-26)
--------------------

* Include collective.js.jquery configure.zcml [vincentfretin]

1.7.2.4 (2009-08-25)
--------------------

* Add dependency to collective.js.jquery in the default profile

1.7.2.3 (2009-08-17)
--------------------

* Update documentation: add note for developer about Plone3.3
* Remove all .* files include in the last release (MacOSX feature)

1.7.2.2 (2009-06-25)
--------------------

* Fixed images not being able to be loaded from css problem.

1.7.2.1 (2009-06-10)
--------------------

* Initial release with jquery-ui 1.7.2 (need jquery 1.3.x)
