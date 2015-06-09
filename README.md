# faceplusplus
Face++ PHP Software Development Kit

### 如何安装
1.  使用 composer
  ```
  composer require "ibuffer/faceplusplus:0.0.*"
  ```

2.  手动安装
    下载指定版本 https://github.com/ibuffer/faceplusplus/releases<br />
    然后直接加载 facepp.php 即可使用

### 如何使用
$facepp = new facepp($api_key, $api_secret);<br />
$response = $facepp->execute(接口名称, 参数数组);<br />
接口名称、参数数组以及返回值，请参考 [Face++API文档](http://www.faceplusplus.com.cn/api-overview)

例如:
```
$api_key = 'api key(请修改)';
$api_secret = 'api secret(请修改)';
$facepp = new facepp($api_key, $api_secret);
$params = array(
    'url'          =>   '图片链接(请修改)',
    'attribute'    =>   'gender,age,race,smiling,glass,pose'
);
$response = $facepp->execute('/detection/detect',$params);
```
  
