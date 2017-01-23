## Laravel 5.2 OneSignal

A Onesignal package for Laravel 5.2 or higher
 
##Installation

````
composer require moathdev/sweetalert
````

Setting up your OneSignal account on your  Enverament file

````
ONESIGNAL_APP_ID=759xxxxxxx

ONESIGNAL_AUTHORIZATION=MjYzxxxxxx
````
##Example Usage
````
use Moathdev\OneSignal\FailedToSendNotificationException;
use Moathdev\OneSignal\OneSignal;


Route::get('/', function (OneSignal $oneSignal) {
    try {

        $res = $oneSignal->SendNotificationToAll('Hello', 'World', [
        ]);

    } catch (FailedToSendNotificationException $e) {

        dd($e);
    }
    dd($res);
});
 ````
 ##Issues

````

If you have any questions or issues, please open an Issue .