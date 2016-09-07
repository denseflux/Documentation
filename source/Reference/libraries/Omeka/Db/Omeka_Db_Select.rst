---------------
Omeka_Db_Select
---------------

.. php:namespace:

.. php:class:: Omeka_Db_Select

    Class for SQL SELECT generation and results.

    .. php:method:: __construct($adapter = null)

        :type $adapter: Zend_Db_Adapter
        :param $adapter: (optional) Adapter to use instead of the one set up by Omeka.

    .. php:method:: hasJoin($name)

        Detect if this SELECT joins with the given table.

        :type $name: string
        :param $name: Table name.
        :returns: boolean
