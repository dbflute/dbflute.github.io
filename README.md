README.mdを付け足してみる
# DBFlute

## DB変更に強い をテーマにした開発支援ツール

- リーン・スタートアップ＆インクリメンタル開発
- 設計しながら実装する開発 (納期の短い開発)

ビジネス要求の変化が激しいシステム開発が増えてきました。DB変更は日常の風景。そんな現場でDB変更に対しアプリケーションが できるだけスピーディーに 対応できるようにするために、DBFlute は大きく二つの機能を備えています。

- O/Rマッパー
  - 自動生成ドリブンでDB変更の影響範囲をスピーディーに検知
- DB管理支援ツール
  - DB環境構築自動化や履歴管理など、DB変更の運用上の悩みを解決

両方の機能を利用することで最大の効果を得られますが、開発運用支援ツールの機能だけを利用することも可能であり、様々なアーキテクチャと組み合わせて利用することもできます。

## セットアップ方法
DBFluteのセットアップには大きく四つの方法があります。 [DBFluteのサポート情報](http://dbflute.seasar.org/ja/environment/supported.html)

- **[Maven DBFlute Plugin でコマンドからセットアップ](http://dbflute.seasar.org/ja/environment/setup/maven.html)** ※Java8 (1.1.x) はこちら
  - Maven の pom.xml に必要な情報を記述し、DBFluteクライアントを作成します。
- **[EMecha (Eclipse Plugin) で Eclipse にてセットアップ](http://dbflute.seasar.org/ja/environment/setup/emecha.html)** ※Java6,7 (1.0.x) はこちら
  - Eclipse上でウィザード画面から必要な情報を入力し、DBFluteクライアント作成とDBFluteモジュールのダウンロードと配置が可能です。 (Java版の1.0.x用のみ、Java8の1.1.xからは別の方法で)
- **[テンプレートを利用して手動でセットアップ](http://dbflute.seasar.org/ja/environment/setup/plain.html)** ※.NET(C#) or Java8でMaven使わないならこちら
  - DBFluteエンジンをサイトからダウンロードし、その中に含まれているDBFluteクライアントのテンプレートを手動修正します。他の方法が利用できないときのための方法です。


## DBFluteのマニュアル
### チュートリアルあります

ここはいわゆる "分厚い本のマニュアル" のようなもので、構造的に網羅された仕様書です。  
なので、機能を探すときは "テーマごとのチュートリアル" がオススメです。
- アーキテクト向け [アーキテクトのためのチュートリアル](http://dbflute.seasar.org/ja/tutorial/architect.html)
- ディベロッパー向け [ディベロッパーのためのチュートリアル](http://dbflute.seasar.org/ja/tutorial/developer.html)
- パッと見たいとき [ひとめでDBFlute](http://dbflute.seasar.org/ja/tutorial/hitomeflute.html)

###機能マニュアル
BFluteの機能に関するマニュアル(機能マニュアル)です。
[機能マニュアルのトップ](http://dbflute.seasar.org/ja/manual/function/index.html)
- [自動生成ツール](http://dbflute.seasar.org/ja/manual/function/generator/index.html)
メタ情報からクラスを自動生成する
  - [DBFlute Client](http://dbflute.seasar.org/ja/manual/function/generator/client/index.html)
DBFluteクライアント：DBFluteを利用するためのアプリケーション設定を含むディレクトリ
  - [DBFlute Module](http://dbflute.seasar.org/ja/manual/function/generator/module/index.html)
DBFluteモジュール：DBFluteの本体で、自動生成などの実処理を行うモジュール
  - [DBFlute Task](http://dbflute.seasar.org/ja/manual/function/generator/task/index.html)
DBFluteタスク：DBFluteが提供する Ant タスク
- [O/Rマッパ](http://dbflute.seasar.org/ja/manual/function/ormapper/index.html)
アプリケーション上でDBにアクセスする
  - [Behavior](http://dbflute.seasar.org/ja/manual/function/ormapper/behavior/index.html)
全てのDBアクセスの処理を司る
  - [ConditionBean](http://dbflute.seasar.org/ja/manual/function/ormapper/conditionbean/index.html)
検索条件を組み立てる
  - [OutsideSql](http://dbflute.seasar.org/ja/manual/function/ormapper/outsidesql/index.html)
外部ファイルのSQL(2Way-SQL)を実行する
  - [Entity](http://dbflute.seasar.org/ja/manual/function/ormapper/entity/index.html)
データ(レコード)を格納する
  - [DBFlute Runtime](http://dbflute.seasar.org/ja/manual/function/ormapper/runtime/index.html)
DBFluteランタイム：アプリケーションの実行時に必要なライブラリ(JAR)
- [現場フィット](http://dbflute.seasar.org/ja/manual/function/genbafit/index.html)
様々な局面で現場にフィットした支援
  - [Implementation Fit](http://dbflute.seasar.org/ja/manual/function/genbafit/implfit/index.html)
アプリ実装の全体最適
  - [Project Fit](http://dbflute.seasar.org/ja/manual/function/genbafit/projectfit/index.html)
プロジェクト構成対応
  - [Runtime Fit](http://dbflute.seasar.org/ja/manual/function/genbafit/runtimefit/index.html)
実行時共通要件の実現
  - [DBFlute Fit](http://dbflute.seasar.org/ja/manual/function/genbafit/dbflutefit/index.html)
DBFlute利用のサポート
  - [Deprecated Fit](http://dbflute.seasar.org/ja/manual/function/genbafit/deprecatedfit/index.html)
非推奨な構造フォロー
- [支援ツール](http://dbflute.seasar.org/ja/manual/function/helper/index.html)
EclipseプラグインやMavenプラグインなど
  - [EMecha(Eclipse Plugin)](http://dbflute.seasar.org/ja/manual/function/helper/emecha/index.html)
環境支援・実装支援のEclipseプラグイン
  - [Maven DBFlute Plugin](http://dbflute.seasar.org/ja/manual/function/helper/maven/index.html)
環境支援のMavenプラグイン

### リファレンス
機能マニュアルを補完する様々な参考資料(リファレンス)です。
[リファレンスのトップ](http://dbflute.seasar.org/ja/manual/reference/index.html)
- [DBMS Way](http://dbflute.seasar.org/ja/manual/reference/dbway/index.html)
DBMSごとの取扱い
- [DI Container Way](http://dbflute.seasar.org/ja/manual/reference/diway/index.html)
DIコンテナごとの取扱い
- [DBFlute Property](http://dbflute.seasar.org/ja/manual/reference/dfprop/index.html)
DBFluteプロパティ(DBFluteの設定)
- [DBFlute Dictionary](http://dbflute.seasar.org/ja/manual/reference/dictionary/index.html)
DBFluteの世界で利用される用語の辞書
- [DBFlute Example](http://dbflute.seasar.org/ja/manual/reference/example/index.html)
DBFluteを使ったプロジェクトの実装例
