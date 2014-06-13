.. _faddfiledisplaycallback:

#########################
add_file_display_callback
#########################

:doc:`Plugin-related functions </Reference/packages/Omeka/Function/Plugin/index>`

*******
Summary
*******

.. include:: /Reference/libraries/globals/summary/add_file_display_callback.rst

.. php:function:: add_file_display_callback($fileIdentifiers, $callback, $options = Array)

    Declare a callback function that will be used to display files with a
    given
    MIME type and/or file extension.
    
    :type $fileIdentifiers: array|string
    :param $fileIdentifiers: Set of MIME types and/or file extensions to which the provided callback will respond.
    :type $callback: callback
    :param $callback: Any valid callback.
    :type $options: array
    :param $options:

*****
Usage
*****

.. include:: /Reference/libraries/globals/usage/add_file_display_callback.rst

********
Examples
********

.. include:: /Reference/libraries/globals/examples/add_file_display_callback.rst

********
See Also
********

.. include:: /Reference/libraries/globals/see_also/add_file_display_callback.rst

