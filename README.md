# ykawa

<p align="left"> 
  <img alt="Top Langs" height="150px" src="https://github-readme-stats.vercel.app/api/top-langs/?username=kurokawa5&layout=compact&show_icons=true&theme=onedark" />
  <img alt="github stats" height="150px" src="https://github-readme-stats.vercel.app/api?username=kurokawa5&theme=onedark&show_icons=ture" />
</p>



```mermaid
sequenceDiagram
    participant User
    participant Frontend
    participant Backend
    participant Database

    User->>Frontend: アクセス（フィード一覧表示要求）
    Frontend->>Backend: GET /feeds
    Backend->>Database: フィードデータのクエリ
    Database-->>Backend: フィードデータ
    Backend-->>Frontend: フィードデータのレスポンス
    Frontend-->>User: フィード一覧を表示

    User->>Frontend: 投稿カードクリック（詳細表示要求）
    Frontend->>Backend: GET /feeds/{id}
    Backend->>Database: 投稿詳細データのクエリ
    Database-->>Backend: 投稿詳細データ
    Backend-->>Frontend: 投稿詳細データのレスポンス
    Frontend-->>User: 投稿詳細を表示
```
