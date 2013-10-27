=== SEO BreadCrumb ===
Contributors: redsnow_
Tags: breadcrumb, topic path, microdata
Requires at least: 3.1
Tested up to: 3.7
Stable tag: 1.0.1

パンくずナビ（トピックパス）表示機能を追加します。

== Description ==
パンくずナビ（トピックパス）表示機能を追加します。表示タイプ、スタイルに関する多数のパラメータやパンくずナビ独自のプラグインフックが用意されており、フレキシブルなカスタマイズが可能です。
"[Prime Strategy Bread
Crumb](http://wordpress.org/plugins/prime-strategy-bread-crumb/
"WordPressbreadcrumb plugin")" を元に改修しています

= Examples =
**Default**<br />
Template Tag<br />
`
<?php if (function_exists('bread_crumb')) bread_crumb(); ?>
`
Output Sample<br />
`
<div id="breadcrumb" class="bread_crumb">
    <div itemscope itemtype="http://data-vocabulary.org/Breadcrumb">
        <a href="http://www.example.com/" itemprop="url">
            <span itemprop="title">Home</span>
        </a>  &gt; 
    </div>
    <div itemscope itemtype="http://data-vocabulary.org/Breadcrumb">
        <a href="http://www.example.com/?cat=2" itemprop="url">
            <span itemprop="title">Seminar</span>
        </a>  &gt; 
    </div>
    <div itemscope itemtype="http://data-vocabulary.org/Breadcrumb">
        <a href="http://www.example.com/?cat=4" itemprop="url">
            <span itemprop="title">Tokyo</span>
        </a>  &gt; 
    </div>
</div>
`

**List types**<br />
Template Tag<br />
`
<?php if (function_exists('bread_crumb')) bread_crumb('type=list'); ?>
`
Output sample<br />
`
<div id="breadcrumb" class="bread_crumb">
    <ul>
        <li itemscope itemtype="http://data-vocabulary.org/Breadcrumb" class="level-1 top">
            <a href="http://www.example.com/" itemprop="url">
                <span itemprop="title">トップページ</span>
            </a> &gt; 
        </li>
        <li itemscope itemtype="http://data-vocabulary.org/Breadcrumb" class="level-2 sub">
            <a href="http://www.example.com/?cat=2" itemprop="url">
                <span itemprop="title">Seminar</span>
            </a> &gt; 
        </li>
        <li itemscope itemtype="http://data-vocabulary.org/Breadcrumb" class="level-3 sub">
            <a href="http://www.example.com/?cat=4" itemprop="url">
                <span itemprop="title">Tokyo</span>
            </a> &gt; 
        </li>
    </ul>
</div>
`

= Special Thanks =

== Installation ==

1. pluginsフォルダに、ダウンロードした SEO BreadCrumb のフォルダをアップロードしてください。
2. プラグインページで "SEO BreadCrumb" を有効化して下さい。
3. 利用しているテーマのパンくずナビを表示したい箇所にページナビのテンプレートタグ "bread_crumb" を追加してください。テンプレートタグで指定できるパラメータについては、下記の Parameters を参照してください。

= Parameters =

**type**<br />
stringを指定すると、リストではなく文字列として出力します。デフォルトはlist

**home_label**<br />
トップページの表示テキスト。デフォルトは「トップページ」

**search_label**<br />
検索結果の表示テキスト。デフォルトは「『%s』の検索結果」（%sが検索文字列）

**404_label**<br />
404ページの表示テキスト。デフォルトは「404 Not Found」

**category_label**<br />
カテゴリーの表示テキスト。デフォルトは「%s」（%sがカテゴリー名）

**tag_label**<br />
投稿タグの表示テキスト。デフォルトは「%s」（%sが投稿タグ名）

**taxonomy_label**<br />
カスタムタクソノミーの表示テキスト。デフォルトは「%s」（%sがタクソノミー名）

**author_label**<br />
寄稿者の表示テキスト。デフォルトは「%s」（%sが寄稿者名）

**attachment_label**<br />
アタッチメントの表示テキスト。デフォルトは「%s」（%sがアタッチメント名）

**year_label**<br />
年の表示テキスト。デフォルトは「%s年」（%sが年の数字）

**month_label**<br />
月の表示テキスト。デフォルトは「%s」（%sは日付フォーマットで指定した月の表示設定）

**day_label**<br />
日の表示テキスト。デフォルトは「%s日」（%sが日の数字）

**post_type_label**<br />
カスタム投稿タイプアーカイブの表示テキスト。デフォルトは「%s」（%sがカスタム投稿タイプ名）

**joint_string**<br />
typeでstringを指定した場合の結合文字列。デフォルトは「 &amp;gt; 」（ > ）

**navi_element**<br />
ラッパー要素名。divまたはnavを選択可能。デフォルトは空（要素無し）

**elm_class**<br />
ラッパー要素のクラス名。ラッパー要素がなくタイプがリストの場合は、ulのクラス名となる。デフォルトは、「bread_crumb」

**elm_id**<br />
ラッパー要素のid名。ラッパー要素がなくタイプがリストの場合は、ulのid名となる。デフォルトは空。（idなし）

**li_class**<br />
タイプがリストの場合のliに付くクラス名。デフォルトは空（なし）

**class_prefix**<br />
各クラスに付く接頭辞。デフォルトは空（なし）

**current_class**<br />
表示中のページのパンくずナビに付与されるクラス名。デフォルトは「current」

**indent**<br />
タブでのインデント数。デフォルトは０。

**echo**<br />
出力を行うか。デフォルトはtrue（出力する）。0またはfalseの指定でPHPの値としてreturnする。 

**disp_current**<br />
表示中のページを表示するか。デフォルトはfalse（出力しない）0またはfalseの指定でPHPの値としてreturnする。

== Changelog ==
= 1.0.0 =
* 日本語翻訳ファイルを修正

= 1.0.0 =
* 一般公開


== Screenshots ==
1. パンくずナビ出力サンプル

== Links ==
