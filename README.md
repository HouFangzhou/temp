# temp
npm run production
composer install --optimize-autoloader --no-dev
php artisan config:cache
php artisan route:cache
php artisan view:cache
php artisan migrate:fresh --seed

php artisan db:seed --class=TestingSeeder
php artisan db:seed --class=TestingUserSeeder

SEEDER_LIMIT=6 php artisan db:seed --class=TestingNUsersSeeder
SEEDER_LIMIT=2 php artisan db:seed --class=TestingRemoveNUsersSeeder
