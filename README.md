# yii2-qcloud-cos
yii2上传文件到腾讯云对象存储组件

[CHANGE LOG](CHANGELOG.md)

Installation
--------------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require xplqcloud/cos
```

or add

```json
"xplqcloud/cos": "*"
```

to the `require` section of your composer.json.


Configuration
--------------------

To use this extension, simply add the following code in your application configuration:

```php
return [
    //....
    'components' => [
        'cos'=>[
            'class'=>'xplqcloud\cos\Cos',
            'app_id' => 'app_id',
            'secret_id' => 'secret_id',
            'secret_key' => 'secret_key',
            'region' => 'region',
            'bucket'=>'bucket',
            'insertOnly'=>true,
            'timeout' => 200
        ],
    ],
];
```


[操作说明]
--------------------
```
//上传文件
\Yii::$app->cos->upload($src, $dst);

//删除文件
\Yii::$app->cos->delFile($dst);

//创建文件夹
\Yii::$app->cos->delFolder($folder);

//删除文件夹
\Yii::$app->cos->delFile($folder);

//获取文件夹列表
\Yii::$app->cos->listFolder($folder);
```
