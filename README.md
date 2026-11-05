# Academic Ethics ウェブサイト

Quarto で生成し、GitHub Pages で公開する研究会サイトのソース。

- 公開先（予定）: https://academic-ethics.github.io/
- 公開の仕組み: `main` へ push すると GitHub Actions（`.github/workflows/publish.yml`）がサイトを生成して公開する

## ファイル構成

| file | 内容 |
|---|---|
| `_quarto.yml` | サイト名、ナビゲーション、テーマ |
| `index.qmd` | ホーム。開催予定の回を最大3件表示 |
| `events.qmd` | 開催案内（`status: "予定"` の回の一覧） |
| `archive.qmd` | 開催記録（`status: "終了"` の回の一覧） |
| `about.qmd` | 趣旨、運営、問い合わせ |
| `events/*.qmd` | 各回のページ。1回につき1file |
| `_templates/event.qmd` | 各回のページの雛形（公開されない） |
| `styles.scss` | 見た目の調整 |

## 次回の開催案内を加える

1. `_templates/event.qmd` を `events/YYYY-MM-DD-短い名前.qmd` に複製する
2. 題、日付、会場、申込URLなどを書き換える（`status: "予定"`）
3. プレビューで確認し、branch を作って Pull Request を出す
4. レビュー後に `main` へ merge すると数分で公開される

開催後は、その回の `status` を `"終了"` に変え、必要なら「記録」の節を書く。開催案内から開催記録へ自動で移る。

公開前の下書きは `draft: true` にする。プレビューには出るが、公開サイトには出ない。

## 手元で確認する

```bash
quarto preview
```

## 載せないもの

- 非公開の議事録、内部資料、参加者名簿（このrepoは公開される）
- 本人の了承のない氏名・所属、個人のメールアドレス
