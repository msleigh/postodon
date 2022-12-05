Usage
=====

.. _installation:

Installation
------------

To use, first:

.. code-block:: console

    pip install postodon
    source .venv/bin/activate
    pip install postodon

.. _setup:

Setup
-----

 - Register an application as described here: https://docs.joinmastodon.org/client/token/#app
 - Get an access token as described here: https://docs.joinmastodon.org/client/authorized/#flow
 - Securely store the returned `access_token` for future reference
 - Edit `config.json` to include the name of the Mastodon instance and the name of the posts file, e.g. `posts.json`

.. _usage:

Usage
-----

To use, put the access token in an environment variable called `AUTH_TOKEN`:

.. code-block:: console

    export AUTH_TOKEN=<your_access_token_here>

To select a random post from the list without either updating the list or posting (dry-run mode):

.. code-block:: console

    postodon -n

To publicly post a random post, marked as English, and update the list (mark the post having been posted):

.. code-block:: console

    postodon

NB if there are no unposted posts left in the list, this will return a random post from the 'posted' selection.

To add new posts to the list for future posting, add them to the specified posts file.
