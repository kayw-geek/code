

## 安装

确保你安装了 [Composer](https://getcomposer.org/):

```
composer require weikaiii/code
```

## 配置

1.打开laravel项目中 `config\app.php`

2.找到`providers`数组，在最下面添加` Weikaiii\Code\CodeServiceProvider::class`              注意 “**，**”





## 生成验证码

```php
<?php

namespace App\Http\Controllers;

use Illuminate\Http\Request;

class IndexController extends Controller
{
    public function index()
    {
        $app = app('code');//可以使用app全局函数 参数为code 生成code实例
         $app->make();		//make() 为生成验证码的方法
         echo $app->get(); //get() 为获取验证码的方法


    }
}
```

