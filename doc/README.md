sudo is needed to restart the workers because we are using the service command. Capistrano deploys with a user which does not have sudo rights, so we need to explicitly enable the services command for the user.

To enable automatic restart of the workers by capistrano run sudo visudo and append this line:

user_name ALL=(root) NOPASSWD: /usr/sbin/service workers *
