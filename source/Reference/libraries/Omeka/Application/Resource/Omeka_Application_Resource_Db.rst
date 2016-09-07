-----------------------------
Omeka_Application_Resource_Db
-----------------------------

.. php:namespace:

.. php:class:: Omeka_Application_Resource_Db

    Set up the default database connection for Omeka.

    .. php:const:: INIT_COMMAND

        Command to run at connect time; currently sets the SQL mode

    .. php:method:: init()

        :returns: Omeka_Db

    .. php:method:: setinipath($path)

        Set the path to the database configuration file.

        Allows {@link $_iniPath} to be set by the app configuration.

        :type $path: string
        :param $path:
