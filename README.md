mmps
====


Here is some software I wrote a little while ago for generating basic
map projections. 

It currently runs on Unix only, though could probably be ported to
Windows without too much trouble (use of mmap and the ppm image format
would be the major obstacles here). It runs OK under cygwin
though. Use of the ImageMagick tools is highly recommended. Interface
is command line only. Of course a little TCL front end would be nice.

To build the relevant executables:

$ make

Code should compile without warnings.

Additionally:

$ make ppms

converts any .jpg images in the <code>images</code> subdirectory to ppm format.

If compilation has gone smoothly,

$ make test

will try an example projection, displaying the result with the
ImageMagick display utility. The test assumes there is file called
earth.ppm in your images subdirectory.

See http://www.users.globalnet.co.uk/~arcus/mmps/ for further details.

Bugs
----

MMPS just maps pixels to pixels. There is no proper sampling and no
anti-aliasing.
The grid lines drawn are a bit rough.

Code Changes
------------

01/04/04 First version
17/07/04 Added circularize and combine utilities. Ensure output is
         binary on systems that make a distinction eg. cygwin.
28/08/06 Tidying up Makefile. Added Hammer projection.

Version 0.1.21, 14/09/06

More tidying. Added version option. Added SimpleTransform.  Corrected
a problem with Hammer and Bonne where the wrong matrix was being used.

MMPS Version 0.1.33 Jan 28 2007

Added sundial features, cylindrical projection. Measure date from
January 0 and not spring equinox.

MMPS Version 0.1.34 Jun 4 2007

Bug fixes

MMPS Version 0.1.35 Dec 31 2008

gridx, gridy feature fixed

18/05/13

Uploaded to github
