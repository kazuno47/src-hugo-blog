---
title: "99.Trouble_shooting"
date: 2018-12-14T10:41:14+09:00
draft: false
---

トラぶった時の対応メモ

## コネクションが日本語

> コネクションを確認 

> nmcli c s 

> UUIDとデバイス名を確認する 

> コネクションを削除 

> nmcli c delete [UUID] 

> コネクション作成 

> nmcli c add type eth ifname [デバイス名] con-name [デバイス名] 

> これでデバイス名と同じコネクションネームになる 

> con-nameの次の[デバイス名]は任意の名前にしてもよい

### 参考

<https://qiita.com/masa-tu/items/ffb28a76ca0ebafa1a16> 

## 不明な接続 'ensxx' です

UUIDで指定するか、コネクションが日本語に記載のとおり、接続名をデバイス名と同じにしておけばいい。 

> nmcliのmanpageをみると、 

> nmcliのmanpage による投稿: 

> modify [--temporary] [id | uuid | path] ID [+|-]setting.property value... 

> となっていて、デバイス名を指定できるとは書かれていません。 

> ここで指定できるものというのはおそらく、 

> コード: 

> nmcli connection show 

> で出力される「NAME（たぶんこれがid）」や「UUID」などが該当すると思われるのですが、ネット上の情報をみると、以前は「NAME」の情報にもデバイス名が表示されていたようです。

### 参考

<https://forums.ubuntulinux.jp/viewtopic.php?id=18652>