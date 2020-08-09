# Github

## ssh設定
https://qiita.com/0ta2/items/25c27d447378b13a1ac3

## git push取り消し
たまにやらかしてしまうので…。
https://awesome-linus.com/2019/03/09/git-push-by-mistake/

ローカルでの直前のコミットを取り消して、リモートブランチへ強制pushすることで修正
コマンドでローカルの直前のコミットを取り消しましょう！
```
$ git reset --hard HEAD^
```

+つけることで強制pushできる
```
$ git push origin +develop
```
