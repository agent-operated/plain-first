# Check result: UNAVAILABLE

<details>
<summary>日本語</summary>

確認できなかった点があります。必要な検査commandを起動できなかったため、依頼内容が
満たされたとは判断できません。

確認できたこと

- 対象revisionは特定できました。
- 検査設定は見つかりました。

確認できなかったこと

- 文書内の対応先が依頼された二つだけかは確認できていません。
- 完了報告の説明が更新されたかは確認できていません。

次に必要なこと

- 検査commandを利用できる環境で再実行するか、対象箇所を人が確認してください。

正式情報: `UNAVAILABLE` / reason `spawn_failed` / `reports/exit-criteria.json`

</details>

Some requested facts could not be checked. The required checker did not start,
so this result cannot establish that the request was satisfied.

What was confirmed

- The target revision was identified.
- The check configuration was found.

What was not confirmed

- The supported-target list was not checked for the two requested clients.
- The revised completion-report explanation was not checked.

What needs to happen next

- Rerun in an environment where the checker can start, or have a person inspect
  the affected sections.

Formal information

- Outcome: `UNAVAILABLE`
- Reason: `spawn_failed`
- Detailed evidence: `reports/exit-criteria.json`

`UNAVAILABLE` must not be presented as a pass.
