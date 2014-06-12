----------
Table_User
----------

.. php:class:: Table_User

extends :php:class:`Omeka_Db_Table`

    .. php:method:: findActiveById($id)

        Find an active User given that user's ID.

        Returns null if the user being requested is not active.

        :param $id:
        :returns: User|null

    .. php:method:: _getColumnPairs()

    .. php:method:: findByEmail($email)

        :param $email:

    .. php:method:: applySearchFilters($select, $params)

        :param $select:
        :param $params:
