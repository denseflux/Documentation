-----------------------------
Omeka_Controller_Plugin_Jsonp
-----------------------------

.. php:namespace:

.. php:class:: Omeka_Controller_Plugin_Jsonp

    Sets the Content-Type header for all JSON-P requests.

    .. php:const:: CALLBACK_KEY

        Callback parameter key.

    .. php:method:: postDispatch(Zend_Controller_Request_Abstract $request)

        Set the 'Content-Type' HTTP header to 'application/x-javascript' for
        omeka-json requests.

        :type $request: Zend_Controller_Request_Abstract
        :param $request: Request object.
        :returns: void
