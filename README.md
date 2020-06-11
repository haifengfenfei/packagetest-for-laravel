### packagetest-for-laravel 发laravel扩展包

=========================================================

```
composer require haifengfenfei/packagetest-for-laravel 
```
# 修改 config/app.php 
 
# 添加服务: providers 
```
Haifengfenfei\Packagetest\PackagetestServiceProvider::class,
```

# 配置别名：aliases 
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

## 示例

# 创建控制器
```
php artisan make:controller TestController 
```

=======================================================

```
namespace App\Http\Controllers;

use Illuminate\Http\Request;
use Packagetest;

class TestController extends Controller
{
    public function index(){

    	$a = Packagetest::test_rtn('test');
        return view('Packagetest::packagetest',['msg'=>$a]);
    }
}
```


