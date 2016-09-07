--------------------------------------
Omeka_Application_Resource_Currentuser
--------------------------------------

.. php:namespace:

.. php:class:: Omeka_Application_Resource_Currentuser

    Retrive the User record corresponding to the authenticated user.

    If the user record is not retrievable (invalid ID), then the authentication ID will be cleared.

    .. php:method:: init()

        Retrieve the User record associated with the authenticated user.

        :returns: User|null
