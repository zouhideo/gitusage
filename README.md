# gitusage
Usage of GitHub

■GitHubにおけるGitリポジトリの使い方自体は一般的なGitと同じです。

■GitHubの根幹はPullRequest仕組み、これを利用し分散開発を効率的に進めることができる。

■PullRequest Workflow
A-元GitHub Upstream、B-GitHub自前リポジトリ、C-ローカルリポジトリ作業場所
1. Bでログイン
2. GitHubでFeedback対象のリポジトリAを探し、Forkする。すると自前のGitHubにBリポジトリは複製される
3. Aではなく、Bを対象に行う(自前のGitHubに作成し編集するか、他のリポジトリにCloneし編集するか)
   git clone https://github.com/<B Account>/<複製リポジトリ名>
4. 編集時、masterではなく、作業用Branchを作成する。git checkout -b some-branch
5. 編集を行い、終わったら、git add,commitで編集内容をGitに反映する。
6. GitHub-Bにpushし、Bリポジトリにsome-branchも作成される git push origin some-branch
7. GitHub-BでPullRequestを作成し送信する
8. Requestを受け取ったAは内容を確認し、レビューやマージを行います。
以上
