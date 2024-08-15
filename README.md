clonar proyecto, 
    npm install
    composer install
crear key 
    php artisan key:generate --ansi
iniciar con: 
    php artisan migrate 
data un error de llenado de datos
ingresar: para resetear todas las tablas con sus seeders incluido
    php artisan migrate:fresh --seed


php artisan serve
npm run dev 



MEMO
min 2:03:38 del video 3 crea una rule particular aplicable a emails que no se repitan



Produccion
# Instalar dependencias con optimización
composer install --optimize-autoloader --no-dev

# Otros comandos necesarios para el despliegue
Subir el Proyecto al Servidor

Subir el Código del Proyecto:
bash
Copiar código
cd /var/www
git clone https://github.com/tu_usuario/tu_proyecto.git your_project
cd your_project

Instalar Dependencias de Laravel y NPM:
bash
Copiar código
composer install --optimize-autoloader --no-dev
npm install
npm run production

Configurar Permisos:
bash
Copiar código
chown -R www-data:www-data /var/www/your_project
chmod -R 775 /var/www/your_project/storage
chmod -R 775 /var/www/your_project/bootstrap/cache

Configurar el Archivo .env:
bash
Copiar código
cp .env.example .env
nano .env


Ajusta las configuraciones de tu entorno, incluyendo la base de datos y otras claves necesarias.

Generar la Clave de la Aplicación:
bash
Copiar código
php artisan key:generate


Migrar la Base de Datos:
bash
Copiar código
php artisan migrate --force