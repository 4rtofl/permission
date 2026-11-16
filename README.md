# permission

4rtofl で使っている GitHub・Discord・Cloudflare・AWS の権限を、このリポジトリで管理します。

> 現在は設計中です。各サービスへの反映はまだ行っていません。

## 申請と承認

- 権限の変更は、このリポジトリへの Pull Request で申請します。
- 申請者以外のメンバー2人がどちらも承認すると、マージできます。`main` は Pull Request 経由でしか変更できません。
- 承認のあとに新しい変更を push すると、承認はやり直しになります。

## このリポジトリは公開されています

次のものはコミットしないでください。

- メールアドレスなどの個人情報
- AWS や Cloudflare のアカウント ID
- API トークン、鍵、パスワード

これらは GitHub Actions の Environment のシークレットに置きます。
コミットに使うメールアドレスも、GitHub の noreply アドレスにしてください。

## ブランチ保護

`main` の保護ルールは [.github/rulesets/protect-main.json](.github/rulesets/protect-main.json) に置いています。
Settings → Rules → Rulesets → New ruleset → Import a ruleset で読み込めます。
