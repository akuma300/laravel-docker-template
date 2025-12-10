# Laravel Lesson レビュー②

## Todo編集機能

### @method('PUT')を記述した行に何が出力されているか
input type="hidden" name="_method" value="PUT"のinputタグが出力されている

### findメソッドの引数に指定しているIDは何のIDか
編集したいTodoのIdカラムが入っている
### findメソッドで実行しているSQLは何か
SELECT文
### findメソッドで取得できる値は何か
idやcontentなどの1レコード分のデータ
### saveメソッドは何を基準にINSERTとUPDATEを切り替えているのか
idが設定されているか設定されていないかによって判別している。
## Todo論理削除

### traitとclassの違いとは
trait =インスタンス化できない・複数のトレイトを追加できる。
class =インスタンス化できる・親クラス１つのみ継承可能。
### traitを使用するメリットとは
いろいろなクラス間でコードを共通化・再利用できる
## その他

### TodoControllerクラスのコンストラクタはどのタイミングで実行されるか
コンストラクタインジェクションで生成したTodoクラスのインスタンスが呼び出されたときに実行される。
### RequestクラスからFormRequestクラスに変更した理由
バリデーションを行う専用のクラスを作成したことにより変更になった。
### $errorsのhasメソッドの引数・返り値は何か
引数　content　返り値：true / false
### $errorsのfirstメソッドの引数・返り値は何か
引数　content　返り値：messages
### フレームワークとは何か
枠組み
### MVCはどういったアーキテクチャか
開発効率を高めるために作られたアーキテクチャ
### ORMとは何か、またLaravelが使用しているORMは何か
プログラミング言語のClassとデータベースのテーブルをマッピング（関連付け）することでSQLを直接操作することなく
データベースとマッピングされたClassのメソッドを用いることでDBとやり取りを行うことができます。

LaravelではEloquentになる。
### composer.json, composer.lockとは何か
composer.json: プロジェクトが必要とするパッケージとそのバージョンが
記述されているファイル
composer.lock:　実際にインストールされたパッケージの正確なバージョンが
記録されるファイル
### composerでインストールしたパッケージ（ライブラリ）はどのディレクトリに格納されるのか
vendor ディレクトリに格納される
