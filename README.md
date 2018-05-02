# Forum

MVP components:

1. Thread
2. Reply
3. User

* A. Thread is created by a user
* B. A reply belongs to both a thread and a user

Commands:

1. laravel new forum
2. php artisan make:model Thread -mr
3. php artisan make:model Reply -mc
4. php artisan migrate
5. php artisan tinker
    6. $threads = factory('App\Thread', 50)->create();
    7. $threads->each(function ($thread) { factory('App\Reply', 10)->create(['thread_id' => $thread->id]); });