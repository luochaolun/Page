PHP简单分页.

安装方法:

composer.phar require luochaolun/page dev-master

使用方法：
require 'vendor/autoload.php';

use LclTools\Page;

$count = 574;

$page = new Page($count, 25);

$limit = $page->get('limit');	//[0,10] 数组形式，方便Medoo中使用

$sql = "SELECT * FROM 表名 LIMIT " . implode(',', $limit);

echo $sql;