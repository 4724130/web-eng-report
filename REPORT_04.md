# 第4回Webエンジニアリング演習レポート
## 学籍番号
4724130
## `const`と`let`の宣言・再代入に使用したコード
const courseName = "Web Engineering";
let retryCount = 1;
courseName = "Other Course"; // エラー確認後に削除する
retryCount = 2;
## VSCodeと`pnpm run check`に 表示されたエラー番号・メッセージ
const courseName: any
error TS2588: Cannot assign to 'courseName' because it is a constant.
Found 1 error in src/index.ts:19
[ELIFECYCLE] Command failed with exit code 2.
## 修正後の実行結果と`const`・`let`の違いの説明（コードまたは確認結果）
修正後のコード
const courseName = "Web Engineering";
let retryCount = 1;

retryCount = 2;

console.log(`Course: ${courseName}`);
console.log(`Retry count: ${retryCount}`);

実行結果
Course: Web Engineering
Retry count: 2

constとletの違い
constは変数への再代入ができないため、別の値を代入するとエラーが発生する。
letは再代入ができるため、後から値を変えるときはlet、変えないときはconstを使うのがよいと分かった。