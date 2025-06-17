# 環境構築手順（Reactハンズオン用）

このディレクトリでは、Reactハンズオンのための開発環境構築手順をまとめます。

---

## 1. 必要なソフトウェアのインストール

- Node.js（推奨バージョン: 22.x）
- npm（Node.jsに同梱）
- エディタ（VSCode推奨）

---

## 2. プロジェクトの作成

1. ターミナルを開き、作業ディレクトリに移動します。
2. 以下のコマンドでReactプロジェクトを作成します（Viteを例とします）。

```sh
npm create vite@latest my-react-pokemon -- --template react
cd my-react-pokemon
npm install
```

---

## 3. 必要なパッケージのインストール

APIリクエスト用にaxiosを利用する場合、以下を実行します。

```sh
npm install axios
```

---

## 4. 開発サーバーの起動

```sh
npm run dev
```

ブラウザで `http://localhost:5173`（Viteの場合）にアクセスし、初期画面が表示されればOKです。

---

## 5. 補足
- 他のReactプロジェクト作成方法（Create React Appなど）でもOKです。
- Windows/Macどちらでも進行可能です。 