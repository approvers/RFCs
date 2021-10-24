[RFCs](https://github.com/approvers/RFCs)にCODEOWNERSを追加する

# Summary

このRFCでは、本RFCsを管理しているリポジトリ(以下、RFCsと呼称)のCODEOWNERSについて定義します。

# Motivation

現在(2021/10/23)、RFCsではGitHubのBranch Protection機能を用いてPRのMergeに3人のApproveを必要としています。

しかしGitHubのApprovers Organizationには現在50名程のメンバーが属しており、その誰しもがRFCsのPRのレビューが可能となっております。
これは限界開発鯖の比較的モデレータに近い人(以下、モデレータと呼称)がPRをレビューしないままPRをMergeすることが可能ということです。

これでは誰かが結託すれば容易に新たなRFCを追加することが可能で、問題があると考えます。

そこでGitHubのCODEROWERS機能を用いて**必ず**PRをレビューしなければいけない人を決め、モデレータが知らない間にPRがMergeされてしまうことを回避することを提案します。

# Guild-level explanation

このRFCを有効にすることによって、以降のRFCsのPRのMergeにはいずれかのモデレータのApproveが必須となります。

# Reference-level explanation

以下の手順でRFCsにCODEOWNERSを追加します。

まず、Approvers Organizationに`moderator`というTeamを作成します。
`moderator`には次のDicordのロールが付与されている人を参加させます。

- 全知全能の神
- 限界治安部隊

次にRFCsのSettings→Manage accessから`moderator`をMaintainとして追加します。

RFCsに`CODEOWNERS`ファイルを作成します。ファイルの内容は次の通りです。

```CODEOWNERS
* @approvers/moderator
```

最後にSettings→Branches→Branch Protectionから"Require review from Code Owners"にチェックを入れます。

# Future possibilities

この変更によってRFCsのPRがMergeされにくくなる恐れがあります。
しかしモデレータは比較的アクティブな人間が多い為深刻な影響はないと考えています。
