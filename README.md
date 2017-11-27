PHP简单分页.

usage:

composer.phar require luochaolun/page dev-master

require 'vendor/autoload.php';
use LclTools\Page;

$count = 574;
$page = new Page($count, 25);
$limit = $page->get('limit');	//[0,10] 数组形式，方便Medoo中使用
$sql = "SELECT * FROM 表名 LIMIT " . implode(',', $limit);
echo $sql;