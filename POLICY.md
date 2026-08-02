# Plain First Policy

<details>
<summary>日本語</summary>

状態: 初期policy

Plain Firstは、機械やagentが人間へ見せる出力に適用します。domainの事実、結果、承認権限、
機械可読contractは定義しません。出力の意味は、各domainの規則が決めます。

## 必須の品質

1. **人間に関係ある事実から書く。** 最初に、依頼に対して何が変わったか、何が分かったか、
   どの状態が重要かを書きます。内部手順、command名、件数を主役にしません。
2. **確認できたことを書く。** 内部検査の名前だけではなく、依頼や判断に対応する事実として
   書きます。
3. **確認できなかったことを隠さない。** 実行できなかった確認、対象外、人による確認が必要な
   事項を書きます。証拠がない状態を、確認済みに見せてはいけません。
4. **人間に残る判断を見えるようにする。** 次に何を判断または確認する必要があるかを伝えます。
   元のsystemにない承認権限を勝手に持ちません。
5. **正式情報を残す。** `PASS`、`FAIL`、`UNAVAILABLE`、path、identifier、version、digestなど、
   重要な正式情報を参照できる状態に保ちます。平易な説明を加えても、正式情報を消したり
   別物へ置き換えたりしません。
6. **詳細を段階的に見せる。** 通常表示では判断に必要な内容を先に出します。技術的な証拠と
   完全な詳細は残しますが、通常表示へ全部ぶちまけません。
7. **専門用語だけで説明を終わらせない。** 正式用語が必要な場合は、人間に関係する意味へ
   つなげて説明します。
8. **証拠より強く言わない。** 元の結果が支えられる範囲を越えて断言または示唆しません。
   通った検査は未検査の挙動を証明しません。実行不能は成功ではありません。記録した判断は
   実装結果ではありません。

## 表示する順序

通常表示では、該当する項目を次の順で見つけやすくします。

1. いま人間に関係すること
2. 確認できたこと
3. 確認できなかったこと、または人による確認が必要なこと
4. 人間が次に判断または実行すること
5. 正式な結果と詳しい証拠の場所

これは情報の順序です。固定rendererや定型文ではありません。各projectはdomainと媒体に合う
段落、list、table、UIを使えます。

## Domainとの境界

Plain Firstは、`PASS`、decision record、instruction routingの状態を同じ意味にしません。
共通化するのは、人間向けの見せ方だけです。

出力元のdomainが、次を所有します。

- 事実と結果の意味
- 正本と証拠
- 評価した範囲と評価していない範囲
- 結果を承認または受理できる人
- 機械可読schemaと正式identifier

Plain Firstは受入判断をせず、元の結果にない証拠を足しません。

</details>

Status: initial policy

Plain First applies to output that a machine or agent presents to a person. It
does not define domain facts, outcomes, approval authority, or machine-readable
contracts. Domain rules remain authoritative for what the output means.

## Required qualities

1. **Lead with human-relevant facts.** The opening must say what changed, what
   was found, or what state matters to the person's request. Internal steps,
   command names, and item counts must not be the main message.
2. **State what was confirmed.** Describe confirmed facts in terms of the
   person's request or decision, not only in terms of internal checks.
3. **Expose what was not confirmed.** Say what could not be checked, was outside
   scope, or still needs human review. Absence of evidence must not look like a
   successful check.
4. **Make the remaining human judgment visible.** Tell the person what they
   still need to decide or inspect. Do not grant approval that the source system
   has no authority to grant.
5. **Preserve exact information.** Material formal outcomes and references such
   as `PASS`, `FAIL`, `UNAVAILABLE`, paths, identifiers, versions, and digests
   must remain available. Plain wording may explain them; it must not erase or
   silently replace them.
6. **Use progressive disclosure.** Show the decision-useful reading first. Keep
   technical evidence and full details available without dumping all of them
   into the normal display.
7. **Do not stop at jargon.** When a formal term is necessary, connect it to the
   consequence a person needs to understand.
8. **Respect the evidence ceiling.** Never state or imply a claim stronger than
   the underlying result supports. A passed check is not proof of unchecked
   behavior. An unavailable check is not a pass. A recorded decision is not an
   implementation result.

## Presentation order

A normal presentation should make these answers easy to find, in this order
when they apply:

1. What matters to the person now?
2. What was confirmed?
3. What was not confirmed or still needs human review?
4. What must the person decide or do next?
5. Where are the formal result and detailed evidence?

This is an information order, not a mandatory renderer or fixed prose template.
Projects may use paragraphs, lists, tables, or interfaces appropriate to their
domain and medium.

## Domain boundary

Plain First does not make `PASS`, a decision record, and instruction-routing
state interchangeable. It only governs their human-facing presentation.

The producing domain owns:

- the meaning of its facts and outcomes;
- the source of truth and evidence;
- what was and was not evaluated;
- who may approve or accept the result;
- its machine-readable schema and exact identifiers.

Plain First owns no acceptance decision and supplies no additional evidence.
