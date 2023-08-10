# データベース設計

```mermaid
erDiagram
  users |--o{ memos : ""
  memos |--|{ pages : ""
  memos |--| icons : ""

  users {
    string user_id PK
    string user_name "ユーザー名"
    string twitter_id "ツイッターID"
    string bearer_token "ベアラートークン"
  }

  memos {
    string memo_id PK "メモID"
    references user_id FK "作成ユーザーID"
    string title "メモタイトル"
    string description "説明文"
    string icon_file_id FK "アイコンのファイルID"
    string param_name_1 "パラメータ名1"
    string param_name_2 "パラメータ名2"
    string param_name_3 "パラメータ名3"
    string param_name_4 "パラメータ名4"
    string param_name_5 "パラメータ名5"
    string param_name_6 "パラメータ名6"
    string param_val_1 "パラメータ値1"
    string param_val_2 "パラメータ値2"
    string param_val_3 "パラメータ値3"
    string param_val_4 "パラメータ値4"
    string param_val_5 "パラメータ値5"
    string param_val_6 "パラメータ値6"
    datetime created_at　"作成日時"
  }

  pages {
    string page_id PK
    references user_id "ユーザーID"
    references memo_id "メモID"
    int index "ページ番号"
    string header "見出し"
    string content "本文"
    string image_file_id FK "画像のファイルID"
    string timer "タイマー設定時間(mm:ss)"
  }

  icons {
    string icon_file_id PK "アイコンファイルのID"
    references user_id FK "ユーザーID"
  }

```