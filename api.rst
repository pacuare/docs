.. _api:

API
###

The public API (accessed using an :ref:`API key <api-keys>` in a Bearer authorization header) allows access to query the database using SQL.

.. warning::
    Your API keys have the *exact* same level of access as your account -- if you're working directly with the main database, then so are your apps! If you'd like a separate, limited-access account to write apps on, please get in touch.

.. _sdk:

SDK
***

The Python SDK (published as `pacuare on PyPI <https://pypi.org/project/pacuare>`_) allows easy access to the API, returning results as a Pandas DataFrame for easy manipulation. You can see a demo of a Streamlit app interfacing with the SDK `here <https://pacuare.streamlit.app>`_.