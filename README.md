## Coding test for the Backend Developer role - Search and Stay

The application was made using the Laravel framework.

- Laravel Version used: 9
- PHP Version used: 8.0

To install the application after cloning, you need to run the `composer install` command inside the application directory. After that you also need to copy the .env.example file to .env and set the database credentials.

That being done, you can now run the `php artisan migrate` command to create the needed tables for the application.

Since this application does not have a user registration path you need to manually create the user, to do it, run the `php artisan tinker`command and type the sequence below, changing the username and password to something of your choice.

```php
$user = new App\Models\User();
$user->password = Hash::make('the-password-of-choice');
$user->email = 'the-email@example.com';
$user->name = 'My Name';
$user->save();
```
Also, if needed, you can populate the database with the Book factory using the following command inside artisan tinker:

`Book::factory()->times(10)->create();`
