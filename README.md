# clientx icon
clientx - icons

### Comments on archive content

  - /font/* - fonts in different formats
  - /css/*  - different kinds of css, for all situations. Should be ok with 
  twitter bootstrap. Also, you can skip <i> style and assign icon classes
  directly to text elements, if you don't mind about IE7.

- demo.html - demo file, to show your webfont content

- config.json - keeps your settings. 

Why so many CSS files ?
-----------------------

Because we like to fit all your needs :)

- basic file, <your_font_name>.css - is usually enough, it contains @font-face
  and character code definitions

- *-ie7.css - if you need IE7 support, but still don't wish to put char codes
  directly into html

- *-codes.css and *-ie7-codes.css - if you like to use your own @font-face
  rules, but still wish to benefit from css generation. That can be very
  convenient for automated asset build systems. When you need to update font -
  no need to manually edit files, just override old version with archive
  content. See fontello source code for examples.

- *-embedded.css - basic css file, but with embedded WOFF font, to avoid
  CORS issues in Firefox and IE9+, when fonts are hosted on the separate domain.
  We strongly recommend to resolve this issue by `Access-Control-Allow-Origin`
  server headers. But if you ok with dirty hack - this file is for you. Note,
  that data url moved to separate @font-face to avoid problems with <IE9, when
  string is too long.

This text you see here is *actually* written in Markdown! To get a feel for Markdown's syntax, type some text into the left window and watch the results in the right.

Attention for server setup
--------------------------

You MUST setup server to reply with proper `mime-types` for font files -
otherwise some browsers will fail to show fonts.

Usually, `apache` already has necessary settings, but `nginx` and other
webservers should be tuned. Here is list of mime types for our file extensions:

- `application/vnd.ms-fontobject` - eot
- `application/x-font-woff` - woff
- `application/x-font-ttf` - ttf
- `image/svg+xml` - svg

License
----

MIT


**ClientX**
