# Viral Video Remake Skill

[English](./README.md) | [简体中文](./README.zh-CN.md) | 日本語

> 👉 こちらもどうぞ [AI Storyboard Generator Skill](https://github.com/beatra-ai/ai-storyboard-generator-skill)

伸びたショート動画をフック・展開・CTA に分解し、その構成を自分の題材で組み直して、ショットリスト、ビートフレーム、ナレーション、縦型クリップまたは分割素材として納品。Claude Code、Cursor、Codex、Windsurf、Cline、OpenClaw のどれからでもそのまま使えます。

> [!IMPORTANT]
> 生成には [Beatra](https://beatra.ai) アカウントが必要で、クレジットを消費します。スキル自体のインストールは無料です。

| 項目 | 内容 |
| --- | --- |
| **できること** | リンクを貼るか手元の素材を渡すだけ。伸びたショート動画を冒頭フック・本編・締めへ分解し、その構成を自分のテーマに移して、絵コンテ・カット画像・ナレーションまで作ります。カット数が少なく尺がモデルの単発生成上限内に収まれば冒頭カットを動かした縦型動画一本、カットが多い、または尺が上限を超える場合はタイムコード付き編集リストを添えた分割済み素材でお渡しします。 |
| **モデル** | Qwen Image 2.0 Fast、Qwen Image 3.0、Qwen Image 3.0 Pro、GPT Image 2.5 Flare、GPT Image 2.5 Sunburst、GPT Image 2、Wan Image 2.7 Fast、Qwen Image 2.0 Pro、Wan Image 2.7 Pro、MiniMax Image 01 Live、MiniMax Voice Clone、MiniMax Speech 2.8 HD、MiniMax Speech 2.8 Turbo、MiniMax M3、Wan 2.7、Wan 3.0 Video、MiniMax H3、Seedance 2.0 Mini、HappyHorse 1.1、Seedance 2.0 Fast、Seedance 2.0、Wan 3.0 Video Prime、Seedance 2.5 |
| **動作要件** | Python 3.10 以上と、`SKILL.md` を読み込めるエージェント |
| **費用** | インストールは無料。生成のたびに Beatra アカウントのクレジットを消費しますが、課金されるのは、その生成を明示的に依頼したとき、または確認カードを承認したときだけです。 |
| **対応エージェント** | Claude Code、Cursor、Codex、Windsurf、Cline、OpenClaw |

<p align="center"><img src="assets/hero.webp" width="800" alt="架空の折りたたみデスクランプ Brightfold のために、「悩みから入る」ショート動画の仮想の構成を作り直した 9:16 のビートフレーム 4 枚（Hook、Demo、Benefits、CTA）。Beatra AI で生成。"></p>

*架空の折りたたみデスクランプ Brightfold のために、「悩みから入る」ショート動画の仮想の構成を作り直した 9:16 のビートフレーム 4 枚（Hook、Demo、Benefits、CTA）。Beatra AI で生成。*

| Skill | Entry point | Version |
| --- | --- | --- |
| [`viral-video-teardown-remake`](skills/viral-video-teardown-remake) | [SKILL.md](skills/viral-video-teardown-remake/SKILL.md) | 0.4.0 |

このリポジトリは [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/tree/main/skills/viral-video-teardown-remake) から自動的に公開されています。問題の報告はそちらへお願いします。

## インストール

[`skills`](https://skills.sh) CLI を使う場合：

```bash
npx skills add beatra-ai/viral-video-remake-skill
```

GitHub CLI を使う場合：

```bash
gh skill install beatra-ai/viral-video-remake-skill viral-video-teardown-remake
```

または、このリポジトリをクローンして `skills/viral-video-teardown-remake` を次の場所にコピーします：Claude Code は `~/.claude/skills/`、Cursor は `~/.cursor/skills/`、Codex は `~/.agents/skills/`、Windsurf は `~/.codeium/windsurf/skills/`、Cline は `~/.cline/skills/`、OpenClaw は `~/.openclaw/skills/`。

または、次の文をエージェントに貼り付けてください：

```text
https://github.com/beatra-ai/viral-video-remake-skill から viral-video-teardown-remake スキル（フォルダ skills/viral-video-teardown-remake）をインストールし、その SKILL.md に従って私の Beatra アカウントに接続してください。
```

## 作例

<p align="center"><img src="assets/preview-1.webp" width="800" alt="Hook のビートフレームから動かした 6 秒の Brightfold リメイククリップの無音ループプレビュー。Beatra AI で生成。"></p>

[▶ フル動画を見る（MP4）](assets/full-1.mp4)

*架空のランプ Brightfold の 6 秒の縦型リメイククリップ：Hook のフレームを動かし、フック・デモ・利点・CTA を 4 行のナレーションで。Beatra AI で生成。*

エージェントへの依頼例：

```text
このショート動画（リンクは ./reference.txt）をフック、ビート、CTA に分解して、その構成を ./brightfold.jpg の折りたたみデスクランプ Brightfold 用に組み直して：ショットリスト、ビートフレーム、ナレーション、縦型クリップまで。
```

プロンプト：

```text
Evening on a cramped desk. The folded sage-green desk lamp in the foreground slowly unfolds on its own: its single flat arm rises from the round base, the long flat light bar lifts open at the small brass hinge, and the light bar switches on with a warm white glow that brightens the desk. Slow gentle camera push-in toward the lamp. The laptop, papers, mug and plant stay still. Smooth, realistic product-video motion.
```

## 技術仕様と出力上限

2026-10-18 時点。最新の一覧：https://docs.beatra.ai/ja/docs/models

- **アップロード** — 1 ファイルあたり最大 100 MB。下記の各モデルの入力制限も適用されます
- **テキストから画像** — 10 モデル（Qwen Image 2.0 Fast、Qwen Image 3.0、Qwen Image 3.0 Pro、GPT Image 2.5 Flare、GPT Image 2.5 Sunburst、GPT Image 2、Wan Image 2.7 Fast、Qwen Image 2.0 Pro、Wan Image 2.7 Pro、MiniMax Image 01 Live）／PNG／1 リクエストあたり最大 4 枚／キャンバス最大 16.8 MP
  - 16.8 MP（4K ティア）：Wan Image 2.7 Pro（1 リクエストあたり最大 4 枚）／GPT Image 2.5 Flare、GPT Image 2.5 Sunburst、GPT Image 2（1 リクエストにつき 1 枚）
- **ボイスクローン** — 1 モデル（MiniMax Voice Clone）／サンプル 10〜300 秒、最大 20 MB／本人の同意確認が必要
- **音声合成** — 2 モデル（MiniMax Speech 2.8 HD、MiniMax Speech 2.8 Turbo）／FLAC、MP3、OPUS、PCM、WAV／40 言語／サンプルレート 8、16、22.05、24、32、44.1 kHz／1 リクエストあたり最大 50000 文字
  - 言語（ISO 639 コード）：zh, yue, en, es, fr, ru, de, pt, ar, it, ja, ko, id, vi, tr, nl, uk, th, pl, ro, el, cs, fi, hi, bg, da, he, ms, fa, sk, sv, hr, fil, hu, no, sl, ca, nn, ta, af
- **動画理解** — 1 モデル（MiniMax M3）／1 リクエストにつき 1 ファイル／各最大 50 MB／最長 360 秒／1 fps でサンプリング
- **画像から動画** — 9 モデル（Wan 2.7、Wan 3.0 Video、MiniMax H3、Seedance 2.0 Mini、HappyHorse 1.1、Seedance 2.0 Fast、Seedance 2.0、Wan 3.0 Video Prime、Seedance 2.5）／480p〜4K／2〜30 秒／アスペクト比 16:9、1:1、21:9、3:4、4:3、9:16／MOV、MP4
  - 4K：Seedance 2.0、最長 15 秒
  - 30 秒：Wan 3.0 Video、Wan 3.0 Video Prime、Seedance 2.5、最高 1080p
  - ネイティブ音声：Wan 2.7、MiniMax H3
- **最初と最後のフレームから動画** — 8 モデル（Wan 2.7、Wan 3.0 Video、MiniMax H3、Seedance 2.0 Mini、Seedance 2.0 Fast、Seedance 2.0、Wan 3.0 Video Prime、Seedance 2.5）／480p〜4K／2〜30 秒／アスペクト比 16:9、1:1、21:9、3:4、4:3、9:16／MOV、MP4
  - 4K：Seedance 2.0、最長 15 秒
  - 30 秒：Wan 3.0 Video、Wan 3.0 Video Prime、Seedance 2.5、最高 1080p
  - ネイティブ音声：Wan 2.7、MiniMax H3
- **動画の延長** — 7 モデル（Wan 2.7、Wan 3.0 Video、Seedance 2.0 Mini、Seedance 2.0 Fast、Seedance 2.0、Wan 3.0 Video Prime、Seedance 2.5）／480p〜4K／2〜30 秒／アスペクト比 16:9、1:1、21:9、3:4、4:3、9:16／MOV、MP4
  - 4K：Seedance 2.0、最長 15 秒
  - 30 秒：Wan 3.0 Video、Wan 3.0 Video Prime、Seedance 2.5、最高 1080p
  - ネイティブ音声：Wan 2.7
- **参照素材から動画** — 9 モデル（Wan 2.7、MiniMax H3、Wan 3.0 Video、HappyHorse 1.1、Seedance 2.0 Mini、Seedance 2.0 Fast、Seedance 2.0、Wan 3.0 Video Prime、Seedance 2.5）／480p〜4K／2〜30 秒／アスペクト比 16:9、1:1、3:4、4:3、9:16、21:9、4:5、5:4、9:21／MOV、MP4
  - 4K：Seedance 2.0、最長 15 秒
  - 30 秒：Wan 3.0 Video、Wan 3.0 Video Prime、Seedance 2.5、最高 1080p
  - ネイティブ音声：Wan 2.7、MiniMax H3

## 得られるもの

- **表面ではなく構成を読む** — 秒単位でフック・本編の各展開・締めへ切り分け、六つの構成パターンのどれに当たるかを判定します。
- **何が効いたのかを分ける** — 構造・内容・演出を層に分けて評価し、あなたが持ち帰るべき層をはっきりさせます。
- **分析で終わらず、撮れる素材まで** — 映像と語りを分けた絵コンテ表、静止画で納品するカット画像、ナレーション音声、そして冒頭カットを動かした縦型動画一本——カットが多い、または尺が単発生成の上限を超える場合は、字幕と編集リストを添えた分割済み素材でお渡しします。

## 活用シーン

- **競合が伸ばした一本を読む** — なぜ伸びたのかを掴み、同じ構成であなたの版を作ります。
- **参考動画を再現できる型にする** — 保存してある一本を、別のテーマにも使える形として取り出します。
- **ベンチマークを自社ブランドで作り直す** — 実績のあるテンポと展開順を保ちつつ、主張はすべて自社の事実に置き換えます。

## よくある質問

### 何を用意すればよいですか。

参考となるショート動画一本と、あなたが作りたいテーマを一言。参考は投稿のリンク、動画ファイル、要所のスクリーンショット、貼り付けたテキスト、展開の口頭説明のいずれでも構いません。

### 分解では何が分かりますか。

秒単位の展開表、当てはまる構成パターン、寄与度順に並べた要因分析、そしてフックの強さ・情報密度・テンポ・被写体の見せ方・感情曲線・行動喚起の六指標評価です。最後に、あなたのリメイクが上回れる弱点も示します。

### 最終的に何が手に入りますか。

映像と語りを別欄に書き分けた絵コンテ表、指定した展開のカット画像、選んだ声のナレーション音声までは共通です。カット数が少なく尺が単発生成の上限内に収まる場合は、冒頭カットを動かしナレーション全編を載せた9:16の縦型動画一本になり、ほかの展開のカット画像は静止画としてお渡しするので、ご自身の編集にそのままお使いいただけます。カットが多い、または尺が上限を超える場合は、展開ごとの分割素材、同じナレーション音声トラック、字幕、タイムコード付き編集リストをお渡しするので、ご自身の編集ソフトで組み立てられます。

## 更新とセキュリティ

2026 年 10 月のリリース以降、このスキルに自動更新機能はありません。インストールしたファイルだけを実行し、
自動的に置き換えることはありません。更新はインストールに使ったツール（`npx skills update viral-video-teardown-remake` または
`gh skill update viral-video-teardown-remake`）で行ってください。詳細はスキル内の `references/updates-and-security.md` を参照してください。

## ライセンス

[MIT-0](LICENSE)：商用を含め、自由に使用・改変・再配布できます。クレジット表記は不要です。ClawHub 上のこれらのスキルと同じ条件です。

## リンク

- ウェブサイト — https://beatra.ai
- ドキュメント — https://docs.beatra.ai
- コンソール — https://console.beatra.ai
- AI エージェント向け — https://beatra.ai/llms.txt（インデックス）· https://beatra.ai/llms-full.txt（全スキルを 1 ファイルに）
