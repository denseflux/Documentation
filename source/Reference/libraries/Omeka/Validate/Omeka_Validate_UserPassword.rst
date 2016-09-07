---------------------------
Omeka_Validate_UserPassword
---------------------------

.. php:namespace:

.. php:class:: Omeka_Validate_UserPassword

    Validate a password to see if it matches that of an existing user.

    .. php:const:: INVALID

        Invalid password error.

    .. php:attr:: _messageTemplates

        protected array

        Error message templates.

    .. php:method:: __construct(User $user)

        :type $user: User
        :param $user:

    .. php:method:: isValid($value, $context = null)

        Validate against a user's stored password.

        :type $value: string
        :param $value: Password to check.
        :type $context: null
        :param $context: Not used.
