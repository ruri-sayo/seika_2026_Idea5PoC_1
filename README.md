# Babylon.js Parametric Creature PoC

Babylon.jsで作った、パラメータ操作による3D生物変形の技術検証用PoCです。

## 概要

- HTML / CSS / JavaScriptのみで構成
- Babylon.jsはCDNから読み込み
- npm、ビルドツール、バックエンド、データベースは不要
- Box、Sphere、CylinderなどのBabylon.js標準Primitiveだけで生物を生成
- スライダー操作時は既存Meshの`position`と`scaling`を更新
- ArcRotateCameraでマウスドラッグによる視点回転が可能

## パラメータ

| Parameter | 変化する部位 |
| --- | --- |
| A | 4本の脚の長さ |
| B | 胴体の大きさ |
| C | 頭の大きさ |
| D | 4本の脚の太さ |
| E | 尻尾の長さ |
| F | 頭の形。`0`で丸、`1`で三角 |

## ローカルで起動

このディレクトリで簡易HTTPサーバーを起動します。

```bash
cd Seika_PoC_idea5
python3 -m http.server 8000
```

ブラウザで http://localhost:8000/ を開いてください。

## GitHub Pagesで公開

1. このディレクトリをGitHubリポジトリにpushします。
2. GitHubリポジトリの **Settings → Pages** を開きます。
3. **Source** で **Deploy from a branch** を選びます。
4. 公開するブランチに`main`、フォルダに`/(root)`を指定して保存します。
5. 数分後に表示されるPagesのURLへアクセスします。

Babylon.jsをCDNから読み込むため、公開ページの利用にはインターネット接続が必要です。

## ファイル構成

```text
Seika_PoC_idea5/
├── index.html
└── README.md
```
