### packagetest-for-laravel 发laravel扩展包

=========================================================

```
composer require haifengfenfei/packagetest-for-laravel 
```

添加服务： 修改 config/app.php 
providers 添加 
```
Haifengfenfei\Packagetest\PackagetestServiceProvider::class,
```

aliases 别名的配置： 
```
'Packagetest' => Haifengfenfei\Packagetest\Facades\Packagetest::class,
```
命令行执行加载指令 

```
composer dump-autoload 
```



