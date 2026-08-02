# Contributing

<details>
<summary>日本語</summary>

Plain Firstは小さく、domainに依存しない状態を保ちます。変更では、解決する人間向け表示の
問題、出力元domainの正式情報をどう残すか、共有runtime dependencyを増やさないことを示して
ください。

pull requestには、繰り返し起きる表示上の失敗、変更するpolicyまたはexample、残る正式情報、
変更後も断言できないことを書きます。policy変更で機械的に区別できる性質を増やす場合は、
good fixtureとbad fixtureも更新します。

</details>

Plain First stays small and domain-neutral. A change should identify the human
presentation problem it solves, preserve the producing domain's exact result,
and avoid introducing a shared runtime dependency.

Use a pull request. Explain:

- the recurring presentation failure;
- the policy text or example that changes;
- what exact information remains available;
- what the revised wording still cannot claim.

Examples may use domain-specific facts, but policy requirements must not redefine
the meaning of a domain outcome. Add or update a good and bad fixture when a
policy change introduces a testable distinction.
