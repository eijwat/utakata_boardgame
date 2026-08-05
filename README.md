# UTAKATA boardgame うたかた

**Every stone is a bubble — it will vanish. Reach the far shore before it does.**
**置いた石は、やがて泡と消える。消えるまえに、岸から岸へ。**

[English](#english) | [日本語](#日本語)

---

## English

**UTAKATA** is a two-player abstract connection game played in minutes. *Utakata* (泡沫) is an old Japanese word for foam on water — the classic image of things that never last. Your stones are bubbles: they fade, and then they are gone.

### How to play

- Take turns placing stones on the **6×6** board. Black moves first.
- **Black wins by connecting the top and bottom edges**; **White wins by connecting the left and right edges** — one unbroken chain of your own stones.
- Stones connect vertically, horizontally, and **diagonally**.

### The diagonal cut

A diagonal link is severed when **two enemy stones cross it in an × shape**. This works both ways: in a full crosscut, both diagonals are cut.

### A bubble's life

- Stones don't last. **When you place your 8th stone after one, that oldest stone vanishes** — you never have more than 8 stones on the board.
- The number on each stone counts down how many of your own moves it has left. **A stone showing "1" turns amber: it vanishes the next time you place.**
- No wall is forever. Defenses dissolve, and attacks aim for one perfect moment. The stone blocking your path will disappear — read *when*, and you are a master of foam.

### Adjudication

If neither side connects within 25 stones each, the widest reach of a single group decides the game. Ties go to White, who moved second.

### Modes

- **Play first** (Black, top–bottom) vs. CPU
- **Play second** (White, left–right) vs. CPU
- **Two players** on one device

### Design notes

The rules were tuned by self-play experiments. With orthogonal-only connections, defense was too strong (90% of games stalled into adjudication); with unrestricted diagonals, the first player won every game in 11 moves. Adding the **crosscut rule** landed exactly in between: in testing, virtually every game ends with a genuine connection, Black and White win at nearly equal rates, and an average game lasts about 26 moves — a few minutes of real thinking.

### Tech

- A single self-contained HTML file (~28KB), no build step, no libraries
- The only external resource is an optional Google Font
- Japanese/English interface with browser-language auto-detection and a live toggle
- Pure algorithmic CPU: shortest-connection-distance evaluation with immediate-win detection and verified blocking

### GitHub Pages

[Utakata Boardgame](https://eijwat.github.io/utakata_boardgame/)

---

## 日本語

**UTAKATA（うたかた）** は、数分で決着する2人用の接続ゲームです。「うたかた（泡沫）」は水面の泡のこと——長くはつづかないものの、昔ながらのたとえです。あなたの石は泡。薄れて、やがて消えます。

### 遊び方

- **6×6** の盤に、黒白交互に石を置きます。黒が先手です。
- **黒は上の辺と下の辺**、**白は左の辺と右の辺**を、自分の石のひとつながりで結べば勝ち。
- 石は縦・横・**ななめ**につながります。

### ななめの切断

ななめのつながりは、**相手の石2つが×の形で横切っている**とき切れます。これはお互いさまで、×の形では両方のななめが切れます。

### 泡の寿命

- 石には寿命があります。**自分が8手置くと、いちばん古い自分の石が消えます**（盤上の自分の石はいつも最大8個）。
- 石の数字は「あと何手（自分の手番）で消えるか」のカウントダウン。**「1」の石はオレンジ色になり、次の自分の手で消えます。**
- 永遠の壁は作れません。守りは崩れつづけ、攻めは一瞬の完成を狙います。道をふさぐ相手の石も、いつか消える——「いつ消えるか」まで読めたら、あなたはもう泡の達人です。

### 判定

どちらもつなげないまま各25手に達したら、いちばん進んだ石の群れの「到達幅」で判定します。同点なら後手の白の勝ちです。

### モード

- **先手（黒・上下）で挑む**（CPU戦）
- **後手（白・左右）で挑む**（CPU戦）
- **ふたりで遊ぶ**（1台交互）

### 設計メモ

ルールは自己対戦実験で調整しました。縦横のみの接続では守りが固すぎて9割の対局が判定にもつれ、ななめを無制限に許すと先手が11手で必勝になりました。そこに**×交差の切断ルール**を入れたところ、ほぼすべての対局が接続で決着し、黒白の勝率はほぼ互角、平均約26手——数分でしっかり考えるゲームになりました。

### 技術

- 単一の自己完結HTMLファイル（約28KB）、ビルド不要、ライブラリなし
- 外部リソースはGoogle Fonts（任意）のみ
- 日英バイリンガルUI。ブラウザ言語の自動判定と、いつでも切り替え可能なトグル
- CPUは純アルゴリズム：最短接続距離の評価＋即勝ち検出＋ブロック検証

### GitHub Pages

[Utakata Boardgame](https://eijwat.github.io/utakata_boardgame/)
