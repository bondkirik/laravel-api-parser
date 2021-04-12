VK friends api parser on Laravel PHP ^8.0

API https://vk.com/dev/manuals 

1. Clone the project from git repository

`git clone ...`
   
2. Install dependencies

`composer install`

3. Copy ".env.example" to ".env" file

`cp .env.example .env`

4. Create a database named `DB_DATABASE` in ".env" file

`create database vk`

5. Generate new application security token

`php artisan key:generate`

6. Run database migrations

`php artisan migrate`

7. Create app for token
https://vk.com/apps?act=manage
`fill in .env.example`
VK_API_URL=
VK_API_ACCESS_TOKEN=
VK_API_VERSION=

8. Create console command
`php artisan make:command VkParse`
`php artisan vk:friends`

9. Create Queues table
`php artisan queue:table`

10. Update db and run jobs
`php artisan queue:work`
