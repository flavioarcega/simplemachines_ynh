This app is simply a blank web app skeleton : you are expected to add you own content (HTML, CSS, PHP, ...) inside `__INSTALL_DIR__/www/`. One way to do so is by using SFTP.

### Login using the command line

Starting YunoHost v11.1.21, you can run `sudo yunohost app shell __APP__` in the command line interface to log in as your app user.

The `php` command will point to the PHP version installed for the app.

### Adding or editing files

Once logged in, under the Web directory you will see a `www` folder which contains the public files served by this app. You can put all the files of your custom Web application inside.

### 403 and 404 error handling

The web server configuration supports http error handling `403` and `404` (access denied and resource not found). Create an `error` folder at `__INSTALL_DIR__/www/error`, and put your `403.html` and `404.html` files in there.

### Customizing the nginx configuration

If you want to add tweak the nginx configuration for this app, it is recommended to edit `/etc/nginx/conf.d/__DOMAIN__.d/__ID__.d/WHATEVER_NAME.conf` (ensure that the file has the `.conf` extension) and reload the nginx after making sure that the configuration is valid using `nginx -t`.
