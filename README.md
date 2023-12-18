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

    User ->> Frontend: ページロード
    activate Frontend

    Frontend ->> Backend: フィード取得要求
    activate Backend

    Backend ->> Database: フィード取得クエリ（ダミーデータ）
    activate Database

    Database -->> Backend: ダミーデータ
    deactivate Database

    Backend -->> Frontend: フィードデータ
    deactivate Backend

    Frontend ->> Frontend: 投稿一覧画面構築

    User ->> Frontend: 投稿一覧表示
    activate Frontend

    Frontend -->> Frontend: 投稿一覧表示

    User ->> Frontend: 投稿選択
    activate Frontend

    Frontend ->> Backend: 投稿詳細取得要求
    activate Backend

    Backend -->> Frontend: 投稿詳細データ
    deactivate Backend

    Frontend ->> Frontend: 投稿詳細表示

    User ->> Frontend: 投稿検索
    activate Frontend

    Frontend ->> Backend: 投稿検索要求
    activate Backend

    Backend -->> Frontend: 検索結果
    deactivate Backend

    Frontend -->> Frontend: 検索結果表示

    User ->> Frontend: フィード手動更新
    activate Frontend

    Frontend ->> Backend: 更新要求
    activate Backend

    Backend ->> Database: フィード更新クエリ（ダミーデータ）
    activate Database

    Database -->> Backend: 更新データ
    deactivate Database

    Backend -->> Frontend: 更新完了
    deactivate Backend

    Frontend -->> Frontend: フィード更新表示

    deactivate Frontend

```
