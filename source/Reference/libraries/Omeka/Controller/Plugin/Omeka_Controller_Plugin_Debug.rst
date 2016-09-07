-----------------------------
Omeka_Controller_Plugin_Debug
-----------------------------

.. php:namespace:

.. php:class:: Omeka_Controller_Plugin_Debug

    This controller plugin allows for debugging Request objects without inserting
    debugging code into the Zend Framework code files.

    Debugging web requests is enabled by setting 'debug.request = true' in the config.ini file.

    .. php:method:: preDispatch(Zend_Controller_Request_Abstract $request)

        Print request debugging info for every request.

        Has no effect if request debugging is not enabled in config.ini.

        :type $request: Zend_Controller_Request_Abstract
        :param $request: Request object.
        :returns: void

    .. php:method:: postDispatch(Zend_Controller_Request_Abstract $request)

        :type $request: Zend_Controller_Request_Abstract
        :param $request:

    .. php:method:: dispatchLoopShutdown()

        Print database profiling info.

        Enabled conditionally when debug.profileDb = true in config.ini.

        :returns: void

    .. php:method:: _getProfilerMarkup(Zend_Db_Profiler $profiler)

        :type $profiler: Zend_Db_Profiler
        :param $profiler:

    .. php:method:: _getRequestMarkup($request, $router)

        Create HTML markup for request debugging.

        :type $request: Zend_Controller_Request_Abstract
        :param $request: Request object.
        :type $router: Zend_Controller_Router_Interface
        :param $router: Router object.
        :returns: string HTML markup.
