# テーブル設計

## usersテーブル
| Column             | Type   | Options     |
| ------------------ | ------ | ----------- |
| nickname           | string | null: false |
| email              | string | null: false, unique: true |
| encrypted_password | string | null: false |

### Association
- has_many :tasks

## tasksテーブル
| Column              | Type      | Options     |
| ------------------- | ----------| ----------- |
| title               | string    | null: false |
| completed           | boolean   | null: false |
| start_time          | datetime  |
| end_time            | datetime  |
| total_time          | datetime  |
| user                | references| null: false, foreign_key: true|

### Association
- belongs_to :user
