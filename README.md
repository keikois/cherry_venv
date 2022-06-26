# practice_venv
- anaconda3-2021.11のVenvを作成

## 🍒チェリーピックで、特定の仮想環境のみ取得
### practice_venvを、ローカルにクローン
- git@github.com:keikois/practice_venv.gitから、clone
```
git clone git@github.com:keikois/practice_venv.git
```
直後の状態
```
* f30e587 - (HEAD -> main, origin/main, origin/HEAD) tada: 🎉 anaconda3-2021.11のVenvを作成 (5 hours ago) <keikoish>
* 9734281 - tada: 🎉 miniconda3-4.7.12のVenvを作成 (6 hours ago) <keikoish>
* 809ff58 - tada: 🎉 miniconda3-4.7.12のVenvを作成 (6 hours ago) <keikoish>
* 3f224c0 - add: ✨ venv3.10.4のバックアップvenv3.10.4−02を作成 (6 hours ago) <keikoish>
* 6176538 - up: 🆙 Python3.6.15のVenvを作成 (31 hours ago) <keikoish>
* b3e0a8f - docs: ✏️ README.mdコマンド訂正 (31 hours ago) <keikoish>
* 1380717 - up: 🆙 Python3.7.13のVenvを作成 (31 hours ago) <keikoish>
* b2599a9 - add:python3.8.13を追加 (2 days ago) <keikoish>
* e0e2002 - docs:venvを作成、アクティベート、バージョン確認 (2 days ago) <keikoish>
* 70f1be2 - add:pyenvの切り替え完了確認 (2 days ago) <keikoish>
* 63d0f36 - add:pyenvの切り替え方法追記 (2 days ago) <keikoish>
* ecf8d91 - docs:Pythonのインストール方法(Pyenv) (2 days ago) <keikoish>
* 192f9cb - add:Python3.9.12のVenvを作成 (2 days ago) <keikoish>
* 8aa5ef1 - add:Python3.10.4のVenvを作成 (2 days ago) <keikoish>
* 89c08ee - Initial commit (2 days ago) <Keikoish>
```
### 🌿ブランチの作成
- keikois/practice_venvの最初のコミット【ID :89c08ee】の部分から、🌿ブランチ(venv_ana)を作成して、venv_anaをheadにする。
```
git checkout 89c08ee -b venv_ana
```
直後の状態。89c08ee - (HEAD -> venv_ana)を確認。
```
* f30e587 - (origin/main, origin/HEAD, main) tada: 🎉 anaconda3-2021.11のVenvを作成 (5 hours ago) <keikoish>
* 9734281 - tada: 🎉 miniconda3-4.7.12のVenvを作成 (6 hours ago) <keikoish>
* 809ff58 - tada: 🎉 miniconda3-4.7.12のVenvを作成 (6 hours ago) <keikoish>
* 3f224c0 - add: ✨ venv3.10.4のバックアップvenv3.10.4−02を作成 (6 hours ago) <keikoish>
* 6176538 - up: 🆙 Python3.6.15のVenvを作成 (31 hours ago) <keikoish>
* b3e0a8f - docs: ✏️ README.mdコマンド訂正 (31 hours ago) <keikoish>
* 1380717 - up: 🆙 Python3.7.13のVenvを作成 (31 hours ago) <keikoish>
* b2599a9 - add:python3.8.13を追加 (2 days ago) <keikoish>
* e0e2002 - docs:venvを作成、アクティベート、バージョン確認 (2 days ago) <keikoish>
* 70f1be2 - add:pyenvの切り替え完了確認 (2 days ago) <keikoish>
* 63d0f36 - add:pyenvの切り替え方法追記 (2 days ago) <keikoish>
* ecf8d91 - docs:Pythonのインストール方法(Pyenv) (2 days ago) <keikoish>
* 192f9cb - add:Python3.9.12のVenvを作成 (2 days ago) <keikoish>
* 8aa5ef1 - add:Python3.10.4のVenvを作成 (2 days ago) <keikoish>
* 89c08ee - (HEAD -> venv_ana) Initial commit (2 days ago) <Keikoish>
```
### 🍒cherry-pick
- 🍒cherry-pickで、欲しいcomitt(仮想環境)の部分だけ、取ってくる。
```
git cherry-pick f30e587
```

直後の状態。
READMEがコンフリクト（重複）を起こしている。
状況に合わせて、適宜修正する。
```
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
error: could not apply f30e587... tada: 🎉 anaconda3-2021.11のVenvを作成
hint: After resolving the conflicts, mark them with
hint: "git add/rm <pathspec>", then run
hint: "git cherry-pick --continue".
hint: You can instead skip this commit with "git cherry-pick --skip".
hint: To abort and get back to the state before "git cherry-pick",
hint: run "git cherry-pick --abort".
```
🌿ブランチの状態を確認。
```
  main
* venv_ana
  remotes/origin/HEAD -> origin/main
  remotes/origin/main
```
リモートリポジトリを新しく作成するため、一旦remoteの登録を解除する。
```
git remote rm origin
```
直後の状態。remoteがなくなっていることを確認。
```
* 9734281 - tada: 🎉 miniconda3-4.7.12のVenvを作成 (6 hours ago) <keikoish>
* 809ff58 - tada: 🎉 miniconda3-4.7.12のVenvを作成 (6 hours ago) <keikoish>
* 3f224c0 - add: ✨ venv3.10.4のバックアップvenv3.10.4−02を作成 (6 hours ago) <keikoish>
* 6176538 - up: 🆙 Python3.6.15のVenvを作成 (31 hours ago) <keikoish>
* b3e0a8f - docs: ✏️ README.mdコマンド訂正 (31 hours ago) <keikoish>
* 1380717 - up: 🆙 Python3.7.13のVenvを作成 (32 hours ago) <keikoish>
* b2599a9 - add:python3.8.13を追加 (2 days ago) <keikoish>
* e0e2002 - docs:venvを作成、アクティベート、バージョン確認 (2 days ago) <keikoish>
* 70f1be2 - add:pyenvの切り替え完了確認 (2 days ago) <keikoish>
* 63d0f36 - add:pyenvの切り替え方法追記 (2 days ago) <keikoish>
* ecf8d91 - docs:Pythonのインストール方法(Pyenv) (2 days ago) <keikoish>
* 192f9cb - add:Python3.9.12のVenvを作成 (2 days ago) <keikoish>
* 8aa5ef1 - add:Python3.10.4のVenvを作成 (2 days ago) <keikoish>
* 89c08ee - (HEAD -> venv_ana) Initial commit (2 days ago) <Keikoish>
[ishiikeiko@ishiikeikonoMacBook-Pro] ~/develop-python/clone/ana/practice_venv

```
🌿ブランチの状態を確認。
```
git branch -a 
```
```
  main
* venv_ana
```
🌿メインブランチは不要なので、削除する。
mergeしていないときに、🌿ブランチを削除するときのコマンドは下記。
```
git branch -D main
```
実行結果
```
* venv_ana
```
🌿mainブランチが削除されていることを確認。
ブランチの名前をvenv_anaからmainに変更する。
```
git branch -m main
```
ここまでの変更をaddしてcommitする。
```
git add .
```
```
git commit
```
昔のコミットメッセージのままだと、🍒cherry-pickしたことが、わかりにくいため、
昔）tada: 🎉 anaconda3-2021.11のVenvを作成
今）[main f835aaf] tada: 🎉 (🍒:f30e587)anaconda3-2021.11のVenvを作成
と記載する。

[main f835aaf] 👉現在のブランチ名とcommit ID
(🍒:f30e587)👉cherry-pickしたIDを記載

何を元に、どこの🌿ブランチに🍒cherry-pickしたのか、分かるように記載する。

## 新しいリモートリポジトリにpushする
ここまでの状態
```
* f835aaf - (HEAD -> main) tada: 🎉 (🍒:f30e587)anaconda3-2021.11のVenvを作成 (2 minutes ago) <keikoish>
* 89c08ee - Initial commit (2 days ago) <Keikoish>
```
githubで、新しいリポジトリ(名前:cherry_venv)をHPで作成してから、リモートリポジトリをgitに登録する。
```
git remote add origin git@github.com:keikois/cherry_venv.git
```
gitを登録したgithubのリポジトリにpushする。
```
git push --set-upstream origin main
```
ログを見ると
```
* f835aaf - (HEAD -> main, origin/main) tada: 🎉 (🍒:f30e587)anaconda3-2021.11のVenvを作成 (11 minutes ago) <keikoish>
* 89c08ee - Initial commit (2 days ago) <Keikoish>
```
githubで、pushした内容が反映されている事を、確認してください。