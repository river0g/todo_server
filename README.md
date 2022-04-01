# todo_server

簡易な api サーバー。\
pythonanywhere で使用することをゴールとしている。

# introduction(自分用)

1. https://www.pythonanywhere.com/ にアクセス, 登録する。
2. ダッシュボード画面右上にある Account をクリック
3. タブメニューから API Token を選択
4. create a new API token をクリック
5. ダッシュボードに戻り New Console→\$bash をクリック
6. ヘルパーツールのインストールをする。以下を実行。
   - `pip3.6 install –user pythonanywhere`
   - `pa_autoconfigure_django.py --python=3.6 https://github.com/river0g/todo_server.git --nuke`
7. スーパーユーザーの作成をする。
   - `python manage.py createsuperuser`
8. Files に行き drfproject 内の settings.py を開く
9. ローカルの環境変数を直入力。終わり。

# introduction(他人用)

1. ローカルで django-rest-framework を作成する。(割愛)
2. それを git にあげる。
3. https://www.pythonanywhere.com/ にアクセス, 登録する。
4. ダッシュボード画面右上にある Account をクリック
5. タブメニューから API Token を選択
6. create a new API token をクリック
7. ダッシュボードに戻り New Console→\$bash をクリック
8. ヘルパーツールのインストールをする。以下を実行。
   - `pip3.6 install –user pythonanywhere`
   - `pa_autoconfigure_django.py --python=3.6 https://github.com/ユーザー名/リポジトリ名.git --nuke`
9. スーパーユーザーの作成をする。
   - `python manage.py createsuperuser`
10. Files に行き drfproject 内の settings.py を開く
11. ローカルの環境変数を直入力。終わり。

# EndPoints

base_url = https://ユーザー名.pythonanywhere.com/

- admin のページ → (GET) `base_url/admin/`
- token が返る(user の name,pass 必須) → (POST) `base_url/auth/`
- token 認証した user の情報 → (GET,PUT,DELETE,POST) `base_url/api/myself`
- 登録したタスクを見る → (GET, POST) `base_url/api/tasks`
- 登録されているユーザーを見る → (GET,PUT,DELETE,POST) `base_url/api/users`
