# git講習(4/3/2018 研修)

## git-flowとは
プロジェクトにおけるgitの運用方法のひとつ。
役割を持たせて各ブランチを切ることを提唱している
[Git-flowって何？ - Qiita](https://qiita.com/KosukeSone/items/514dd24828b485c69a05)


## コンフリクトマーカー
gitにpushする段階で吐かれるエラー
HEADが表すのはいくつ前のコミットか
[コンフリクトの解決 - Linux 入門](http://linux.keicode.com/prog/git-conflicts.php)


## git diffの使い方
**gitにステージングされてるファイルに対して変更を行った場合に表示される**
gitにステージングされてないファイルとステージングされているファイルの差分を表示するものではない

## `git add . ` or `git add (単体ファイル名)` ?
基本的には`git add .`で問題無い。
けど、実際に開発していく中でこの機能を実装したためこのファイルだけコミットしたい、とか、このバグを修正したためこのファイルだけをコミットしたい。みたいなタイミングで`git add (単体ファイル名)`でステージングして別々にcommitしてやる必要がある。
=> **コメントを分けれるから**

## `git merge`の方向
マージしたいファイルがあるブランチから`git merge  (マージさせたいブランチ名)`
ではなく、
マージさせたいブランチにあらかじめcheckoutしてから、
`git merge (マージしたいブランチ名)`
でマージさせる。
他動詞としてのmerge(溶け合わせる)ではなく、自動詞としてのmerge(溶け合う)
なので、mergeを反映したいブランチ上でmergeコマンドを実行するという考え方?なのかな

