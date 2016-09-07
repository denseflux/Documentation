--------------------------
Omeka_File_MimeType_Detect
--------------------------

.. php:namespace:

.. php:class:: Omeka_File_MimeType_Detect

    Represents the detected MIME types of a file.

    .. php:attr:: _file

        protected string

    .. php:attr:: _strategies

        protected array

    .. php:attr:: _mimeType

        protected string

    .. php:attr:: _mimeTypes

        protected array

    .. php:attr:: _ambiguousMimeTypes

        protected array

    .. php:method:: __construct($file, $strategies = array())

        Set the required properties for detecting the MIME types of a file.

        :type $file: string|File
        :param $file: The full path to the file or a File record.
        :type $strategies: array
        :param $strategies: An array of file detection strategies in priority order. If none are passed, a default list will be set. All strategies must implement Omeka_File_MimeType_Detect_StrategyInterface.

    .. php:method:: detect()

        Detect the MIME type of this file.

        :returns: string The definitive MIME type.

    .. php:method:: getMimeType()

        Get the definitive MIME type of this file.

        :returns: string

    .. php:method:: getMimeTypes()

        Get the MIME types of this file, one for each detection strategy.

        :returns: array
