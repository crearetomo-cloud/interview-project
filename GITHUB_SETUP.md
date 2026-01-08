# GitHub へのプッシュ手順

## ✅ 現在の状態

ローカルリポジトリは準備完了しました：
- ✅ Gitリポジトリ初期化済み
- ✅ 全ファイルコミット済み（23ファイル、1904行）

## 📋 次のステップ：GitHubにプッシュする

### 1. GitHubでリポジトリを作成

1. GitHubにログイン（https://github.com）
2. 右上の「+」→「New repository」をクリック
3. リポジトリ名を入力（例：`interview-project`）
4. **Public** または **Private** を選択
5. 「Initialize this repository with a README」は**チェックしない**（既にREADMEがあるため）
6. 「Create repository」をクリック

### 2. リモートリポジトリを追加

GitHubでリポジトリを作成したら、以下のコマンドを実行してください：

#### SSH方式（推奨）
```powershell
git remote add origin git@github.com:YOUR_USERNAME/interview-project.git
```

#### HTTPS方式
```powershell
git remote add origin https://github.com/YOUR_USERNAME/interview-project.git
```

**注意**: `YOUR_USERNAME` を実際のGitHubユーザー名に置き換えてください。

### 3. GitHubにプッシュ

```powershell
git branch -M main
git push -u origin main
```

#### 認証が必要な場合

- **SSH方式**: SSH鍵が設定されている必要があります
- **HTTPS方式**: Personal Access Token (PAT) が必要です
  - GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
  - 「Generate new token」で作成し、`repo` スコープを選択

---

## 📁 プッシュされるファイル一覧

以下のファイルがGitHubに保存されます：

- `README.md` - プロジェクト概要
- `.gitignore` - Git除外設定
- `docs/` - プロジェクトドキュメント
  - `project-overview.md`
  - `outreach/` - アウトリーチテンプレート
  - `process/` - プロセスガイド
- `playbooks/` - ベストプラクティス
  - `interview/` - インタビューガイド
  - `writing/` - ライティングガイド
- `content/interviews/_template/` - インタビューテンプレート
- `assets/` - メディアファイル用ディレクトリ

---

## 🔄 今後の更新方法

ファイルを更新したら、以下のコマンドでプッシュできます：

```powershell
git add .
git commit -m "更新内容の説明"
git push
```

---

*作成日: 2025年1月*

