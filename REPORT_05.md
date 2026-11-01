# 第5回 Webエンジニアリング演習 レポート


## 学籍番号
4724130


## TODO配列のコード
const todos = [
{ id: 1, title: "型を復習する", completed: true },
{ id: 2, title: "配列を学ぶ", completed: false },
{ id: 3, title: "レポートを書く", completed: false },
{ id: 4, title: "ファイルを開く", completed: false }
];


## TODOを更新した 条件
for  ofとifを使い、completedがfalseのTODOをすべてtrueに更新した。


## 完了件数の 更新前後の 実行結果
$ tsx src/index.ts
1: 型を復習する [完了]
2: 配列を学ぶ [未完了]
3: レポートを書く [未完了]
4: ファイルを開く [未完了]
[ { id: 1, title: '型を復習する', completed: true } ]
[ '型を復習する', '配列を学ぶ', 'レポートを書く', 'ファイルを開く' ]
更新後: 配列を学ぶ [完了]
更新後: レポートを書く [完了]
更新後: ファイルを開く [完了]
完了件数: 更新前 1件 -> 更新後 4件