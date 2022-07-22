# [#8975](https://github.com/apache/trafficserver/pull/8975) Fix reverting PR#7302
[#7302](https://github.com/apache/trafficserver/pull/7302)のrevert
HttpSM::send_origin_throttled_response()が二回呼び出されクラッシュする

# [#8971](https://github.com/apache/trafficserver/pull/8971) Fixes issue with file size calculation for existing logs
ログのファイルサイズ計算の不具合の修正
既存のファイルのバイト数が考慮されていなかった

# [#8965](https://github.com/apache/trafficserver/pull/8965) Proxy Verifier: Update to version 2.4.1
Proxy Verifierを2.4.1にバージョンアップ
これによってALPNの検証ができる
ALPNはTLS拡張 アプリケーションレイヤープロトコルのこと

# [#8957](https://github.com/apache/trafficserver/pull/8957) Remove unneccessary const qualifiers
いらないconstの削除

# [#8954](https://github.com/apache/trafficserver/pull/8954) Use std::unique_ptr for X509 and BIO scoped heap objects.
X509とBIOでstd::unique_ptrを使用するように変更
std::unique_ptrはリソースへの所有権を唯一持つポインタでコピーを行おうとするとエラーが発生する。

# [#8953](https://github.com/apache/trafficserver/pull/8953) Hostdb Restructure (要確認!)
HostDBの再構築

# [#8950](https://github.com/apache/trafficserver/pull/8950) .fit/fmt/.clang-format-installed prerequisite
clang-formatが既にinstallされている際の条件変更

# [#8947](https://github.com/apache/trafficserver/pull/8947) Enable warning for deprecated declarations on macOS
[#8946](https://github.com/apache/trafficserver/pull/8946)のマージによってmacOsで非推奨の宣言による警告を有効化

# [#8946](https://github.com/apache/trafficserver/pull/8946) Remove use of sbrk()
sbrkはarm64のプラットフォームのFreeBSDは使用できず、maxOsでは非推奨とされている。
sbrkはメモリ使用量のチェックに使われているが、他のツールでもメモリ使用量の監視はできるのであまり役に立たない。
arm64: 64ビット単位で処理をするCPUの設計
FreeBSD: Unix風のOs

# [#8945](https://github.com/apache/trafficserver/pull/8945) Grants some karma to active contributors which are not committers
コミッターではないアクティブな貢献者にカルマの付与
これらの人々はissueとPRのトリアージができるようになる

# [#8944](https://github.com/apache/trafficserver/pull/8944) Make the autopep8 clang-format targets quieter 
autopep8とclang-formatの対象をを変更したファイルのみに変更

# [#8943](https://github.com/apache/trafficserver/pull/8943) Fix doc formatting for rate_limit plugin
rate_limitプラグインのドキュメントフォーマットを修正

# [#8942](https://github.com/apache/trafficserver/pull/8942) Fix doc formatting for plugin remap_stats
remap_statsのドキュメント修正

# [#8940](https://github.com/apache/trafficserver/pull/8940) Fix the body_buffer AuTest for 10-Dev
body_bufferのAutestの修正
出力をstderrからtraffic.outに変更

# [#8937](https://github.com/apache/trafficserver/pull/8937) Add nullptr check of HTTPInfo
cache_info.object_readのnullチェックの追加

# [#8935](https://github.com/apache/trafficserver/pull/8935) Make clang-format not modify ink_autoconf.h.in and ink_autoconf.h
ink_autoconf.h.inとink_autoconf.hをautoconfを使って作成した後にbuildをしてclang-formatをするとmakeが再び呼び出された時にほとんどのファイルを再構築することになるため修正

# [#8932](https://github.com/apache/trafficserver/pull/8932) Initialize TLSTunnelSupport on startup
起動時にTLSTunnelSupportを初期化

# [#8931](https://github.com/apache/trafficserver/pull/8931) Fix clang-format installation with multiple threads
clang-formatを他のターゲットがinstallしなくなる

# [#8928](https://github.com/apache/trafficserver/pull/8928) proxy_serve_stale: Test updates
proxy_serve_staleテストがより高速に実行されるように変更

# [#8927](https://github.com/apache/trafficserver/pull/8927) Add docs for remap_stats plugin
remap_statsプラグインにdocumetの追加

# [#8926](https://github.com/apache/trafficserver/pull/8926) Allows errors from plugin initialization to bubble up
プラグインの初期化のエラーが出るように変更
以前まではプラグインの初期化に失敗した場合、DSOをアンロードしようとするとinitのエラーメッセージが消されてた。
DSO: 動的共有オブジェクト

# [#8925](https://github.com/apache/trafficserver/pull/8925) Cleanup. Remove unnecessary use of a memory arena when logging.
logging時に不要なメモリの削除

# [#8924](https://github.com/apache/trafficserver/pull/8924) Update location for core rule set in modsecurity example
documentのURL変更

# [#8923](https://github.com/apache/trafficserver/pull/8923) JSONRPC: Deal with an empty id as an id error.
JSONRPCでidが空のときにエラーが返るように変更
JSONRPC: エンコードにJSONを採用したプロトコルの一種

# [#8922](https://github.com/apache/trafficserver/pull/8922) Use std::variant to clean up handling of unmarshal functions.
std::variantを使ってunmarshal関数をきれいに
std::variant: 格納される候補の型を切り替えながら使用できる記憶型
