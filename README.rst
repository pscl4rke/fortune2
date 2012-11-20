

Fortune2
========

Fortune2 is a reimplementation of the classic Fortune program that is better
suited to the modern age.  When run it selects a random quote from the database
and displays it on the screen.  It can be used to welcome you to a new shell
session, etc etc.


Why Re-implement
----------------

The original fortune was designed primarily with system administration in mind.
The database is stored centrally, requiring root privileges to edit, with no
way for a user to override.

It also over-complicates matters by expecting the plain-text data files to
be compiled into a binary form before use.  But thanks to the likes of Moore's
Law this is no longer needed.


How To Use
----------

The Program:
    The only dependency is Python 2 (tested with 2.7).  Put the ``fortune``
    script somewhere on your path.

The Database:
    This is the directory ``$HOME/.fortune``.  Any files in here with a
    ``.fortune`` file extension will be treated as data files, and quotes
    will be loaded from them.  They can be symlinks if desired.  The format
    has been copied from the original fortune's source files, sometimes
    referred to as the *Cookie Jar* format.  This means it contains
    paragraphs of quotes separated by a percent sign on a line on its own.


Room For Improvement
--------------------

*   It would be good for it to take an argument that lets it use a different
    database directory.

*   The program could be refactored to work better as a Python module if that
    would be useful.

*   I don't want to get into maintaining database files myself, but it would good
    to point to a number of other sources.  I could provide a sample file.

*   If I do provide a sample file then I could put together a test routine.

*   Some definitions of *Cookie Jar* say that multiple percent signs should
    be used a separators, so I could consider supporting this.

