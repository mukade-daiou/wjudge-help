# WJudgeのスペシャルジャッジについて

## 入力

スペシャルジャッジを行うコード(以下ジャッジコード)に与えられる入力はユーザーの提出したコード(以下ユーザーコード)によって出力された結果とユーザーコードに与えた入力、ユーザーコードの行数、ユーザーコードが以下の形式で与えられる
```
ユーザーコードに与えた入力
ユーザーコードの出力
ユーザーコードの行数
ユーザーコード
```
不要なものは受け取らなくても構わない

## 出力

ジャッジコードによる出力は次の7種類のみを認識し、それ以外は`WrongAnswer`とみなす
- Accepted
- WrongAnswer
- TimeLimitExceeded
- RuntimeError
- CompileError
- MemoryLimitExceeded
- (0~9)のみによって構成される文字列
  
数字が出力された場合それをそのテストケースの入力の得点とする(テストケースに定められた点数は反映されない)

## 制約
ジャッジコードはC++及びPython3しか対応していない
ジャッジコードの実行時間が10秒を超過した場合処理は中断され`WrongAnswer`扱いとなる
