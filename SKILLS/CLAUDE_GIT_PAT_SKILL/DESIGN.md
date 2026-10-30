PAT は HTTPS 形式の URL で使用します。対象リポジトリの遠隔 URL が HTTPS になっているか確認します。

Bash
git remote -v
出力結果が [https://github.com/ユーザー名/リポジトリ名.git](https://github.com/ユーザー名/リポジトリ名.git) になっていればOKです。

もし git@github.com:...（SSH形式）になっている場合は、以下で HTTPS に変更します：

Bash
git remote set-url origin https://github.com/ユーザー名/リポジトリ名.git
Step 3: git push 時に PAT を入力する
git push を実行すると、ユーザー名とパスワードを求められます。

Bash
git push origin main
Username for '[https://github.com](https://github.com)':
👉 自分の GitHub のユーザー名（または登録メールアドレス）を入力して Enter。

Password for 'https://...':
👉 Step 1 で取得した PAT（ghp_...） を貼り付けて Enter。

(画面には文字が表示されませんが、正しく入力されています)

認証が成功すると、push が完了します。