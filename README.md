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

    activate User
    User->>Frontend: フィードを表示リクエスト
    activate Frontend
    Frontend->>Backend: フィード取得リクエスト
    activate Backend
    Backend-->>Database: ダミーデータ取得リクエスト
    activate Database
    Database-->>Backend: ダミーデータ
    deactivate Database
    Backend-->>Frontend: ダミーデータ
    deactivate Backend
    Frontend-->>User: フィード表示

    User->>Frontend: 投稿詳細表示リクエスト
    activate Frontend
    Frontend->>Backend: 投稿詳細取得リクエスト
    activate Backend
    Backend-->>Database: ダミーデータ取得リクエスト
    activate Database
    Database-->>Backend: ダミーデータ
    deactivate Database
    Backend-->>Frontend: ダミーデータ
    deactivate Backend
    Frontend-->>User: 投稿詳細表示

    User->>Frontend: 投稿検索リクエスト
    activate Frontend
    Frontend->>Backend: 投稿検索リクエスト
    activate Backend
    Backend-->>Database: ダミーデータ検索リクエスト
    activate Database
    Database-->>Backend: ダミーデータ
    deactivate Database
    Backend-->>Frontend: ダミーデータ
    deactivate Backend
    Frontend-->>User: 検索結果表示

    User->>Frontend: 更新リクエスト
    activate Frontend
    Frontend->>Backend: 更新リクエスト
    activate Backend
    Backend-->>Database: ダミーデータ更新リクエスト
    activate Database
    Database-->>Backend: ダミーデータ
    deactivate Database
    Backend-->>Frontend: ダミーデータ
    deactivate Backend
    Frontend-->>User: 更新完了

    deactivate Frontend
    deactivate User
```
