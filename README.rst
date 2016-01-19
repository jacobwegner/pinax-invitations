Pinax Invitations
=================

.. image:: http://slack.pinaxproject.com/badge.svg
   :target: http://slack.pinaxproject.com/
   
.. image:: https://img.shields.io/travis/pinax/pinax-invitations.svg
   :target: https://travis-ci.org/pinax/pinax-invitations

.. image:: https://img.shields.io/coveralls/pinax/pinax-invitations.svg
   :target: https://coveralls.io/r/pinax/pinax-invitations

.. image:: https://img.shields.io/pypi/dm/pinax-invitations.svg
   :target:  https://pypi.python.org/pypi/pinax-invitations/

.. image:: https://img.shields.io/pypi/v/pinax-invitations.svg
   :target:  https://pypi.python.org/pypi/pinax-invitations/

.. image:: https://img.shields.io/badge/license-MIT-blue.svg
   :target:  https://pypi.python.org/pypi/pinax-invitations/
   

Pinax
------

Pinax is an open-source platform built on the Django Web Framework. It is an ecosystem of reusable Django apps, themes, and starter project templates. 
This collection can be found at http://pinaxproject.com.

This app was developed as part of the Pinax ecosystem but is just a Django app and can be used independently of other Pinax apps.


pinax-invitations
------------------

``pinax-invitations`` is a site invitation app for Django.

Quickly setup the scaffolding for your django app.

What you get:

* test infrastructure
* Travis configuration with coveralls
* documentation instrastructure
* MIT LICENSE
* setup.py


Running the Tests
------------------

    ::

        $ pip install detox
        $ detox


Migrating from kaleo
---------------------
Previously, this app was named ``kaleo``.

To update an existing installation of Kaleo to become ``pinax-invitations``

* uninstall ``kaleo``
* install ``pinax-invitations``
* replace ``kaleo`` with ``pinax.invitations`` in your project's ``INSTALLED_APPS`` setting
* update any imports within your project (e.g. ``kaleo.urls``) to point to pinax.invitations (e.g. ``pinax.invitations.urls``)
* fake the initial migration of the ``invitations`` app::

     $ python manage.py migrate invitations --fake
* rename the table prefixes from ``kaleo_`` to ``invitations_``::

     $ python manage.py dbshell
     ALTER TABLE "kaleo_invitationstat" RENAME TO "invitations_invitationstat";
     ALTER TABLE "kaleo_joininvitation" RENAME TO "invitations_joininvitation";


Documentation
--------------

The pinax-invitations documentation is currently under construction. If you would like to help us write documentation, please join our Slack channel and let us know! 
The Pinax documentation is available at http://pinaxproject.com/pinax/.


Code of Conduct
----------------

In order to foster a kind, inclusive, and harassment-free community, the Pinax Project has a code of conduct, which can be found here  http://pinaxproject.com/pinax/code_of_conduct/.


Pinax Project Blog and Twitter
-------------------------------

For updates and news regarding the Pinax Project, please follow us on Twitter at @pinaxproject and check out our blog http://blog.pinaxproject.com.


    
