# よく使うDockerfile

AWS クレデンシャルセット
クレデンシャルディレクトリを用意してそこから呼び出し、環境変数に通す。

``` bash
mkdir credential
```

jsonファイルを読み込み
``` bash
touch aws_credentials.json
```

クレデンシャル書き込み
``` aws_credentials.json
{
  "AccessKeyId": "XXXX",
  "SecretAccessKey": "XXXX"
}
```
