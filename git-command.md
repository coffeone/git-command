# 開発のながれ
1. ベースブランチに移動します、例えば、ベースブランチがdevelopの場合
```bash
git switch develop
```
2. 最新の状態を取得します
```bash
git pull
```

3. 自分のブランチに移動します、たとえば、自分のブランチがyht-branchの場合
```bash
git switch yht-branch
```

4. ベースブランチをマージします
```bash
git merge develop
```

5. マージした後,pushします
```bash
git push
```


# git 操作メモ

- repository project
    |- main-------> master-------> release(production)
    |- - develop----> develop
    |- - feature(bugfix)
    |- - yht-branch(add function)
    |- - - yht-branch(add function)
    |- - - -- yht-branch(add function)
    |- - zhangsan-branch(add function)

## git
local --- stage --- commit --- remote

1. local: 開発環境(バージョン管理していない)
2. stage: ステージング環境 (バージョン管理対象になる)
3. commit: ローカルリポジトリ(バージョン管理対象アップロード)
4. remote: リモートリポジトリ(バージョン管理レポジトリ)(gitlab, github)

dev process
  1. yht-branch 開発
  2. develop にマージ --> main マージ

1. リポジトリの作成

```bash
git init
```

2. リポジトリのクローン( main ブランチのみ)

```bash

```bash
git clone <URL>
```

3. 自分のブランチを作成(main ---> yht-branch)
```bash
git branch yt-branch
```

4. ブランチの名前変更
```bash
git branch -m yht-branch
```

5. ブランチの切り替え
```bash
git switch yht-branch
```


6. 開発作業(create file, edit file)
```bash
touch index.html
echo "Hello World" > index.html
```
7. ステージング(add)
```bash
git add .
```

8. コミット(commit)
```bash
git commit -m "add index.html"
```
9. プッシュ(push)
```bash
git push
```


# ファイルのキャンセル処理

1. 編集のしたファイルをキャンセル（add前)
```bash
git checkout -- <file>
```
2. 新規したファイルをキャンセル(add前)
```bash
git checkout  .
git clean -df
```

3. ステージングしたファイルをキャンセル(add)
```bash
git reset HEAD <file>
git reset --soft HEAD^
```

4. コミットしたファイルをキャンセル(commit)( --hard: ファイルも削除)
```bash
git reset --soft HEAD^ (add前の状態に戻る)
git reset --mixed HEAD^(add前の状態に戻る)
```


5. diff(差分確認) ( local と stage)
```bash
git diff
```

6. diff main branch(current branch and main branch)
```bash
git diff main
```

7. merge develop branch
```bash
git merge develop
```


