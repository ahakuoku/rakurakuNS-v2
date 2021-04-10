**こちらはpython版らくらくNS（開発中）のページです。bat版らくらくNSのページは[こちら](https://github.com/ahakuoku/rakurakuNS/blob/main/readme.md)。**

# らくらくNSとは？
SimutransのNSを管理するツールです。
- サーバーがクラッシュした場合に自動で再起動、それに付帯して必要な動作もすべて自動で行います。(一部要nettool)
- 一定の間隔でオートセーブを行います。(要nettool)オートセーブしたファイルはautosaveフォルダに100個まで保存されます。

といった機能があります。

# 導入方法
現在公開しているファイルはありません。

# ダウンロード
現在公開しているファイルはありません。

# 使用条件
**※注意※ このライセンスは仮のものです。**  
著作権は作者であるahakuokuが保有しています。  
改造・再配布(未改造・改造問わず)は自由にしていただいても結構です。(報告は任意)  
ただし、再配布をする場合はどこかに必ず原作者であるahakuokuの名を入れてください。  
改造はノンサポート、自己責任です。改造したことによる損害は一切責任を負いません。 このbatの営利目的での使用はご遠慮ください。

# 内容
現在公開しているファイルはありません。

# 使用方法

## setting.py(仮称)
各種動作を設定するファイルです。使用する前にこちらを編集してください。具体的な使用方法は下にあります。なお、現在python版らくらくNSは開発中のため、設定ファイルに存在しない項目が記載されている場合があります。そのような設定は原則使用できません。
- use_nettool … nettoolを使用するかどうかを設定します。1の場合に使用します。
- nettool_password … nettoolのパスワードを設定します。usingnettoolが0の場合は使用しません。
- launch_file … サーバーがクラッシュした際に起動するファイルを設定します。-server オプションをつけたショートカットを起動するなどに使用できます。
- server_save … オートセーブでのセーブ先データー(server13353-network.sveなど)を指定します。
- load_save … サーバーで読み込まれるセーブデーターを指定します。
- check_exe … サーバーのファイル名を指定します。サーバーが動いているかのチェックに使用します。
- server_address … サーバーのIPアドレスを指定します。
- topmost_company_password … デフォルト会社のパスワードを指定します。usingnettoolが0の場合は使用しません。
- autosave_interval … オートセーブの間隔を秒で指定します。usingnettoolが0の場合は使用しません。60未満にはできません。
- conflict_error_avoidanc … 自動再起動の後にスペースキーを自動で押すかどうかを指定します。pak重複警告の回避に使用できます。1の場合に有効になります。
- ban_address_1 … BANするIPアドレスを指定します。
- ban_address_2 … 同上
- ban_address_3 … 同上
- ban_address_4 … 同上
- ban_address_5 … 同上
- use_discord_bot … サーバークラッシュなどの際に、Discordにメッセージを投稿するかを設定します。1の場合にメッセージを投稿します。
- discord_bot_token … Discordのbotのトークンを設定します。このトークンは外部に漏らさない様ご注意ください。
- discord_send_channel … Discordにメッセージを投稿する際の送信先チャンネルを指定します。

## autostart.py(仮称)
サーバーがクラッシュした場合に、自動再起動などの必要な動作を自動で行います。  
具体的には、pak重複警告を回避するためのスペースキー自動押下、自動での操作禁止会社へのパスワード設定、クラッシュによりリセットされたBANリストの再設定を行います。(デフォルトではいずれも無効です)

## autosave.py(仮称)
一定の間隔でオートセーブを行います。オートセーブ30秒前に予告メッセージを流します。オートセーブ前のデーターは100までautosaveフォルダにバックアップされます。動作にはnettoolが必要です。

## autoclose.py(仮称)
自動的にサーバーを安全な状態で停止します。サーバー停止の前にautostart.pyを終了させてください。動作にはnettoolが必要です。

## serverupdate.py(仮称)
サーバーの本体をアップデートします。古い本体はserver_old.exeとしてバックアップされます。

# Discordへのメッセージ投稿機能
らくらくNS(python版)では、Discordへのメッセージ投稿機能を使用する事により次のことが行えるようになります。
- サーバーがクラッシュしたこと、復旧したことをDiscordで通知できる
- オートセーブの予告をDiscordで自動的に行える  
なお、使用するには設定の`use_discord_bot`を1にする必要があります。また、らくらくNS(bat版)とは異なり、[Simutrans world monitor](https://github.com/teamhimeh/simutrans_world_monitor)との連携機能は使用できません。

# 更新履歴
- 現在開発中です。公開までしばらくお待ちください。