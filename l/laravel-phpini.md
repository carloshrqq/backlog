---
created: 2025-02-28 04:46
tags:
  - "#new"
  - "#new/tags"
  - "#new/pkm"
  - "#review"
---
_Data da última atualização do texto  `=dateformat(this.file.mtime, "yyyy-MM-dd HH:mm")`_
#new #new/tags #new/pkm #review
# php artisan serve fix

You need to change the `variables_order` value to `GPCS` in php.ini file. For Herd users on Windows, here is how you can do it:

1. Right click on Herd icon and click **Open configuration files** [![Herd Open Configuration Files](https://i.sstatic.net/2BKLKUM6.png)](https://i.sstatic.net/2BKLKUM6.png)
    
2. Navigate to `bin` folder > Click on which php version you use (eg `php82` or `php83` > Find `php.ini` file. Here is usually where it sits: `"C:\Users\<username>\.config\herd\bin\php82\php.ini"`
    
3. Open the file using text editor
    
4. Find the part with `variables_order` and change the value to `GPCS`.
    

[![php.ini variables_order](https://i.sstatic.net/Z4QQx9Cm.png)](https://i.sstatic.net/Z4QQx9Cm.png)

1. Save the file and retry the artisan serve command from your project

# AutoReload/Hot on blade.php files

https://laracasts.com/discuss/channels/vite/no-hot-reload-with-new-laravel-vite

[pverhaert](https://laracasts.com/@pverhaert)

[Posted 2 years ago](https://laracasts.com/discuss/channels/vite/no-hot-reload-with-new-laravel-vite?reply=824589)

[@DanielTamargo](https://laracasts.com/@DanielTamargo) Problem found. I installed Laravel with Jetstream (Livewire) and it modified my `vite.config.js`.

Just did a complete fresh installation (v 9.27.0).

In `vite.config.js` you don't have to change anything at all.

`package.json/vite.config.js` 
```php
import { defineConfig } from 'vite';
import laravel from 'laravel-vite-plugin';

export default defineConfig({
    plugins: [
        laravel({
            input: ['resources/css/app.css', 'resources/js/app.js'],
            refresh: true,
        }),
    ],
});
```

Just add to the all blade files and hot reload will works with `npm run dev`
For example:
resources/views/welcome.blade.php
```html
<head>
		...
		@vite(['resources/css/app.css', 'resources/js/app.js'])
</head>
```

Open bash terminal

`npm run dev`

Then open cmd terminal

`php artisan serve`