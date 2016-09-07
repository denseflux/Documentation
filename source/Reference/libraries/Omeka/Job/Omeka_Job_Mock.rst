--------------
Omeka_Job_Mock
--------------

.. php:namespace:

.. php:class:: Omeka_Job_Mock

    Mock job class for unit tests.

    .. php:attr:: options

    .. php:attr:: performed

    .. php:attr:: _db

        protected Omeka_Db

    .. php:attr:: _dispatcher

        protected Omeka_Job_Dispatcher_DispatcherInterface

    .. php:attr:: _user

        protected User

    .. php:attr:: _options

        protected

    .. php:method:: __construct($options)

        :param $options:

    .. php:method:: perform()

    .. php:method:: getDb()

        Getter method to expose protected properties.

    .. php:method:: getDispatcher()

        Getter method to expose protected properties.

    .. php:method:: getMiscOptions()

    .. php:method:: _setOptions($options)

        Set all the options associated with this task.

        This is a convenience method that calls setter methods for the options
        given in the array.  If an element in the array does not have an
        associated setter method, it will be passed into the options array.

        :param $options:

    .. php:method:: setDb(Omeka_Db $db)

        :type $db: Omeka_Db
        :param $db:

    .. php:method:: setJobDispatcher(Omeka_Job_Dispatcher_DispatcherInterface $dispatcher)

        :type $dispatcher: Omeka_Job_Dispatcher_DispatcherInterface
        :param $dispatcher:

    .. php:method:: setUser(User $user)

        Set the given User object on the Job object.

        :type $user: User
        :param $user:

    .. php:method:: getUser()

        Get the User currently set on this Job, if any.

        :returns: User|null

    .. php:method:: resend()

        Resend the job using the same options that were passed to the current
        job.
