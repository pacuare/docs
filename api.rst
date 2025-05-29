.. _api:

API
###

The public API (accessed using an :ref:`API key <api-keys>` in a Bearer authorization header) allows access to query the database using SQL. For easier programmatic access, take a look at the :doc:`sdk`.

.. warning::
    Your API keys have the *exact* same level of access as your account -- if you're working directly with the main database, then so are your apps! If you'd like a separate, limited-access account to write apps on, please get in touch.

``/query`` allows you to query the database; it can be called using either a plain SQL request body or SQL with parameters encoded in JSON. Make sure to pass an ``Authorization: Bearer <api_key>`` header to authenticate.

``/query.csv`` takes the same request as ``/query``, but returns a CSV instead of JSON data. You can play with it here, if you're logged into ``app.pacuare.dev``:

.. raw:: html

   <form action="https://api.pacuare.dev/v1/query.csv/form" method="POST" target="_blank" style="display:flex;flex-direction:row;gap:5px;">
      <input type="text" name="query" placeholder="Query">
      <button type="submit">Query</button>
   </form>

.. note::
   Both ``query`` and ``query.csv`` also have ``/form`` sub-endpoints that take form data instead of JSON -- useful if you're trying to avoid JavaScript, or just keep things simple.

For the most up-to-date information, examples, and interactive documentation, please see the `API-hosted docs <https://api.pacuare.dev>`_.

.. openapi:: openapi.json
