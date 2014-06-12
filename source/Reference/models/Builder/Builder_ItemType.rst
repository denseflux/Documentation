----------------
Builder_ItemType
----------------

.. php:class:: Builder_ItemType

extends :php:class:`Omeka_Record_Builder_AbstractBuilder`

    Build an item type.

    .. php:attr:: _recordClass

        protected

    .. php:attr:: _settableProperties

        protected

    .. php:method:: setElements($elementMetadata)

        Set the elements that will be attached to the built ItemType record.

        :type $elementMetadata: array
        :param $elementMetadata:
        :returns: void

    .. php:method:: _beforeBuild()

        Add elements to be associated with the Item Type.
