# PukiWiki用プラグイン<br>Base64画像表示 img64.inc.php

Base64エンコードされた画像を埋め込み表示する[PukiWiki](https://pukiwiki.osdn.jp/)用プラグイン。  
ファイルをアップロードすることなく、画像をページに直接埋め込むことができます。  
権限のない一般ユーザーでも任意の画像を掲載でき、添付ファイル管理の煩わしさからも解放されます。  
画像のBase64エンコーダーは「image base64 encoder」等でネット検索して見つけてください。

|対象PukiWikiバージョン|対象PHPバージョン|
|:---:|:---:|
|PukiWiki 1.5.3 ~ 1.5.4RC (UTF-8)|PHP 7.4 ~ 8.1|

## インストール

下記GitHubページからダウンロードした img64.inc.php を PukiWiki の plugin ディレクトリに配置してください。

[https://github.com/ikamonster/pukiwiki-img64](https://github.com/ikamonster/pukiwiki-img64)

## 使い方

```
#img64(画像のBase64エンコード文字列[,代替文字列])
```

## 使用例

```
#img64(data:image/jpeg;base64,xxxxxxxxx...)
```

## 設定

ソース内の下記の定数で動作を制御することができます。

|定数名|値|既定値|意味|
|:---|:---:|:---:|:---|
|PLUGIN_IMG64_MAXSIZE|数値|0|Base64文字列最大長（キロバイト）。0なら無制限|
