----------------------------
Installer_InstallerInterface
----------------------------

.. php:interface:: Installer_InstallerInterface

    Interface for creating different installers for Omeka.

    .. php:method:: __construct(Omeka_Db $db)

        :type $db: Omeka_Db
        :param $db:

    .. php:method:: install()

    .. php:method:: isInstalled()
