# 技術書典21

技術加速研究所の技術書典21向け原稿です。Vivliostyleを使って、オンライン向けと印刷向けのPDFを生成します。

## 必要な環境

- [mise](https://mise.jdx.dev/)
- Node.js 24.2.0
- [pnpm 12.3.4](https://pnpm.io/)

Node.js と pnpm のバージョンは `mise.toml` で管理しています。

## セットアップ

```sh
mise install
mise exec -- pnpm install --frozen-lockfile
```

以降のコマンドは、mise のツールが有効なシェルでは `pnpm` から実行できます。有効化していない場合は、各コマンドの先頭に `mise exec --` を付けてください。

## PDFの生成

オンライン向けのカラーPDFを生成します。

```sh
pnpm run build
```

印刷向けPDFを生成します。

```sh
pnpm run build:print
```

生成物はプロジェクト直下の `screen.pdf` と `print.pdf` です。

GitHub Actionsでは、push、Pull Request、手動実行のいずれでもPDFをビルドし、アーティファクトとして保存します。

## プレビュー

```sh
pnpm run preview
```

## ライセンス

- `src/*` は原稿ファイルと画像ファイルなので、オープンソースとしてのライセンスは付与しません。
- サンプルコードは自由に利用できます。
- それ以外のファイルはMIT Licenseのもとで利用できます。

### 使用しているフォントのライセンス

License: SIL Open Font License, Version 1.1.

- https://github.com/microsoft/cascadia-code
- https://github.com/IBM/plex
- https://github.com/trueroad/HaranoAjiFonts
