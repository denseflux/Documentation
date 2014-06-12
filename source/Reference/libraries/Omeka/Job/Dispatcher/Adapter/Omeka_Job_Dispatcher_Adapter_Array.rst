----------------------------------
Omeka_Job_Dispatcher_Adapter_Array
----------------------------------

.. php:class:: Omeka_Job_Dispatcher_Adapter_Array

implements :php:interface:`Omeka_Job_Dispatcher_Adapter_AdapterInterface`

    Store dispatched jobs in an array.

    This is used primarily by unit tests and should not be used in production code.

    .. php:method:: setQueueName($name)

        :param $name:

    .. php:method:: send($encodedJob, $metadata)

        :param $encodedJob:
        :param $metadata:

    .. php:method:: getJobs()

    .. php:method:: getJob($index = 0)

        :param $index:
