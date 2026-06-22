# images

研究で作った図(プロット)を置いておくための作業用リポジトリ。研究メモの図版置き場であり、AIが図を読み取るために使用。

AI は画像を URL から読み取るとき GitHub の raw URL しか取得できないため、図をここに置いて raw URL から参照している。
必要なときのみ public にする。

> Working repository that holds figures (plots) from ongoing research, used so an AI research assistant can read the plots via GitHub raw URLs. It is part of a research note-taking workflow.

## 中身・使い方

- 中身は図のみ(PNG / SVG / JPG)。テキスト・数値・データ・コード・ログは別の研究リポジトリに保管している(`.gitignore` で画像以外はコミットできないようにしてある)。
- 構造: `<project>/<name>.png`
- raw URL: `https://raw.githubusercontent.com/rikuriku4321/images/main/<project>/<name>.png`
- 図の追加: `publish-figure <project> <figure-file...>`、または `<project>/` に置いて commit & push。
