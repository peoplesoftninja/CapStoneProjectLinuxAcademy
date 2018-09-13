pgbackup
=======

CLI for backup remote PostgreSQL database either locally or to S3

Preparing the Development
-------------

1. Ensure `pip` and ``pipenv`` are installed
2. Clone repository: ``git clone git@github.com:example/pgbackup``
3. ``cd`` into the repository
4. Fetch development dependecies ``make install``
5. Activate virtualenv: ``pipenv shell``

Usage
----

Pass in a full DB url, the storage dirver, and the destination

S3 Eample w/ bucket name:

::

  $ pgbackup postgres://bob@example.com::5432/db_one --driver s3 backups

Local Example w/ local paths

::

  $ pgbackup postgres://bob@example.com:5432/db_one --driver local /var/dump.sql

Running Tests
----

Run tests locally using ``make`` if virutalenv is active:

::

  $ make

If virualenv isn't active then use:

::
  $ pipenv run make

