## Exported names
Goでは、最初の文字が大文字で始まる名前は、外部のパッケージから参照できるエクスポート（公開）された名前( exported name )です。 例えば、 Pi は math パッケージでエクスポートされています。

小文字ではじまる pi や hoge などはエクスポートされていない名前です。

パッケージをインポートすると、そのパッケージがエクスポートしている名前を参照することができます。 エクスポートされていない名前(小文字ではじまる名前)は、外部のパッケージからアクセスすることはできません。

コードを実行し、エラーを確認してみましょう。

エラーを修正するために、 math.pi を math.Pi に書き換え、もう一度実行してみてください。

## Commands

```zsh
# 実行
go run ./basics/3/exported-names.go
```

## 備考

fmt.Printf(math.Pi)のケース
```zsh
go run ./basics/3/exported-names.go
# command-line-arguments
basics/3/exported-names.go:9:13: cannot use math.Pi (untyped float constant 3.14159) as string value in argument to fmt.Printf
```

fmt.Printf(math.pi)のケース
```zsh
go run ./basics/3/exported-names.go
# command-line-arguments
basics/3/exported-names.go:9:18: undefined: math.pi
```
