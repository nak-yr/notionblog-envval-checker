# notion-blog の環境変数の変更を検知するツール

本ツールは、notion-blog プロジェクトにて用いる環境変数について、
Notion 側での変更をチェックし、変更があれば通知するものである（予定)。

## Background

[notion-blog](https://github.com/ijjk/notion-blog)は、ijjk 氏が公開している、SSG や Notion 非公式 API を用いた
Next.js プロジェクトのサンプルである。

上記プロジェクトは記事の取得に NOTION_TOKEN などの環境変数を利用するが、
Notion 側でその変数が定期的に変更されると言う状況である。

環境変数が変更されると、notion-blog プロジェクト側で記事一覧が取得できない問題が発生する。
また、変更を定期的にチェックするのは面倒。

## Requirements

基本的にはシェルスクリプトとして作成予定。
`bash`　や　`zsh` で利用可能なようにしたい。

## Usage

あとで書く。

```bash
# 現在設定中の環境変数と差分がない場合
$ ./notionblog-envval-checker <Notion側の記事があるページのURL>
　Checking...
  Every environment valiables is up-to-date!

# 現在設定中の環境変数と差分がある場合
$ ./notionblog-envval-checker <Notion側の記事があるページのURL>
  Checking...
  We found x differences between local and internet.
  Please check below information for details.

  <Details>
  NOTION_TOKEN
    local : ...
    internet: ...

```

## License

This project is under [MIT license](https://en.wikipedia.org/wiki/MIT_License).
