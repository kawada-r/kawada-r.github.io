---
layout: page
title: "git memo"
permalink: /docs/git-memo
---

# ソフトウェア工学2024

## ソフトウェアライフサイクル
ソフトウェアライフサイクルとは、ソフトウェア開発を行うためのプロセスである。相手のニーズを確認した後、以下の流れを行う。

### 計画
要求を形にするための企画・計画を行う。

### 要件定義
システムの目的や概要、開発スケジュールなどを明確に示す。

### ソフトウェア開発・運用
設計および製作、テストとデバッグを行った後に実稼働する。稼働後、データを活用した保守運用も行う。

## ソフトウェア分析
ソフトウェアを分析する上では、様々な観点がある。

### QCD
Quality(品質)・Cost(コスト)・Delivery(納期)の略であり、ソフトウェアの目的によってどれを優先するかが変わる。
例として、緊急時に確実に動作しなければならないものは品質優先、公共事業など使える予算が限られているものはコスト優先、日程が決まっているイベントに使うものなどは納期優先といった考え方がある。

### ソフトウェア評価
ソフトウェアは以下の基準に基づき評価することができる。
1.ステップ数
2.オブジェクト容量
3.ファンクションポイント法による数値化
4.使い勝手

ファンクションポイント法は入出力のしやすさなどを数値化して評価するものである。

## 開発手法
ソフトウェアの開発手法は以下のものなどがある。

### ウォーターフォール型プロセス
進捗管理が容易だが、後になるほどリスクが大きくなるデメリットがある。

### スパイラルモデル
開発過程を小さなフェーズに分けることで、定期的にフィードバックを行うことができる。ただし、作業量が増えるリスクがある。

### 反復型開発プロセス
部分的に完成させていくことで、随時顧客の要求を反映させるプロセス。管理業務が増えてしまうデメリットがある。

### アジャイル開発プロセス
計画からテストまでのサイクルを何度も行う手法。スクラム、XPなど細かい分類がある。

どのプロセスも一長一短であり、場面によって最適な手法は異なる。

## WBS
プロジェクトを作業ごとに分解し、構成図としてならべたもの。作業を明確化でき、自分が何をするかをはっきりさせられる。
作業をいくつかのフェーズにわけ、そのフェーズ内で行う作業、担当者、日数などを定義することでプロジェクトを進行させる。

## コーディングの注意点
コーディングをする時は、以下の事に注意しなければならない。

・1行につき、コードは79文字以内、コメントなどは72文字以内にする必要がある。
・行をまたいで書くときは、折り返された要素を縦に揃える。
・インデントはスペース4つ分にする。
・演算子の前後にはスペースを入れる。
・必要の無いスペースは入れない。
・2つの文を1行に書かない。
・行をまたぐ場合、演算子の位置も極力縦に揃える。
・関数などを命名する際は規則に沿った名前をつける。

## バージョン管理
ファイルの変更があった際、変更したユーザー、時間、内容がわかれば複数のメンバーでも共同でコード開発することが可能になる。これを管理する方法として、集中管理型と分散管理型がある。

## git
分散管理型のバージョン管理システムであり、プロジェクトをレポジトリと呼ばれるフォルダで管理する。コミットすることで変更の記録を残すことができる。また、ブランチを分けることによって並行作業も行うことができる。
以下はgitコマンドの一例である。
・git version:gitのバージョンを確認するコマンド
・git init:gitを初期化するコマンド
・git branch:ブランチを作成するコマンド
・git checkout:ブランチを切り替えるコマンド
・git merge:ブランチを統合するコマンド
・git config:コミット操作の際に使う名前やメールアドレス等を設定するコマンド
・git rm:ファイルを削除するコマンド
・git log:ログを表示するコマンド
・git diff:ファイルの差分を表示するコマンド
・git status:変更があったステータスを一覧で表示するコマンド
・git clone:レポジトリーをコピーするコマンド
・git add:ファイルをステージングエリアに追加するコマンド
・git commit:コミットを行うコマンド
・git push:ブランチの変更をGitHubにアップロードするコマンド
・git pull:レポジトリーの変更を同期するコマンド
・git request-pull:変更依頼を行うコマンド

## CI/CD
それぞれContinuous IntegrationとContinuous Deliveryの略である。CIはコード変更を共有リポジトリに統合するプロセスであり、CDはコード変更を本番環境に自動的にデプロイするプロセスである。GitHub Pagesなどに応用することが可能である。

## テスト・デバッグ
ソフトウェアを開発する際には、バグをを見つけるためにテストやデバッグを行う必要がある。

### ブラックボックステスト
内部で何が起きているかを考慮せずに行うテスト。異常な動作が起こらないかを確認する。

### ホワイトボックステスト
中身を見ながら行うテスト。ブラックボックステストと違い、プログラムを精査しながら行う。

### デバッグ
バグを取り除く作業。バグの発見前に対処するプロアクティブアプローチとバグの発生後に対処するリアクティブアプローチの2種類がある。PDCAサイクルや、OODAサイクルに基づき行う。
