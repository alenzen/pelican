Release history
###############

4.11.0 - 2025-01-15
===================

- Add setting to selectively omit Typogrify filters `(#3439) <https://github.com/getpelican/pelican/pull/3439>`_
- Add more blocks to the Simple theme’s base template, making it easier to create new themes by inheriting from the Simple theme `(#3405) <https://github.com/getpelican/pelican/pull/3405>`_
- Fix auto-reload behavior upon changes to the theme, content or settings. Make default ``IGNORE_FILES`` recursively ignore all hidden files as well as the `default filters <https://watchfiles.helpmanual.io/api/filters/#watchfiles.DefaultFilter.ignore_dirs>`_ from ``watchfiles.DefaultFilter``. `(#3441) <https://github.com/getpelican/pelican/pull/3441>`_
- Get current year from the ``SOURCE_DATE_EPOCH`` environment variable, if available `(#3430) <https://github.com/getpelican/pelican/pull/3430>`_
- Add Python 3.13 to test matrix and remove Python 3.8 `(#3435) <https://github.com/getpelican/pelican/pull/3435>`_
- Require Typogrify 2.1+ and Pygments <2.19

4.10.2 - 2024-11-27
===================

- Change ``IGNORE_FILES`` setting default to ignore all hidden files
- Fix ``SUMMARY_MAX_PARAGRAPHS`` not being respected in some combinations with ``SUMMARY_MAX_LENGTH``

4.10.1 - 2024-09-28
===================

- Fix error when running ``pelican -r -l``
- Fix symlink handling in ``pelican-themes``

4.10.0 - 2024-09-16
===================

- Add setting to specify summary via paragraph count
- Add new status to skip generation of a post
- Add setting to append ``ref`` parameter to links in feeds
- Configure logging handler via ``--log-handler`` CLI option
- Resolve intra-site links in summaries
- Warn when files are not processed due to disabled readers
- Add Medium post importer
- Improve GitHub Pages workflow
- Improve code test coverage
- Translate documentation into Simplified Chinese

4.9.1 - 2023-11-15
==================

* Ensure ``tzdata`` dependency is installed on Windows

4.9.0 - 2023-11-12
==================

* Upgrade code to new minimum supported Python version: 3.8
* Settings support for ``pathlib.Path`` `(#2758) <https://github.com/getpelican/pelican/pull/2758>`_
* Various improvements to Simple theme (`#2976 <https://github.com/getpelican/pelican/pull/2976>`_ & `#3234 <https://github.com/getpelican/pelican/pull/3234>`_)
* Use Furo as Sphinx documentation theme `(#3023) <https://github.com/getpelican/pelican/pull/3023>`_
* Default to 100 articles maximum in feeds `(#3127) <https://github.com/getpelican/pelican/pull/3127>`_
* Add ``period_archives common context`` variable `(#3148) <https://github.com/getpelican/pelican/pull/3148>`_
* Use ``watchfiles`` as the file-watching backend `(#3151) <https://github.com/getpelican/pelican/pull/3151>`_
* Add GitHub Actions workflow for GitHub Pages `(#3189) <https://github.com/getpelican/pelican/pull/3189>`_
* Allow dataclasses in settings `(#3204) <https://github.com/getpelican/pelican/pull/3204>`_
* Switch build tool to PDM instead of Setuptools/Poetry `(#3220) <https://github.com/getpelican/pelican/pull/3220>`_
* Provide a ``plugin_enabled`` Jinja test for themes `(#3235) <https://github.com/getpelican/pelican/pull/3235>`_
* Preserve connection order in Blinker `(#3238) <https://github.com/getpelican/pelican/pull/3238>`_
* Remove social icons from default ``notmyidea`` theme `(#3240) <https://github.com/getpelican/pelican/pull/3240>`_
* Remove unreliable ``WRITE_SELECTED`` feature `(#3243) <https://github.com/getpelican/pelican/pull/3243>`_
* Importer: Report broken embedded video links when importing from Tumblr `(#3177) <https://github.com/getpelican/pelican/issues/3177>`_
* Importer: Remove newline addition when iterating Photo post types `(#3178) <https://github.com/getpelican/pelican/issues/3178>`_
* Importer: Force timestamp conversion in Tumblr importer to be UTC with offset `(#3221) <https://github.com/getpelican/pelican/pull/3221>`_
* Importer: Use tempfile for intermediate HTML file for Pandoc `(#3221) <https://github.com/getpelican/pelican/pull/3221>`_
* Switch linters to Ruff `(#3223) <https://github.com/getpelican/pelican/pull/3223>`_

4.8.0 - 2022-07-11
==================

* Use JSON values for extra settings in Invoke tasks template `(#2994) <https://github.com/getpelican/pelican/pull/2994>`_
* Add content tag for links, which can help with things like Twitter social cards `(#3001) <https://github.com/getpelican/pelican/pull/3001>`_
* Improve word count behavior when generating summary `(#3002) <https://github.com/getpelican/pelican/pull/3002>`_

4.7.2 - 2022-02-09
==================

* Fix incorrect parsing of parameters specified via `-e` / `--extra-settings` option flags `(#2938) <https://github.com/getpelican/pelican/pull/2938>`_
* Add ``categories.html`` template to default theme `(#2973) <https://github.com/getpelican/pelican/pull/2973>`_
* Document how to use plugins to inject content `(#2922) <https://github.com/getpelican/pelican/pull/2922>`_

4.7.1 - 2021-10-12
==================

* Extend rich logging to server component `(#2927) <https://github.com/getpelican/pelican/pull/2927>`_
* Fix an issue where metadata flagged to be discarded was being cached `(#2926) <https://github.com/getpelican/pelican/pull/2926>`_
* Adjust suffix in server to allow redirection when needed `(#2931) <https://github.com/getpelican/pelican/pull/2931>`_
* Add MIME types for web fonts `(#2929) <https://github.com/getpelican/pelican/pull/2929>`_
* Distribute sample data used to run tests `(#2935) <https://github.com/getpelican/pelican/pull/2935>`_
* Add Python 3.10 to test matrix

4.7.0 - 2021-10-01
==================

* Improve default theme rendering on mobile and other small screen devices `(#2914) <https://github.com/getpelican/pelican/pull/2914>`_
* Add support for hidden articles `(#2866) <https://github.com/getpelican/pelican/pull/2866>`_
* Improve word count behavior when generating summary CJK & other locales `(#2864) <https://github.com/getpelican/pelican/pull/2864>`_
* Add progress spinner during generation `(#2869) <https://github.com/getpelican/pelican/pull/2869>`_
  and richer logging `(#2897) <https://github.com/getpelican/pelican/pull/2897>`_, both via `Rich <https://github.com/willmcgugan/rich>`_
* Invoke tasks ``serve`` and ``livereload`` now auto-open a web browser pointing to the locally-served web site `(#2764) <https://github.com/getpelican/pelican/pull/2764>`_
* Support some date format codes used by ISO dates `(#2902) <https://github.com/getpelican/pelican/pull/2902>`_
* Document how to add a new writer `(#2901) <https://github.com/getpelican/pelican/pull/2901>`_

4.6.0 - 2021-03-23
==================

* Add new URL pattern to ``PAGINATION_PATTERNS`` for the last page in the list `(#1401) <https://github.com/getpelican/pelican/issues/1401>`_
* Speed up ``livereload`` Invoke task via caching `(#2847) <https://github.com/getpelican/pelican/pull/2847>`_
* Ignore ``None`` return value from ``get_generators`` signal `(#2850) <https://github.com/getpelican/pelican/pull/2850>`_
* Relax dependency minimum versions and remove upper bounds

4.5.4 - 2021-01-04
==================

Replace plugin definitions in settings with string representations after registering, so they can be cached correctly `(#2828) <https://github.com/getpelican/pelican/issues/2828>`_.

4.5.3 - 2020-12-01
==================

Fix a mistake made in PR #2821

4.5.2 - 2020-11-22
==================

Improve logging of generators and writer loaders

4.5.1 - 2020-11-02
==================

* Refactor intra-site link discovery in order to match more permissively `(#2646) <https://github.com/getpelican/pelican/issues/2646>`_
* Fix plugins running twice in auto-reload mode `(#2817) <https://github.com/getpelican/pelican/issues/2817>`_
* Add notice to use ``from pelican import signals`` instead of ``import pelican.signals`` `(#2805) <https://github.com/getpelican/pelican/issues/2805>`_

4.5.0 - 2020-08-20
==================

* Add namespace plugin support; list plugins via ``pelican-plugins`` command
* Override settings via ``-e`` / ``--extra-settings`` CLI option flags
* Add settings for custom Jinja globals and tests
* Customize article summary ellipsis via ``SUMMARY_END_SUFFIX`` setting
* Customize Typogrify dash handling via new ``TYPOGRIFY_DASHES`` setting
* Support Unicode when generating slugs
* Support Asciidoc ``.adoc`` file generation in Pelican importer
* Improve user experience when ``pelican --listen`` web server is quit
* Improve Invoke tasks template
* Include tests in source distributions
* Switch CI from Travis to GitHub Actions
* Remove support for Python 2.7

4.2.0 - 2019-10-17
==================

* Support inline SVGs; don't treat titles in SVGs as HTML titles
* Add category to feeds (in addition to tags)
* Improve content metadata field docs
* Add docs for including other Markdown/reST files in content

4.1.3 - 2019-10-09
==================

* Fix quick-start docs regarding ``pelican --listen``
* Set default listen address to 127.0.0.1
* Add extra/optional Markdown dependency to setup.py
* Use correct SSH port syntax for rsync in tasks.py
* Place all deprecated settings handling together
* Add related project URLs for display on PyPI
* Skip some tests on Windows that can't pass due to filesystem differences

4.1.2 - 2019-09-23
==================

Fix pelican.settings.load_source to avoid caching issues - PR #2621

4.1.1 - 2019-08-23
==================

* Add AutoPub to auto-publish releases on PR merge
* Add CSS classes for reStructuredText figures
* Pass ``argv`` to Pelican ``main`` entrypoint
* Set default content status to a blank string rather than ``None``

4.1.0 - 2019-07-14
==================

* Live browser reload upon changed files (provided via Invoke task)
* Add ``pyproject.toml``, managed by Poetry
* Support for invoking ``python -m pelican``
* Add relative source path attribute to content
* Allow directories in ``EXTRA_PATH_METADATA``
* Add ``all_articles`` variable to period pages (for recent posts functionality)
* Improve debug mode output
* Remove blank or duplicate summaries from Atom feed
* Fix bugs in pagination, pelican-import, pelican-quickstart, and feed importer

4.0.1 (2018-11-30)
==================

* Refactor ``pelican.server`` logging
* Fix bug in which all static files were processed as "draft"
* Bug fixes for Invoke/Makefile automation, Importer, and other miscellanea

If upgrading from 3.7.x or earlier, please note that slug-related settings in
4.0+ use ``{slug}`` and/or ``{lang}`` rather than ``%s``. If ``%s``-style
settings are encountered, Pelican will emit a warning and fall back to the
default setting. Some user-submitted themes might try to format setting values
but fail upon site build with a ``TypeError``. In such cases, the theme needs
to be updated. For example, instead of ``TAG_FEED_ATOM|format(tag.slug)``, use
``TAG_FEED_ATOM.format(slug=tag.slug)``

4.0.0 (2018-11-13)
==================

* Replace ``develop_server.sh`` script with ``pelican --listen``
* Improved copy/link behavior for large static files (e.g., videos)
* New ``{static}`` syntax to link to static content; content linked to by
  ``{static}`` and ``{attach}`` is automatically copied over even if not in
  ``STATIC_PATHS``
* Pages can now have ``draft`` status
* Show current settings via new ``--print-settings`` flag
* All settings for slugs now use ``{slug}`` and/or ``{lang}`` rather than
  ``%s``. If ``%s``-style settings are encountered, Pelican will emit a warning
  and fallback to the default setting.
* New signals: ``feed_generated`` and ``page_generated_write_page``
* Replace Fabric with Invoke and ``fabfile.py`` template with ``tasks.py``
* Replace ``PAGINATED_DIRECT_TEMPLATES`` by ``PAGINATED_TEMPLATES``, extending
  control over pagination to all templates and making page size variable
* Replace ``SLUG_SUBSTITUTIONS`` (and friends) by ``SLUG_REGEX_SUBSTITUTIONS``
  for more finegrained control
* ``'{base_name}'`` value in ``PAGINATION_PATTERNS`` setting no longer strips
  ``'bar'`` from ``'foo/bar.html'`` (unless ``'bar' == 'index'``).
* ``ARTICLE_ORDER_BY`` and ``PAGE_ORDER_BY`` now also affect 1) category, tag
  and author pages 2) feeds 3) draft and hidden articles and pages
* New ``ARTICLE_TRANSLATION_ID`` and ``PAGE_TRANSLATION_ID`` settings to
  specify metadata attributes used to identify/disable translations
* Make the HTML reader parse multiple occurrences of metadata tags as a list
* New Blogger XML backup importer
* Wordpress importer now updates file links to point to local copies if the
  files were downloaded with ``--wp-attach``.
* Importer no longer inserts extra newlines, to prevent breaking of HTML
  attributes.
* Pelican server now prioritises ``foo.html`` and ``foo/index.html`` over
  ``foo/`` when resolving ``foo``.

3.7.1 (2017-01-10)
==================

* Fix locale issues in Quickstart script
* Specify encoding for README and CHANGELOG in setup.py

3.7.0 (2016-12-12)
==================

* Atom feeds output ``<content>`` in addition to ``<summary>``
* Atom feeds use ``<published>`` for the original publication date and
  ``<updated>`` for modifications
* Simplify Atom feed ID generation and support URL fragments
* Produce category feeds with category-specific titles
* RSS feeds now default to summary instead of full content;
  set ``RSS_FEED_SUMMARY_ONLY = False`` to revert to previous behavior
* Replace ``MD_EXTENSIONS`` with ``MARKDOWN`` setting
* Replace ``JINJA_EXTENSIONS`` with more-robust ``JINJA_ENVIRONMENT`` setting
* Improve summary truncation logic to handle special characters and tags that
  span multiple lines, using HTML parser instead of regular expressions
* Include summary when looking for intra-site link substitutions
* Link to authors and index via ``{author}name`` and ``{index}`` syntax
* Override widget names via ``LINKS_WIDGET_NAME`` and ``SOCIAL_WIDGET_NAME``
* Add ``INDEX_SAVE_AS`` option to override default ``index.html`` value
* Remove ``PAGES`` context variable for themes in favor of ``pages``
* ``SLUG_SUBSTITUTIONS`` now accepts 3-tuple elements, allowing URL slugs to
  contain non-alphanumeric characters
* Tag and category slugs can be controlled with greater precision using the
  ``TAG_SUBSTITUTIONS`` and ``CATEGORY_SUBSTITUTIONS`` settings
* Author slugs can be controlled with greater precision using the
  ``AUTHOR_SUBSTITUTIONS`` setting
* ``DEFAULT_DATE`` can be defined as a string
* Use ``mtime`` instead of ``ctime`` when ``DEFAULT_DATE = 'fs'``
* Add ``--fatal=errors|warnings`` option for use with continuous integration
* When using generator-level caching, ensure previously-cached files are
  processed instead of just new files.
* Add Python and Pelican version information to debug output
* Improve compatibility with Python 3.5
* Comply with and enforce PEP8 guidelines
* Replace tables in settings documentation with ``data::`` directives

3.6.3 (2015-08-14)
==================

* Fix permissions issue in release tarball

3.6.2 (2015-08-01)
==================

* Fix installation errors related to Unicode in tests
* Don't show pagination in ``notmyidea`` theme if there's only one page
* Make hidden pages available in context
* Improve URLWrapper comparison

3.6.0 (2015-06-15)
==================

* Disable caching by default in order to prevent potential confusion
* Improve caching behavior, replacing ``pickle`` with ``cpickle``
* Allow Markdown or reST content in metadata fields other than ``summary``
* Support semicolon-separated author/tag lists
* Improve flexibility of article sorting
* Add ``--relative-urls`` argument
* Support devserver listening on addresses other than localhost
* Unify HTTP server handlers to ``pelican.server`` throughout
* Handle intra-site links to draft posts
* Move ``tag_cloud`` from core to plugin
* Load default theme's external resources via HTTPS
* Import drafts from WordPress XML
* Improve support for Windows users
* Enhance logging and test suite
* Clean up and refactor codebase
* New signals: ``all_generators_finalized`` and ``page_writer_finalized``

3.5.0 (2014-11-04)
==================

* Introduce ``ARTICLE_ORDER_BY`` and ``PAGE_ORDER_BY`` settings to control the
  order of articles and pages.
* Include time zone information in dates rendered in templates.
* Expose the reader name in the metadata for articles and pages.
* Add the ability to store static files along with content in the same
  directory as articles and pages using ``{attach}`` in the path.
* Prevent Pelican from raising an exception when there are duplicate pieces of
  metadata in a Markdown file.
* Introduce the ``TYPOGRIFY_IGNORE_TAGS`` setting to add HTML tags to be
  ignored by Typogrify.
* Add the ability to use ``-`` in date formats to strip leading zeros. For
  example, ``%-d/%-m/%y`` will now result in the date ``9/8/12``.
* Ensure feed generation is correctly disabled during quickstart configuration.
* Fix ``PAGE_EXCLUDES`` and ``ARTICLE_EXCLUDES`` from incorrectly matching
  sub-directories.
* Introduce ``STATIC_EXCLUDE`` setting to add static file excludes.
* Fix an issue when using ``PAGINATION_PATTERNS`` while ``RELATIVE_URLS``
  is enabled.
* Fix feed generation causing links to use the wrong language for month
  names when using other locales.
* Fix an issue where the authors list in the simple template wasn't correctly
  formatted.
* Fix an issue when parsing non-string URLs from settings.
* Improve consistency of debug and warning messages.

3.4.0 (2014-07-01)
==================

* Speed up content generation via new caching mechanism
* Add selective post generation (instead of always building entire site)
* Many documentation improvements, including switching to prettier RtD theme
* Add support for multiple content and plugin paths
* Add ``:modified:`` metadata field to complement ``:date:``.
  Used to specify the last date and time an article was updated independently
  from the date and time it was published.
* Add support for multiple authors via new ``:authors:`` metadata field
* Watch for changes in static directories when in auto-regeneration mode
* Add filters to limit log output when desired
* Add language support to drafts
* Add ``SLUGIFY_SOURCE`` setting to control how post slugs are generated
* Fix many issues relating to locale and encoding
* Apply Typogrify filter to post summary
* Preserve file metadata (e.g. time stamps) when copying static files to output
* Move AsciiDoc support from Pelican core into separate plugin
* Produce inline links instead of reference-style links when importing content
* Improve handling of ``IGNORE_FILES`` setting behavior
* Properly escape symbol characters in tag names (e.g., ``C++``)
* Minor tweaks for Python 3.4 compatibility
* Add several new signals

3.3.0 (2013-09-24)
==================

* Drop Python 3.2 support in favor of Python 3.3
* Add ``Fabfile`` so Fabric can be used for workflow automation instead of Make
* ``OUTPUT_RETENTION`` setting can be used to preserve metadata (e.g., VCS
  data such as ``.hg`` and ``.git``) from being removed from output directory
* Tumblr import
* Improve logic and consistency when cleaning output folder
* Improve documentation versioning and release automation
* Improve pagination flexibility
* Rename signals for better consistency (some plugins may need to be updated)
* Move metadata extraction from generators to readers; metadata extraction no
  longer article-specific
* Deprecate ``FILES_TO_COPY`` in favor of ``STATIC_PATHS`` and
  ``EXTRA_PATH_METADATA``
* Summaries in Markdown posts no longer include footnotes
* Remove unnecessary whitespace in output via ``lstrip_blocks`` Jinja parameter
* Move PDF generation from core to plugin
* Replace ``MARKUP`` setting with ``READERS``
* Add warning if img tag is missing ``alt`` attribute
* Add support for ``{}`` in relative links syntax, besides ``||``
* Add support for ``{tag}`` and ``{category}`` relative links
* Add a ``content_written`` signal

3.2.1 and 3.2.2
===============

* Facilitate inclusion in FreeBSD Ports Collection

3.2 (2013-04-24)
================

* Support for Python 3!
* Override page save-to location from meta-data (enables using a static page as
  the site's home page, for example)
* Time period archives (per-year, per-month, and per-day archives of posts)
* Posterous blog import
* Improve WordPress blog import
* Migrate plugins to separate repository
* Improve HTML parser
* Provide ability to show or hide categories from menu using
  ``DISPLAY_CATEGORIES_ON_MENU`` option
* Auto-regeneration can be told to ignore files via ``IGNORE_FILES`` setting
* Improve post-generation feedback to user
* For multilingual posts, use meta-data to designate which is the original
  and which is the translation
* Add ``.mdown`` to list of supported Markdown file extensions
* Document-relative URL generation (``RELATIVE_URLS``) is now off by default

3.1 (2012-12-04)
================

* Importer now stores slugs within files by default. This can be disabled with
  the ``--disable-slugs`` option.
* Improve handling of links to intra-site resources
* Ensure WordPress import adds paragraphs for all types of line endings
  in post content
* Decode HTML entities within WordPress post titles on import
* Improve appearance of LinkedIn icon in default theme
* Add GitHub and Google+ social icons support in default theme
* Optimize social icons
* Add ``FEED_ALL_ATOM`` and ``FEED_ALL_RSS`` to generate feeds containing all
  posts regardless of their language
* Split ``TRANSLATION_FEED`` into ``TRANSLATION_FEED_ATOM`` and
  ``TRANSLATION_FEED_RSS``
* Different feeds can now be enabled/disabled individually
* Allow for blank author: if ``AUTHOR`` setting is not set, author won't
  default to ``${USER}`` anymore, and a post won't contain any author
  information if the post author is empty
* Move LESS and Webassets support from Pelican core to plugin
* The ``DEFAULT_DATE`` setting now defaults to ``None``, which means that
  articles won't be generated unless date metadata is specified
* Add ``FILENAME_METADATA`` setting to support metadata extraction from
  filename
* Add ``gzip_cache`` plugin to compress common text files into a ``.gz``
  file within the same directory as the original file, preventing the server
  (e.g. Nginx) from having to compress files during an HTTP call
* Add support for AsciiDoc-formatted content
* Add ``USE_FOLDER_AS_CATEGORY`` setting so that feature can be toggled on/off
* Support arbitrary Jinja template files
* Restore basic functional tests
* New signals: ``generator_init``, ``get_generators``, and
  ``article_generate_preread``

3.0 (2012-08-08)
================

* Refactored the way URLs are handled
* Improved the English documentation
* Fixed packaging using ``setuptools`` entrypoints
* Added ``typogrify`` support
* Added a way to disable feed generation
* Added support for ``DIRECT_TEMPLATES``
* Allow multiple extensions for content files
* Added LESS support
* Improved the import script
* Added functional tests
* Rsync support in the generated Makefile
* Improved feed support (easily pluggable with Feedburner for instance)
* Added support for ``abbr`` in reST
* Fixed a bunch of bugs :-)

2.8 (2012-02-28)
==================

* Dotclear importer
* Allow the usage of Markdown extensions
* Themes are now easily extensible
* Don't output pagination information if there is only one page
* Add a page per author, with all their articles
* Improved the test suite
* Made the themes easier to extend
* Removed Skribit support
* Added a ``pelican-quickstart`` script
* Fixed timezone-related issues
* Added some scripts for Windows support
* Date can be specified in seconds
* Never fail when generating posts (skip and continue)
* Allow the use of future dates
* Support having different timezones per language
* Enhanced the documentation

2.7 (2011-06-11)
==================

* Use ``logging`` rather than echoing to stdout
* Support custom Jinja filters
* Compatibility with Python 2.5
* Added a theme manager
* Packaged for Debian
* Added draft support

2.6 (2011-03-08)
==================

* Changes in the output directory structure
* Makes templates easier to work with / create
* Added RSS support (was Atom-only)
* Added tag support for the feeds
* Enhance the documentation
* Added another theme (brownstone)
* Added translations
* Added a way to use cleaner URLs with a rewrite url module (or equivalent)
* Added a tag cloud
* Added an autoreloading feature: the blog is automatically regenerated each
  time a modification is detected
* Translate the documentation into French
* Import a blog from an RSS feed
* Pagination support
* Added Skribit support

2.5 (2010-11-20)
==================

* Import from WordPress
* Added some new themes (martyalchin / wide-notmyidea)
* First bug report!
* Linkedin support
* Added a FAQ
* Google Analytics support
* Twitter support
* Use relative URLs, not static ones

2.4 (2010-11-06)
================

* Minor themes changes
* Add Disqus support (so we have comments)
* Another code refactoring
* Added config settings about pages
* Blog entries can also be generated in PDF

2.3 (2010-10-31)
================

* Markdown support

2.2 (2010-10-30)
================

* Prettify output
* Manages static pages as well

2.1 (2010-10-30)
================

* Make notmyidea the default theme

2.0 (2010-10-30)
================

* Refactoring to be more extensible
* Change into the setting variables

1.2 (2010-09-28)
================

* Added a debug option
* Added per-category feeds
* Use filesystem to get dates if no metadata is provided
* Add Pygments support

1.1 (2010-08-19)
================

* First working version
