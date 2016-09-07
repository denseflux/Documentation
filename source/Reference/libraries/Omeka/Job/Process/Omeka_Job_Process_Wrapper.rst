-------------------------
Omeka_Job_Process_Wrapper
-------------------------

.. php:namespace:

.. php:class:: Omeka_Job_Process_Wrapper

    Wrapper that allows Omeka_Job to work with the existing Process/
    Omeka_Job_Process_Dispatcher API. Jobs are passed in as the 'job' argument,
    and this wrapper handles decoding and executing the job.

    .. php:attr:: _process

        protected

    .. php:method:: _getJob($str)

        :param $str:

    .. php:method:: run($args)

        Args passed in will consist of the JSON-encoded task.

        :param $args:

    .. php:method:: __construct(Process $process)

        :type $process: Process
        :param $process:

    .. php:method:: __destruct()
