**A Tour of Go: Imports**

**・ページの概要**  
Go言語におけるパッケージのインポート方法について説明されています。特に、複数のパッケージをインポートする際の「factored」インポート文の使用方法とそのスタイルについて触れられています。

**・サンプルコードとその説明**  
```go
package main

import (
 "fmt"
 "math"
)

func main() {
 fmt.Printf("Now you have %g problems.\n", math.Sqrt(7))
}
```
このコードでは、`fmt`と`math`の2つのパッケージをインポートしています。`main`関数内で、`fmt`の`Printf`関数と`math`の`Sqrt`関数を使用して、7の平方根を計算し、その結果を出力しています。

**・考えるべき点や質問とその答え**  
1. **Go言語での「factored」インポート文とは何ですか？**  
   - 「factored」インポート文は、複数のパッケージを一つの`import`文内で括弧を使用してまとめてインポートする方法を指します。

2. **なぜ「factored」インポート文を使用するのが良いスタイルとされていますか？**  
   - 「factored」インポート文を使用することで、コードが簡潔になり、追加や削除が容易になるため、読みやすく保守しやすいコードとなります。

3. **`math.Sqrt`関数は何を行う関数ですか？**  
   - `math.Sqrt`関数は、与えられた数値の平方根を計算して返す関数です。

**問題1**  
以下のコードは何を出力しますか？
```go
package main

import (
 "fmt"
 "math"
)

func main() {
 fmt.Printf("Square root of 16 is %g.\n", math.Sqrt(16))
}
```
<details>
  <summary>回答</summary>

出力: `Square root of 16 is 4.`

解説: `math.Sqrt(16)`は、16の平方根を計算するため、結果は4となります。

</details>

**問題2**  
以下のコードのエラーを修正して、`9.0`と出力するようにしてください。
```go
package main

import "fmt"

func main() {
 fmt.Printlin(math.Sqrt(81))
}
```
<details>
  <summary>回答</summary>

修正後のコード:
```go
package main

import (
 "fmt"
 "math"
)

func main() {
 fmt.Println(math.Sqrt(81))
}
```

解説: `Printlin`という関数は存在しないため、正しくは`Println`と記述する必要があります。また、`math`パッケージもインポートする必要があります。

</details>
