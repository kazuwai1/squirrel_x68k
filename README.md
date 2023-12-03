# Squirrel_x68k
組み込み系スクリプト言語の squirrel を X680x0向けにelf2x68環境でビルドして動かしてみました。
Makefileを修正するだけでとりあえず動くバイナリが作成できます。

## とりあえず使ってみる
- 本プロジェクトからリリースファイルをダウンロードします
- sq.xをx68k環境にコピーして実行するとREPLが起動します
- REPLは quit() を入力するか、ctrl-Cで終了できます
- REPL上で複数行にまたがるスクリプトを入力する場合は行末に "\\\\"を入力すると改行しても入力継続となります

## ビルド方法
[Squirrel 公式ページ](http://squirrel-lang.org/)  
[Squirrel github](https://github.com/albertodemichelis/squirrel/tree/master)  
[Squirrel 3.2 stable ソースコードをダウンロードできるページ](https://sourceforge.net/projects/squirrel/)  

[elf2x68k github](https://github.com/yunkya2/elf2x68k)

- ビルドするためには elf2x68k 20231202版以降のリリースをインストールした環境が必要です
- Squirrelのダウンロードページもしくはgithubからソースコードを入手してビルドPC上に展開します
- 本リポジトリの sq/Makefile, sqstdlib/Makefile, squirrel/Makefile をビルドするディレクトリに上書きします
- "make sq32"でビルドします
- binファイルに実行形式ファイル、libディレクトリにライブラリファイルが作成されます
- C/C++プログラムに組み込む場合は includeディレクトリのヘッダファイルも必要になります。etcディレクトリのファイルを参考にしてください。

## ライセンスについて
- squirrel のオリジナルの COPYRIGHT ファイルを本プロジェクトに追加しています
- x68k向けの実行ファイル、Makefileに関するライセンスはオリジナルの取り扱いに準じます
