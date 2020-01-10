# Atomic
## Components
apiやreduxに依存がないcomponentであることを示します。

### Atoms
simpleなcomponentです。
他のAtomsに依存してもよいですが、wrapする形での依存しか認めません。
例: Buttonに依存した、RoundButton等

#### 設計思想
どのサイトでも利用されるComponentで、どの場所でも利用されるような物を想定しています。

### Molecules
サイトに依存しないcomponentです。
サイトやページに依存する処理がありません。

#### 設計思想
サイトに依存しないcomponentとして利用するMoleculesに関しては、
Jobだけに依存する場合ではなく、Recruiterに依存する場合も含まれる可能性があるComponentを作成することを想定しています。
例: Table等

### Organisms
サイトに依存した処理が入っています。
Molecules以下を利用した、サイト固有のロジックを含めたコンポーネント。

Moleculesをwrapし、自身のmodelをpropsに受け取るものも含めます。

#### 設計思想
サイト内で再利用性の高いものをこちらで利用します。
JobCardや、JobList等を想定しています。

### Templates
APIに依存しないページ構成です。
useState等は使用可能
デザインに関数ロジックも導入可能

## Containers
### Pages
APIに依存する処理が入っている。
デザインに関するロジックは入れません。

## リファクタリングする上で
大きな単位から徐々に、下の層に分解するような形でリファクタリングする形でリファクタリングしてください。
