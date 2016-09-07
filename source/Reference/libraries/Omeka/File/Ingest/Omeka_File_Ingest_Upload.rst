------------------------
Omeka_File_Ingest_Upload
------------------------

.. php:namespace:

.. php:class:: Omeka_File_Ingest_Upload

    This class creates a bridge between the ZF File Transfer HTTP adapter and
    Omeka's file ingest classes.

    .. php:attr:: _adapter

        protected Zend_File_Transfer_Adapter_Http

    .. php:attr:: _adapterOptions

        protected array

    .. php:attr:: _item

        protected Item

    .. php:attr:: _options

        protected array

        Set of arbitrary options to use when ingesting files.

    .. php:attr:: mimeType

        string

        The current validated file MIME type.

    .. php:method:: _buildAdapter()

        Create a ZF HTTP file transfer adapter.

        :returns: void

    .. php:method:: setOptions($options)

        In addition to the default options available for
        Omeka_File_Ingest_AbstractIngest, this understands the following options:
        - 'ignoreNoFile' => boolean False by default.  Whether or not to ignore
        - validation errors that occur when an uploaded file is missing.  This
        - may occur when a file input is left empty on a form.

        This option can be overridden by the 'ignore_invalid_files' option.  For
        instance, if 'ignoreNoFile' is set to false but 'ignore_invalid_files' is
        set to true, any exceptions due to missing uploads will be suppressed and
        ignored.

        :type $options: array
        :param $options:
        :returns: void

    .. php:method:: _getOriginalFilename($fileInfo)

        The 'name' attribute of the $_FILES array will always contain the
        original name of the file.

        :type $fileInfo: array
        :param $fileInfo:
        :returns: string

    .. php:method:: _transferFile($fileInfo, $originalFilename)

        Use the Zend_File_Transfer adapter to upload the file.

        :type $fileInfo: array
        :param $fileInfo:
        :type $originalFilename: string
        :param $originalFilename:
        :returns: string Path to the file in Omeka.

    .. php:method:: _parseFileInfo($fileInfo)

        Use the adapter to extract the array of file information.

        :type $fileInfo: string|null
        :param $fileInfo: The name of the form input to ingest.
        :returns: array

    .. php:method:: addValidator(Zend_Validate_Interface $validator)

        Use the Zend Framework adapter to handle validation instead of the
        built-in _validateFile() method.

        :type $validator: Zend_Validate_Interface
        :param $validator:
        :returns: void

    .. php:method:: setItem(Item $item)

        Set the item to use as a target when ingesting files.

        :type $item: Item
        :param $item:
        :returns: void

    .. php:method:: factory($adapterName, $item, $options = array())

        Factory to retrieve Omeka_File_Ingest_* instances.

        :type $adapterName: string
        :param $adapterName: Ingest adapter.
        :type $item: Item
        :param $item:
        :type $options: array
        :param $options:
        :returns: Omeka_File_Ingest_AbstractIngest

    .. php:method:: ingest($fileInfo)

        Ingest based on arbitrary file identifier info.

        If this is an array that has a 'metadata' key, that should be an array
        representing element text metadata to assign to the file.  See
        ActsAsElementText::addElementTextsByArray() for more details.

        :type $fileInfo: mixed
        :param $fileInfo: An arbitrary input (array, string, object, etc.) that corresponds to one or more files to be ingested into Omeka.
        :returns: array Ingested file records.

    .. php:method:: _ignoreIngestErrors()

        Determine whether or not to ignore file ingest errors.  Based on
        'ignore_invalid_files', which is false by default.

        :returns: boolean

    .. php:method:: _logException(Exception $e)

        Log any exceptions that are thrown as a result of attempting to ingest
        invalid files.

        These are logged as warnings because they are being ignored by the script,
        so they don't actually kill the file ingest process.

        :type $e: Exception
        :param $e:
        :returns: void

    .. php:method:: _createFile($newFilePath, $oldFilename, $elementMetadata = array())

        Insert a File record corresponding to an ingested file and its metadata.

        :type $newFilePath: string
        :param $newFilePath: Path to the file within Omeka.
        :type $oldFilename: string
        :param $oldFilename: The original filename for the file.  This will usually be displayed to the end user.
        :type $elementMetadata: array
        :param $elementMetadata: See ActsAsElementText::addElementTextsByArray() for more information about the format of this array.
        :returns: File

    .. php:method:: _getDestination($fromFilename)

        Retrieve the destination path for the file to be transferred.

        This will generate an archival filename in order to prevent naming
        conflicts between ingested files.

        This should be used as necessary by Omeka_File_Ingest_AbstractIngest
        implementations in order to determine where to transfer any given file.

        :type $fromFilename: string
        :param $fromFilename: The filename from which to derive the archival filename.
        :returns: string

    .. php:method:: _validateFile($filePath, $fileInfo)

        Validate a file that has been transferred to Omeka.

        Implementations of Omeka_File_Ingest_AbstractIngest should use this to
        validate the uploaded file based on user-defined security criteria.

        Important: $fileInfo may need to contain the following keys in order to
        work with particular Zend_Validate_File_* validation classes:

        - 'name': string filename (for Zend_Validate_File_Extension) If ZF is
        unable to determine the file extension when validating, it will check the
        'name' attribute instead.  Current use cases involve saving the file to a
        temporary location before transferring to Omeka. Most temporary files do
        not maintain the original file extension.
        - 'type': string MIME type (for Zend_Validate_File_MimeType) If ZF is
        unable to determine the mime type from the transferred file.  Unless the
        server running Omeka has a mime_magic file or has installed the FileInfo
        extension, this will be necessary.

        :type $filePath: string
        :param $filePath: Absolute path to the file.  The file should be local and readable, which is required by most (if not all) of the Zend_Validate_File_* classes.
        :type $fileInfo: array
        :param $fileInfo: Set of file info that describes a given file being ingested.
        :returns: boolean True if valid, otherwise throws an exception.
