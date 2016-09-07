------------------------------
Omeka_Application_Resource_Acl
------------------------------

.. php:namespace:

.. php:class:: Omeka_Application_Resource_Acl

    Initializes Omeka's ACL.

    .. php:attr:: _acl

        protected Zend_Acl

        Access control list object.

    .. php:method:: init()

        Load the hardcoded ACL definitions, then apply definitions from plugins.

        :returns: Zend_Acl

    .. php:method:: getAcl()
