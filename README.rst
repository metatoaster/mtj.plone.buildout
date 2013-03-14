Minimum Buildout for Zope/Plone with zeoserver
==============================================

This is a basic foundational buildout extracted from the standard Plone
unified installer, with bits added to aid development and deployment
such as the inclusion of mr.developer and definition of a separate
zeoserver to allow a separate debug/python shell instance to connect to
a running instance.

To make use of this, fork/clone the repo, include specific development
bits as per normal usage of mr.developer, and::

    $ python bootstrap.py --version 1.5.2
    $ bin/buildout
    ... wait for buildout to finish
    $ bin/zeoserver-testing start
    $ bin/instance-testing fg  # or start if you want it in background
