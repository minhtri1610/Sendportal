# Sendportal
### How to install sendportal in Laravel
#### create project laravel
```javascript
laravel new sources
```

### Clone sendportal packges core
```javascript
cd sources
mkdir packges
cd  packges
git clone https://github.com/mettle/sendportal-core.git
```

### Add config composer.json
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

### Rename packages sendportal core
cd sources/packges/sendportal-core
vi composer.json
"name": "packges/sendportal-core"

### Installation
### cd sources
composer install

### Config database in .env

### Publish vendor
php artisan vendor:publish --provider=Sendportal\\Base\\SendportalBaseServiceProvider

### Migrate
php artisan migrate

### Publish Assets with force
php artisan vendor:publish --provider=Sendportal\\Base\\SendportalBaseServiceProvider --force

### Set up account admin
php artisan sp:install


(Setup sendportal DockerFile)
