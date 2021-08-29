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

## 6.新規登録後のurlがおかしい
- urlにtodolist.idとなっている
 >todolists_path(list.id)の引数を消す

## 6.indexで削除できない
- method: :delete
 > method: :deleteをlinkに付与する
 
## 7.newの投稿でリロードしないと反映されない
- local: trueの書き忘れ
 > form_withにlocal: trueの追加をする

## 8.updateでエラーはく
- 引数の(list_params)がない
 > list.update(list_params)にすれば良い

## 9.destroyの後に思った先にpathがいかない
- パスの遷移してがおかしい
 > todolists_path に変更する