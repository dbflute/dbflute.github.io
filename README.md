<h1>DBfluteの使い方</h1>
<p>DBfluteの使い方を説明します。</p>
<h2>DBfluteとは何か</h2>
<p>DB変更に強い をテーマにした開発支援ツールです。</p>
<h2>DBfluteのインストールとセットアップ方法</h2>
<h3>1. DBFluteランタイムの設定 (JDBCドライバも)</h3>
<p>まずは pom.xml の dependencies に "DBFluteランタイム" の dependency を入れます。
propertiesタグに dbflute.version プロパティを定義しておくと、dbflute-maven-plugin がダウンロードするDBFluteエンジンのバージョンが同じになります。 (もし、propertiesがない場合、プラグインはruntimeの定義に関わらず最新バージョンをダウンロードします)</p>
<h2>How use DBflute activate</h2>
<p>O/Rマッパー、DB管理支援ツール</p>
