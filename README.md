# デバック内容
## 1.migrateができない
- db/migrate/20210723060706_add_name_to_lists.rbファイルのversionが違う
 > AddNameToLists < ActiveRecord::Migration[6.0]を→[5.2]にする

## 2.indexで表示されない
- 1行目クラスの名前がおかしい
 > TdolistsController→TodolistsControllerにする

## 3.アタッチメントでエラーが吐く
- app/models/list.rbにattachmentのimageに_idがある
 > app/models/list.rbにattachmentのimage_idの_idを消す

## 4.createアクションに遷移ができない
- config/routes.rbにcreateアクションがない
 > post 'todolists' => 'todolists#create'を追加

## 5.新規投稿ができない
- Strong paramaterのrequireがない、imageに_idが付与されている
 > params.require(:list).permit(:title, :body, :image)とすれば良い

## 6.indexで削除できない
- method: :delete
 > method: :deleteをlinkに付与する


app/views/todolists/index.html.erb
-loaal: trueを削除


