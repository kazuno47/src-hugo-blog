---
title: "02.Install"
date: 2018-12-14T10:22:46+09:00
draft: false
---

# CentOS7 の初期設定

RHEL が本番で使われることが多いので CentOS.

しかし、IBMに買収されたため、他のディストリビューションを選択肢にいれるべきかも。

## ユーザアカウントをsudoに追加 

<pre>
> visudo 
# ファイルの最終行に下記を追加 
username ALL=(ALL) ALL 
</pre>

## ネットワーク設定 

<pre>
# 下記がなぜかnoのため、yesに変える 
sudo vim /etc/sysconfig/network-scripts/ifcfg-ens32 
ONBOOT=no → ONBOOT=yes 
</pre>

## yum の proxy 設定

<pre>
> sudo yum vim /etc/yum.conf 
proxy={username}:{password}@{proxyhost}:{port} 
</pre>

## epel-release repository　の追加 

追加するくらいなら、最初から Fedora でいい気もする。

<pre>
> sudo yum install epel-release 
</pre>

## xrdp のインストール 

> sudo yum install xrdp 

## xrdp の色数変更 

<pre>
> sudo vim /etc/xrdp/xrdp.ini 
max_bpp=32 → max_bpp=24 
# 接続時にWindows側のRDPの設定変更もいるかも

# xrdp用にfirewallの穴あけ 
> firewall-cmd --permanent --zone=public --add-port=3389/tcp 
> firewall-cmd --reload 
</pre>
 

## 自動生成されるhomeフォルダを英語化する 

<pre>
LANG=C xdg-user-dirs-gtk-update 
</pre>

## Google Chrome のインストール

<pre>
> sudo vim /etc/yum.repos.d/google.chrome.repo 

[google-chrome] 
name=google-chrome 
baseurl=http://dl.google.com/linux/chrome/rpm/stable/$basearch 
enabled=1 
gpgcheck=1 
gpgkey=https://dl-ssl.google.com/linux/linux_signing_key.pub  

> sudo yum update 
> sudo yum install google-chrome-stable 

</pre>

## PyCharmのインストール 

Pycharmをダウンロードしてくる 

解凍してOptに配置 

<pre>
$ tar -xf pycharm-community-4.5.4.tar.gz 
$ sudo mv pycharm-community-4.5.4 /opt/pycharm 
</pre>
 
初回起動する。初回起動の設定で起動シェルが作られるので、以降はシェル起動が可能となる。 

<pre>
$ cd /opt/pycharm/bin 
$ ./pycharm.sh 
# シェル起動 
$ charm 
</pre>

## CNTLM 

日本のエンジニアは Proxy により生産性を大きく落とされている。

<pre>
# epel リポジトリが必要? 

sudo yum install cntlm  
sudo vim /etc/cntlm.conf 

&lt;!-- 
Username        &lt;username&gt;
Domain          &lt;domainname&gt;
Password        &lt;password&gt;
Proxy           &lt;proxyipaddress&gt;:&lt;portno&gt;
NoProxy         localhost, 127.0.0.*, 10.*, 192.168.* 
Listen          3128 
--&gt;

sudo systemctl restart cntlm 
</pre>
 

## JDKのインストール 

<pre>
> sudo yum install -y java-1.8.0-openjdk java-1.8.0-openjdk-devel
</pre>