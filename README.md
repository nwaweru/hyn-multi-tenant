# Hyn/Multi-Tenant Demo

## VirtualHost

```
<VirtualHost *:80>
    ServerName hyn-multi-tenant.test
    ServerAlias www.hyn-multi-tenant.test
    ServerAdmin ndiranguwaweru@gmail.com
    DocumentRoot /home/nwaweru/drashlabs/playground/hyn-multi-tenant/public
    <Directory "/home/nwaweru/drashlabs/playground/hyn-multi-tenant">
        Options Includes FollowSymLinks MultiViews
        AllowOverride all
        Require all granted
    </Directory>
    ErrorLog ${APACHE_LOG_DIR}/hyn-multi-tenant-error.log
    CustomLog ${APACHE_LOG_DIR}/hyn-multi-tenant-access.log combined
</VirtualHost>
```
