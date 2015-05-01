#DBFlute
JFluteのDBFrameworks!
##DBFluteとは？
DB変更に強い をテーマにした開発支援ツール
リーン・スタートアップ＆インクリメンタル開発
設計しながら実装する開発 (納期の短い開発)
ビジネス要求の変化が激しいシステム開発が増えてきました。DB変更は日常の風景。そんな現場でDB変更に対しアプリケーションが できるだけスピーディーに 対応できるようにするために、DBFlute は大きく二つの機能を備えています。
O/Rマッパー
自動生成ドリブンでDB変更の影響範囲をスピーディーに検知
DB管理支援ツール
DB環境構築自動化や履歴管理など、DB変更の運用上の悩みを解決
両方の機能を利用することで最大の効果を得られますが、開発運用支援ツールの機能だけを利用することも可能であり、様々なアーキテクチャと組み合わせて利用することもできます。
 
##DBFluteのセットアップ
DBFluteのセットアップには大きく四つの方法があります。
DBFluteのサポート情報
Maven DBFlute Plugin でコマンドからセットアップ ※Java8 (1.1.x) はこちら
Maven の pom.xml に必要な情報を記述し、DBFluteクライアントを作成します。
EMecha (Eclipse Plugin) で Eclipse にてセットアップ ※Java6,7 (1.0.x) はこちら
Eclipse上でウィザード画面から必要な情報を入力し、DBFluteクライアント作成とDBFluteモジュールのダウンロードと配置が可能です。 (Java版の1.0.x用のみ、Java8の1.1.xからは別の方法で)
テンプレートを利用して手動でセットアップ ※.NET(C#) or Java8でMaven使わないならこちら
DBFluteエンジンをサイトからダウンロードし、その中に含まれているDBFluteクライアントのテンプレートを手動修正します。他の方法が利用できないときのための方法です。


##チュートリアル
http://dbflute.seasar.org/ja/tutorial/architect.html
http://dbflute.seasar.org/ja/tutorial/developer.html
