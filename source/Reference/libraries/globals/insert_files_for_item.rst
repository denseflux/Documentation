.. _finsertfilesforitem:

#####################
insert_files_for_item
#####################

:doc:`Item-related functions </Reference/packages/Omeka/Function/Db/Item/index>`

*******
Summary
*******

.. include:: /Reference/libraries/globals/summary/insert_files_for_item.rst

.. php:function:: insert_files_for_item($item, $transferStrategy, $files, $options = Array)

    Add files to an item.
    
    :type $item: Item|integer
    :param $item:
    :type $transferStrategy: string|Omeka_File_Ingest_AbstractIngest
    :param $transferStrategy:
    :type $files: array
    :param $files:
    :type $options: array
    :param $options: Available Options: <ul> <li>'ignore_invalid_files': boolean false by default.  Determine whether or not to throw exceptions when a file is not valid. </li> </ul>
    :returns: array

*****
Usage
*****

.. include:: /Reference/libraries/globals/usage/insert_files_for_item.rst

********
Examples
********

.. include:: /Reference/libraries/globals/examples/insert_files_for_item.rst

********
See Also
********

.. include:: /Reference/libraries/globals/see_also/insert_files_for_item.rst

