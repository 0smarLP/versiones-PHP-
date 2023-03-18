## Pasos para cambiar de versiones en PHP usando 'Aliases' en Bash

1. Abre tu terminal y escribe **gedit ~/.bashrc** para abrir el archivo de configuración de tu shell bash en un editor de texto.

2. Desplázate hasta el final del archivo y agrega las siguientes líneas:

```
alias php56='sudo a2dismod php* && sudo a2enmod php5.6 && sudo update-alternatives --set php /usr/bin/php5.6 && sudo service apache2 restart'
alias php70='sudo a2dismod php* && sudo a2enmod php7.0 && sudo update-alternatives --set php /usr/bin/php7.0 && sudo service apache2 restart'
alias php71='sudo a2dismod php* && sudo a2enmod php7.1 && sudo update-alternatives --set php /usr/bin/php7.1 && sudo service apache2 restart'
alias php72='sudo a2dismod php* && sudo a2enmod php7.2 && sudo update-alternatives --set php /usr/bin/php7.2 && sudo service apache2 restart'
alias php73='sudo a2dismod php* && sudo a2enmod php7.3 && sudo update-alternatives --set php /usr/bin/php7.3 && sudo service apache2 restart'
alias php74='sudo a2dismod php* && sudo a2enmod php7.4 && sudo update-alternatives --set php /usr/bin/php7.4 && sudo service apache2 restart'
alias php80='sudo a2dismod php* && sudo a2enmod php8.0 && sudo update-alternatives --set php /usr/bin/php8.0 && sudo service apache2 restart'
alias php81='sudo a2dismod php* && sudo a2enmod php8.1 && sudo update-alternatives --set php /usr/bin/php8.1 && sudo service apache2 restart'
```

3. Guarda el archivo y cierra el editor de texto.
4. Escribe **source ~/.bashrc** en tu terminal para aplicar los cambios.
5. Para cambiar de versión de PHP, simplemente escribe el alias para la versión que quieres usar. Por ejemplo, para cambiar a PHP 7.4, escribe php74 y presiona enter. Esto deshabilitará la versión actual de PHP, habilitará PHP 7.4, actualizará la alternativa de PHP y reiniciará Apache.

### Nota:

Esto supone que tienes varias versiones de PHP instaladas en tu sistema y que están ubicadas en /usr/bin/. Si tus versiones de PHP están instaladas en otro lugar, deberás ajustar las rutas de archivo en los aliases en consecuencia.
