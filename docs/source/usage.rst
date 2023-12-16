Usage
=====

Installation
------------

Для установки Currencies в своем проекте:

.. code-block:: console

   (.venv) $ git clone ...


Получение списка валют
----------------

Для получения списка валют необходимо создать класс, имплементирующий BaseCurrenciesRequester, а так же класс CurrenciesDict:
.. code-block:: python
    requester = CBRCurrenciesRequester()
    c = CurrenciesDict(requester)

    c.request_currencies()
    cs = c.get_currencies()
    usd = c.get_currencies_by_id('R01235')

    c.set_tracked_currencies('R01335', 'R01239', 'R01235')
    tracked = c.get_tracked_currencies()

.. automodule:: currencies.currencies

.. autoclass:: currencies.currencies.CurrenciesDict

.. automethod:: currencies.currencies.CurrenciesDict.request_currencies

.. automethod:: currencies.currencies.CurrenciesDict.visualize

.. automethod:: currencies.currencies.CurrenciesDict.get_currencies

.. automethod:: currencies.currencies.CurrenciesDict.get_currencies_by_id

.. automethod:: currencies.currencies.CurrenciesDict.set_tracked_currencies

.. automethod:: currencies.currencies.CurrenciesDict.get_tracked_currencies