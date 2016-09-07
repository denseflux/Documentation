-----------------
Omeka_Http_Client
-----------------

.. php:namespace:

.. php:class:: Omeka_Http_Client

    Wrapper for Zend_Http_Client.

    Adds the following functionality: retries on timeouts.

    .. php:method:: request($method = null)

        Wraps Zend_Http_Client to automatically retry timed out requests.

        :param $method:

    .. php:method:: setMaxRetries($count)

        Set the maximum number of retries to make when a request times out.

        :type $count: integer
        :param $count:
