# はじめに

本レポジトリは、フロント開発を効率化してくれるツール（Bit）を紹介するハンズオンです。

複数のReactアプリとStoryBookを用いて、Bitを利用した開発プロセスを簡単に紹介します。

# 事前準備

以下の流れで、`bit cli`とreactアプリを2つ作成している状態から始めます。

[事前準備](doc/Preparation.md)

# ハンズオンの流れ

1. 類似ツール（コンポーネントカタログツール）のStoryBookの紹介
2. Bitを利用した開発プロセスのデモ（クロスレポジトリ）

# ストーリーブック初期化

```
$ npx sb init
```

# コンポーネント追加

* 前準備（ログインなど）

```
$ cd app1
$ bit init
$ bit login
```

* 対象に追加

```
$ bit add src/utils/*
$ bit status
```

* コンパイラ追加

```
$ bit import bit.envs/compilers/react@1.0.21 --compiler
```

* ビルド

```
$ bit build
```

* タグ付与 & push

```
$ bit tag --all 1.0.0
$ bit export thirosue.react-hands-on
```

# 使い方

* Bit レポジトリを取得対象に追加

```
$ npm config set @bit:registry https://node.bit.dev
```

* 普通に`yarn add`

# おまけ

* テストも書ける

https://bit.dev/thirosue/react-tutorial/submit

* 料金

かなり高め

https://bit.dev/pricing

Proプランで5人開発で、1万円強

# 終わりに

プライベートレポジトリとStoryBookのいいとこどりしたSaas。

Gitライクに利用できるのも、良い感じ。

マイクロサービス開発、複数チームでの開発、マルチテナントのサービス開発、会社の資源の共有などに役立ちそう。

開発プロセスに組み込むことで、
コンポーネント設計（IF設計、再利用性やテスト容易性）も意識することになり、最終的な生産性向上も見込めるかも。
