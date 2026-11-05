# AIエージェント向けの作業指示

- このrepoは公開される。非公開の議事録、内部資料、参加者の個人情報、了承のない氏名を書かない。
- 新しい回は `_templates/event.qmd` を複製して `events/YYYY-MM-DD-短い名前.qmd` に作る。既存の回と同じfront matterの項目を使う。
- 開催後の回は `status: "終了"` に変える。ファイルは移動しない。
- 変更はbranchとPull Requestで出し、`main` へ直接pushしない。
- 変更後は `quarto render` が警告なく通ることを確認する。
- 日付・会場・申込URLなど依頼に書かれていない事実を推測で埋めない。不明な項目は「（未定）」とする。
