# wist-bicycle

ウィスティリア中田マンション管理組合／駐輪シール管理システムの**公開ページ（包み）**。

中身は全部 Google Apps Script 側にある。このリポジトリに置いているのは `index.html` 1枚だけで、
やっているのは **自分のURLのクエリをそのまま GAS のWebアプリへ渡して iframe で表示する**ことだけ。

## なぜ必要か

GASのWebアプリを直接開くと、Googleが「このアプリケーションは Google Apps Script のユーザーによって
作成されたものです／不正行為を報告」という青いバナーを必ず出す。GAS側の設定では消せない
（Googleはこれを仕様としている）。**別ドメインのページに iframe で埋め込むと出ない。**

## LINE Developers 側の登録

このページのURLを、次の両方に登録する。

- LIFFアプリ（`駐輪シール`）の**エンドポイントURL**
- LINEログインの**コールバックURL**

## 直すとき

画面や処理を直すのは GAS 側（`~/Projects/Mansion/bicycle/gas/`）。
このファイルは、GASのデプロイURLが変わったときだけ直す。

仕様書：`~/Projects/Mansion/bicycle/docs/bicycle-parking-spec.md`
