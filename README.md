# Sendportal
### How to install sendportal in Laravel
#### create project laravel
```javascript
laravel new sources
```

### clone sendportal packges core
cd sources
mkdir packges
cd  packges
git clone https://github.com/mettle/sendportal-core.git

### add config composer.json
cd sources
vi composer.json
```javascript
"repositories": [
    {
            "type": "path",
            "url": "packges/sendportal-core",
            "options": {
                "symlink": true
            }
    
    }],

"require": {
    "packges/sendportal-core": "*"
}
```

### rename packages sendportal core
cd sources/packges/sendportal-core
vi composer.json
"name": "packges/sendportal-core"

### installation
### cd sources
composer install

### config database in .env

### publish vendor
php artisan vendor:publish --provider=Sendportal\\Base\\SendportalBaseServiceProvider

### migrate
php artisan migrate

### Publish Assets with force
php artisan vendor:publish --provider=Sendportal\\Base\\SendportalBaseServiceProvider --force

### Set up account admin
php artisan sp:install


(Setup sendportal DockerFile)
