-------------------------
Omeka_Navigation_Page_Uri
-------------------------

.. php:namespace:

.. php:class:: Omeka_Navigation_Page_Uri

    Customized subclass of Zend Framework's Zend_Navigation_Page_Uri class.

    .. php:method:: isActive($recursive = false)

        Returns whether page should be considered active or not

        :param $recursive:
        :returns: bool             whether page should be considered active

    .. php:method:: setHref($href)

        Sets page href.  It will parse the href and update the uri and fragment
        properties.

        :param $href:
        :returns: Omeka_Navigation_Page_Uri   fluent interface, returns self

    .. php:method:: _normalizeHref($href)

        Normalizes a string href for a navigation page and returns an array with
        the following keys:
        'uri' => the uri of the href.
        'fragment' => the fragment of the href
        If the $href is a relative path, then it must be a root path.
        If the $href is a relative path then the value for the 'uri' key will be a
        relative path.
        If $href is an invalid uri, then return null.

        :type $href: String
        :param $href:
        :returns: array
