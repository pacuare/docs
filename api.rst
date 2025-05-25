.. _api:

API
###

The public API (accessed using an :ref:`API key <api-keys>` in a Bearer authorization header) allows access to query the database using SQL. For easier programmatic access, take a look at the :doc:`sdk`.

.. warning::
    Your API keys have the *exact* same level of access as your account -- if you're working directly with the main database, then so are your apps! If you'd like a separate, limited-access account to write apps on, please get in touch.

``/api/query`` allows you to query the database; it can be called using either a plain SQL request body or SQL with parameters encoded in JSON. Make sure to pass an ``Authorization: Bearer <api_key>`` header to authenticate.

For the most up-to-date information, examples, and interactive documentation, please see the `API-hosted docs <https://api.pacuare.dev>`_.

.. openapi:: openapi.json
