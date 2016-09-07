----------------------------------
Omeka_Form_Decorator_SavePanelHook
----------------------------------

.. php:namespace:

.. php:class:: Omeka_Form_Decorator_SavePanelHook

    Decorator to add hooks into the admin save panel created via Omeka_Form_Admin

    .. php:method:: render($content)

        :param $content:

    .. php:method:: getType()

        Get the record type if the Omeka_Form_Admin was created with that option
        set

        :returns: mixed false or the record

    .. php:method:: getRecord()

        Get the record if the Omeka_Form_Admin was created with that option set

        :returns: mixed false or the record
