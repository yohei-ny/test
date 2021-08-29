# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

app/controller/todolists_controller
-1行目クラスの名前を変更
-Strong paramaterのrequireを削除、imageに_idを追加

app/models/list.rb
-attachmentのimageに_idを

app/views/todolists/new.html.erb
-loaal: trueを削除

db/migrate/20210723060706_add_name_to_lists.rb 
-versionを変更