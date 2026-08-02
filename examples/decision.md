# Decision presentation

<details>
<summary>日本語</summary>

配布するpolicyは各Skillへ同梱し、runtimeでは共有repositoryへ依存しない方針に決まりました。

判断したこと

- Plain Firstは小さなsource部品として管理します。
- 各projectは、採用する版を自分の配布物へ同梱します。
- 共通renderer、registry、network serviceは初期範囲に含めません。

この判断で残ること

- どの版を各projectが採用したかは、各project側で管理する必要があります。
- fixture checkerが必要かは、実例が増えてから判断します。

正式情報: decision `DR-0001` / status `accepted` /
`gtp/decisions/DR-0001-vendor-policy-source.md`

</details>

The policy will be vendored into each Skill distribution instead of becoming a
shared runtime dependency.

What was decided

- Plain First remains a small source component.
- Each project vendors the policy version it adopts into its own distribution.
- A shared renderer, registry, and network service are outside the initial scope.

What remains

- Each project must record which Plain First version it adopted.
- The need for a fixture checker will be judged after more examples exist.

Formal information

- Decision ID: `DR-0001`
- Status: `accepted`
- Record: `gtp/decisions/DR-0001-vendor-policy-source.md`

This is a design decision record. It does not establish that every adopting
project has implemented the decision.
