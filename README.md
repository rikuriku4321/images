# images — 図の public ホスト

このリポジトリは **public**。唯一の目的: 研究の図(プロット)を、ChatGPT が取得できる **public な raw URL** で配信すること。

理由: ChatGPT の GitHub connector は GitHub 系 URL しか fetch できず、**private repo の画像は取得できない**。Cloudflare 等の外部 URL も connector は fetch しない。public な GitHub raw URL なら ChatGPT が vision で読める(検証済 2026-06-21)。

## 置くもの / 置かないもの
- 置く: **図のみ**(PNG / SVG / JPG)。
- 置かない: テキスト・数値・データ(CSV/JSON)・コード・ログ・生データ。**それらは private repo(research-lab / research)に残す**。
- ⚠ このリポジトリは**完全に公開**(誰でも閲覧・一覧可)。公開してよい図だけを置くこと。`.gitignore` で画像以外はコミット不可にしてある。

## 構造
```
<project>/<name>.png
```
例: `PolicyMap-Likelihood/2026-06-21_seed2-kl-recovery.png`

## raw URL
```
https://raw.githubusercontent.com/rikuriku4321/images/main/<project>/<name>.png
```
これを private repo(research-lab)の報告 markdown に埋め込むと、ChatGPT が図を読める。

## 公開フロー
`publish-figure <project> <figure-file...>`(deploy 鍵で push、raw URL を表示)。
手動なら: 図を `<project>/` に置いて commit & push。
