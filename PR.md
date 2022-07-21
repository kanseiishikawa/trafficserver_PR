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
