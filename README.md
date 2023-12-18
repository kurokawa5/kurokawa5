# ykawa

<p align="left"> 
  <img alt="Top Langs" height="150px" src="https://github-readme-stats.vercel.app/api/top-langs/?username=kurokawa5&layout=compact&show_icons=true&theme=onedark" />
  <img alt="github stats" height="150px" src="https://github-readme-stats.vercel.app/api?username=kurokawa5&theme=onedark&show_icons=ture" />
</p>



```mermaid
sequenceDiagram
    participant User as 利用者
    participant Frontend as フロントエンド
    participant Backend as バックエンド
    participant Database as データベース

    User->>Frontend: アプリケーション起動
    Frontend->>Backend: フィード取得要求
    Backend->>Database: フィードデータ取得要求
    Database-->>Backend: ダミーデータ

    loop フィード取得
        Backend-->>Backend: フィードデータ処理
    end

    Backend-->>Frontend: フィードデータ
    Frontend->>Frontend: 投稿一覧画面構築

    User->>Frontend: 投稿一覧表示
    Frontend->>Frontend: 選択した投稿詳細取得要求
    Frontend->>Backend: 投稿詳細取得要求
    Backend->>Database: 投稿詳細データ取得要求
    Database-->>Backend: ダミーデータ

    loop 投稿詳細取得
        Backend-->>Backend: 投稿詳細データ処理
    end

    Backend-->>Frontend: 投稿詳細データ
    Frontend->>Frontend: 投稿詳細画面構築

    User->>Frontend: 投稿検索
    Frontend->>Frontend: 検索条件入力
    Frontend->>Backend: 投稿検索要求
    Backend->>Database: 投稿検索データ取得要求
    Database-->>Backend: ダミーデータ

    loop 投稿検索処理
        Backend-->>Backend: 投稿検索データ処理
    end

    Backend-->>Frontend: 検索結果データ
    Frontend->>Frontend: 検索結果画面構築

    User->>Frontend: フィード更新
    Frontend->>Backend: フィード更新要求
    Backend->>Database: 新しいフィードデータ取得要求
    Database-->>Backend: ダミーデータ

    loop フィード更新処理
        Backend-->>Backend: 新しいフィードデータ処理
    end

    Backend-->>Frontend: 更新されたフィードデータ
    Frontend->>Frontend: 投稿一覧画面更新

```
