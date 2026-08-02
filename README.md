# Plain First

<details>
<summary>日本語</summary>

Plain Firstは、機械やagentが持つ正確な情報を失わず、人間が最初に読んで判断できる形で
提示するための、小さく領域非依存なpolicyです。何を報告するかは各domainが決めます。
Plain Firstが決めるのは、人間へどう見せるかの品質です。

GTPは判断を、Exit Criteriaは検査結果を、Context Cascadeはinstruction routingの状態を
見せます。中身を共通化してはいけません。共通化するのは、人間に関係ある事実を先に書く、
正確な情報を残す、未確認事項を隠さない、元の結果より強く断言しない、という表示方針です。

最初の実体はpolicy、example、fixtureだけです。renderer、schema、runtime service、共有
dependencyではありません。各projectは必要な版をSkillなどの配布物へ同梱でき、runtimeで
このrepositoryへ依存しません。

</details>

> Keep machine-exact information. Put what people need to judge first.

Plain First is a small, domain-neutral policy for presenting machine and agent
output to people. It defines the quality of the human-facing presentation, not
the domain result being presented.

GitHub Task Protocol can present a decision, Exit Criteria can present check
results, and Context Cascade can present instruction-routing state. Those
outputs remain different. Plain First gives them a shared rule: lead with the
facts a person needs, preserve exact information, expose uncertainty, and never
claim more than the source result supports.

The repository starts as a source policy, examples, and fixtures. It is not a
renderer, schema, runtime service, or shared dependency. A project can vendor
the policy into a Skill or other distribution without making its runtime depend
on this repository.

- [Policy](POLICY.md)
- [Examples](examples/)
- [Good and bad fixtures](fixtures/)
- [Contributing](CONTRIBUTING.md)
- [Security](SECURITY.md)

## License

[MIT](LICENSE)
