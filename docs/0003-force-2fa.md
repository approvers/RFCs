# Summary

[summary]: #summary

[限界開発鯖GitHub Organization](https://github.com/approvers/) の2要素認証必須設定を有効にしたい。

# Motivation

[motivation]: #motivation

- セキュリティ向上

# Guide-level explanation

[guide-level-explanation]: #guide-level-explanation

現在限界開発鯖のGitHub Organizationでは、Owner権限を持つメンバーは全員2FAを有効にしていますが、Member権限のメンバーについては特段2FAの設定を求めていなかったため
各自の判断に基づいています。

ここで、限界開発鯖全体のセキュリティを向上させるため、Organizationの設定に存在する `Require two-factor authentication for everyone in the † 限界開発鯖 † organization.` を有効にすることを提案します。

# Reference-level explanation

[reference-level-explanation]: #reference-level-explanation

このRFCでは[限界開発鯖のGitHub Organizationの設定](https://github.com/organizations/approvers/settings/security)にある`Require two-factor authentication for everyone in the † 限界開発鯖 † organization.`を有効にすることを提案します。

# Drawbacks

[drawbacks]: #drawbacks

この設定を有効化すると、有効化した時点で2FAの設定が済んでいないメンバーはOrganizationから強制的に退出させられます。
そのため、有効化の呼びかけに応じなかったメンバー分だけOrganizationのメンバー数が減少します。

また、2FAを設定していないアカウントはOrganizationにjoinできなくなります。そのため、新規メンバーが参加し、Organizationにinviteする際は2FAの設定を依頼する必要が発生します。

# Rationale and alternatives

[rationale-and-alternatives]: #rationale-and-alternatives

- 説明面倒くさいのでここ読んでください
  - https://docs.github.com/ja/organizations/keeping-your-organization-secure/requiring-two-factor-authentication-in-your-organization

# Prior art

[prior-art]: #prior-art

- https://viibar-engineering.hatenablog.com/entry/2020/05/20/131917
- https://qiita.com/IZUMIRU/items/e96282ab4f3183cf53a8

# Unresolved questions

[unresolved-questions]: #unresolved-questions

- [haracho](https://github.com/orgs/approvers/people/haracho)の2FAをどうするか
- 非アクティブメンバーの扱いをどうするか

# Future possibilities

[future-possibilities]: #future-possibilities

非アクティブ鯖民をばっさり切って推し進めるか、鯖民が面倒くせぇと言って頓挫するかの2択だと考えています。
この際なので推し進めたい気持ちです。
