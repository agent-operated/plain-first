# Check result: FAIL

<details>
<summary>日本語</summary>

依頼どおりでない点が見つかりました。対応先に、依頼されていないclientが残っています。

確認できたこと

- 終了時確認の案内は追加されています。
- 完了報告と進捗報告の違いは説明されています。

直す必要があること

- 対応先の一覧から、対象外のclientを外す必要があります。

まだ確認できていないこと

- 一覧を直した後の再検査は実行していません。

正式情報: `FAIL` / criterion `supported_clients_only` / `reports/exit-criteria.json`

</details>

One part does not match the request: the supported-target list still includes
an unrequested client.

What was confirmed

- The end-of-run check guidance was added.
- The guidance distinguishes a completion report from a progress update.

What needs to change

- Remove the out-of-scope client from the supported-target list.

What remains unchecked

- The checks have not been rerun after that correction.

Formal information

- Outcome: `FAIL`
- Failed criterion: `supported_clients_only`
- Detailed evidence: `reports/exit-criteria.json`

This result identifies a required correction. It does not claim the correction
has already been made.
