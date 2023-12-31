**A Tour of Go: 関数**

**・ページの概要**  
Go言語における関数の定義と使用方法について説明されています。関数は0個以上の引数を取ることができ、変数名の後に型を記述することが特徴です。

**・サンプルコードとその説明**  
```go
package main

import "fmt"

func add(x int, y int) int {
 return x + y
}

func main() {
 fmt.Println(add(42, 13))
}
```
このコードでは、`add`という関数を定義しています。この関数は2つの整数型の引数を取り、それらの合計を返します。`main`関数内で、`add`関数を呼び出して42と13の合計値を出力しています。

**・考えるべき点や質問とその答え**  
1. **Go言語での関数の定義方法や呼び出し方にはどのような特徴がありますか？**  
   - Go言語では、関数を定義する際に、変数名の後に型を記述します。また、関数の戻り値の型も関数名の後に記述します。

2. **関数の引数や戻り値の型の記述位置は他の言語とどのように異なりますか？**  
   - 多くの言語では、型の宣言が変数名の前に来るのに対し、Go言語では変数名の後に型を記述します。

3. **関数の引数が複数ある場合、それらの型が同じであればどのように簡潔に記述できますか？**  
   - 引数が複数あり、それらの型が同じ場合、変数名をカンマで区切って列挙し、その後に共通の型を1回だけ記述することで簡潔に表現できます。例: `func add(x, y int) int`

**問題1**  
以下の関数`multiply`は、2つの整数を引数として取り、それらの積を返す関数です。この関数を完成させてください。
```go
func multiply(?, ?) ? {
 return ? * ?
}
```
<details>
  <summary>回答</summary>

```go
func multiply(x int, y int) int {
 return x * y
}
```
解説: `multiply`関数は2つの整数を引数として取るため、引数の型は`int`となります。また、戻り値も整数型のため、戻り値の型も`int`となります。

</details>

**問題2**  
以下のコードは何を出力しますか？
```go
package main

import "fmt"

func subtract(x int, y int) int {
 return x - y
}

func main() {
 fmt.Println(subtract(15, 5))
}
```
<details>
  <summary>回答</summary>

出力: `10`

解説: `subtract`関数は、第1引数から第2引数を引いた結果を返します。この場合、15から5を引いた結果、10が出力されます。

</details>
