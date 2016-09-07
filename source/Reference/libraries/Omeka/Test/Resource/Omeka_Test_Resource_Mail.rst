------------------------
Omeka_Test_Resource_Mail
------------------------

.. php:namespace:

.. php:class:: Omeka_Test_Resource_Mail

    Testing resource for saving mail to the filesystem.

    .. php:method:: init()

        :returns: Zend_Mail

    .. php:method:: mailCallback($transport)

        Makes mail output names contain both the timestamp and an incrementing
        counter. The timestamp ensures mails between test runs don't
        collide, the counter differentiates between messages sent during
        the same timestamp unit (common).

        :param $transport:
