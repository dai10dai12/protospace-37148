# テーブル設計

##usersテーブル

| Column             | Type   | Options                   |
| ------------------ | ------ | ------------------------  |
| email              | string | null: false, unique: true |
| encrypted_password | string | null: false               |
| name               | string | null: false               |
| profile            | string | null: false               |
| occupation         | text   | null: false               |
| position           | text   | null: false               |

##prototypesテーブル

| Column             | Type   | Options                        |
| ------------------ | ------ | -----------------------------  |
| title              | string | null: false                    |
| catch_copy         | string | null: false                    |
| concept            | string | null: false                    |
| user               | string | null: false, foreign_key: true |
| occupation         | text   | null: false                    |
| position           | text   | null: false                    |

##commentテーブル

| Column             | Type   | Options                        |
| ------------------ | ------ | -----------------------------  |
| content            | string | null: false                    |
| prototype          | string | null: false, foreign_key: true |
| user               | string | null: false, foreign_key: true |