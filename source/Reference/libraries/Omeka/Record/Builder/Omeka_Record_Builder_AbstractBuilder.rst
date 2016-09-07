------------------------------------
Omeka_Record_Builder_AbstractBuilder
------------------------------------

.. php:namespace:

.. php:class:: Omeka_Record_Builder_AbstractBuilder

    Build or update an {@link Omeka_Record_AbstractRecord} as needed.

    .. php:attr:: _recordClass

        protected string

        Class of record that the builder will create.

    .. php:attr:: _settableProperties

        protected array

        String names denoting the properties of a specific record
        that can be set directly through the builder.  This will not always
        be all of the fields for the record.

    .. php:attr:: _record

        protected Omeka_Record_AbstractRecord

        Record being built or updated.

    .. php:attr:: _db

        protected Omeka_Db

    .. php:method:: __construct(Omeka_Db $db)

        :type $db: Omeka_Db
        :param $db:

    .. php:method:: build()

        Build the actual record.  If the record already exists, update it as
        necessary.

        :returns: Omeka_Record_AbstractRecord

    .. php:method:: setRecordMetadata($metadata)

        Set basic metadata for the record.

        Note that the columns to be set must be specified in the
        $_settableProperties property of subclassed Builders.

        :type $metadata: array
        :param $metadata:
        :returns: void

    .. php:method:: getRecordMetadata()

        Get the metadata that will be saved to the record.

        :returns: array

    .. php:method:: getRecord()

        Get the record that is being acted upon by the builder.

        When an Omeka_Record_AbstractRecord instance has been provided via
        setRecord(), that will be returned.  If a record ID has been provided,
        then the appropriate record will be returned.

        Otherwise, a new instance of Omeka_Record_AbstractRecord will be returned.

        :returns: Omeka_Record_AbstractRecord

    .. php:method:: setRecord($record = null)

        Set the record upon which this builder will act.

        :type $record: Omeka_Record_AbstractRecord|integer|null
        :param $record:
        :returns: void

    .. php:method:: _beforeBuild(Omeka_Record_AbstractRecord $record)

        All necessary tasks to take place before the record is inserted.

        Exceptions may be thrown, validation errors may be added.

        :type $record: Omeka_Record_AbstractRecord
        :param $record:
        :returns: void

    .. php:method:: _afterBuild(Omeka_Record_AbstractRecord $record)

        All necessary tasks that take place after the record has been inserted
        into the database.

        Should not throw exceptions in this method.

        :type $record: Omeka_Record_AbstractRecord
        :param $record:
        :returns: void

    .. php:method:: _setRecordProperties($record)

        Set the properties for the record, taking care to filter based on the
        $_settableProperties array.

        :type $record: Omeka_Record_AbstractRecord
        :param $record:
        :returns: void
