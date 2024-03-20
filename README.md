# Nova Countdown

A countdown card for Laravel Nova. Inspired by swooinc/nova-countdown

## Installation

Install the package with composer using the following command:

```
composer require morph07/nova-countdown
```

## Usage

You can pass a Carbon instance for the countdown.

```php
<?php

namespace App\Nova;

use Morph07\NovaCountdown\NovaCountdown;

class User extends Resource
{
    // Other methods
    
    /**
     * Get the cards available for the request.
     *
     * @param  \Illuminate\Http\Request  $request
     * @return array
     */
    public function cards(Request $request)
    {
        return [
            (new NovaCountdown)
                ->to(now()->addDays(30))
                ->label('30 Days Later'),
        ];
    }
}
```

## License

The MIT License (MIT). Please see [License File](https://github.com/morph07/nova-countdown/blob/master/LICENSE) for more information.
