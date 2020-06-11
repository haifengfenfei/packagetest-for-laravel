### packagetest-for-laravel 发laravel扩展包

=========================================================

```
composer require haifengfenfei/packagetest-for-laravel 
```
# 修改 config/app.php 
 
# 添加服务 providers 
```
Haifengfenfei\Packagetest\PackagetestServiceProvider::class,
```

# aliases 配置别名： 
```
'Packagetest' => Haifengfenfei\Packagetest\Facades\Packagetest::class,
```
# 命令行执行加载指令 

```
composer dump-autoload 
```
# 发布资源文件
```
php artisan vendor:publish --provider="Haifengfenfei\Packagetest\PackagetestServiceProvider"

```



