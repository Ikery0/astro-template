# Astro 基本テンプレート

ざっと必要そうなとこだけ日本語訳＆追記

## 🚀 Project Structure

```text
/
├── public/
│   └── favicon.svg
├── src/
├   ├──js/
│   │   └── lib/
│   │   │   └── scroll.js
│   │   └── meta.js
│   ├── components/
│   │   └── Card.astro
│   ├── layouts/
│   │   └── Layout.astro
│   └── pages/
│       └── index.astro
└── package.json
```

ページは `src/pages/` に入れてく

コンポーネントフォルダ `src/components/` にコンポーネントは入れる
コンポーネントの粒度は決めてないのでやってみていい感じにする

静的アセット(画像などは)`public/` に入れてく
いい感じにディレクトリ切る

共通のもの(reset.css や common.css)は基本 Layout.astro で読み込む
あまり読み込ませすぎると邪魔になりそうなので、
スタイルは.astro ファイルの中でコンポーネント毎に当てる方がいいと思う
js も全体に必要なもの以外はコンポーネント内で読む方がいいかも

meta 周りは`src/js/meta.js`にページ毎に連想配列を書いてく
必要に応じて項目を増やしたり、共通するものはまとめるなどする

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro ...`       | Run CLI commands like `astro add`, `astro check` |
| `npm run astro -- --help` | Get help using the Astro CLI                     |

## TODO

- 画像周りの設定をする(https://docs.astro.build/ja/guides/images/)
  - Image コンポーネントがいい感じに動くかを確認
  - 背景画像もいい感じになるかも確認
- reset.scss, common.scss などプロジェクトの基本となるものを準備する
-
