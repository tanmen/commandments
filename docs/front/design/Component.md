# Component and Container
## Component
apiやreduxに依存がないcomponentであることを示します。
Design向けロジックはこちらに依存します。

## Container
Apiやreduxへの処理に依存しています。
stateからの複雑な処理dataを整形したりする処理はこちらに書きます。
