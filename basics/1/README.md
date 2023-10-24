**A Tour of Go: パッケージ**

**・ページの概要**  
Go言語のプログラムは、複数のパッケージから構成されます。プログラムの実行は`main`パッケージから開始されます。このページでは、`fmt`と`math/rand`というインポートパスを持つパッケージの使用方法について説明されています。慣習として、パッケージ名はインポートパスの最後の要素と同じ名前になります。例えば、`math/rand`パッケージは`package rand`という文で始まるファイルから構成されます。

**・サンプルコードとその説明**  
```go
package main

import (
 "fmt"
 "math/rand"
)

func main() {
 fmt.Println("My favorite number is", rand.Intn(10))
}
```
このコードでは、`fmt`と`math/rand`の2つのパッケージをインポートしています。`main`関数内で、`fmt`の`Println`関数と`math/rand`の`Intn`関数を使用して、0から9までのランダムな整数を出力しています。

**・考えるべき点や質問とその答え**  
1. **Go言語のパッケージとは何ですか？**  
   - Go言語のパッケージは、関連する関数、型、変数などのコードの集まりです。パッケージを使用することで、コードの再利用やモジュール性を向上させることができます。

2. **`main`パッケージの特徴は何ですか？**  
   - `main`パッケージは、Goプログラムのエントリーポイントとなる特別なパッケージです。`main`関数を持つ`main`パッケージからプログラムの実行が開始されます。

3. **`rand.Intn(10)`の動作はどのようなものですか？**  
   - `rand.Intn(10)`は、0から9までのランダムな整数を返す関数です。引数に与えられた値よりも小さい非負の整数を返します。

**問題1**  
以下のコードは何を出力しますか？
```go
package main

import (
 "fmt"
 "math/rand"
)

func main() {
 fmt.Println("Random number:", rand.Intn(5))
}
```
<details>
  <summary>回答</summary>

出力: `Random number:`の後に0から4までのランダムな整数が表示されます。

解説: `rand.Intn(5)`は、0から4までのランダムな整数を返す関数です。

</details>

**問題2**  
以下のコードのエラーを修正して、`Hello, Go!`と出力するようにしてください。
```go
package main

import "fmt"

func main() {
 fmt.Printlin("Hello, Go!")
}
```
<details>
  <summary>回答</summary>

修正後のコード:
```go
package main

import "fmt"

func main() {
 fmt.Println("Hello, Go!")
}
```

解説: `Printlin`という関数は存在しないため、正しくは`Println`と記述する必要があります。

</details>
