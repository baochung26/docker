Rename container_name in docker-composer.yml file with prefix is curent project ( vd :ramen_php7.4 )
Change apache port to any port you want ( vd: "8088:80" )
Change mysql port to any port you want ( vd: "33066:3306" )
Change phpmyadmin port to any port you want ( vd: "18882:80" ) => url web 127.0.0.1:18882

env laravel config:
DB_CONNECTION=mysql
DB_HOST=mysql => this is name of service in docker-compose.yml ( not container_name )
DB_PORT=3306
DB_DATABASE=ramen
DB_USERNAME=miichi
DB_PASSWORD=123456