---
title: "Dblib Error Message 20009"
date: 2019-01-15T17:27:18+09:00
draft: False
---

pymssql というライブラリを使用して、ローカルに立てた Microsoft SQL Server に接続を試みたが失敗した。

エラーメッセージは下記の感じ

> pymssql.OperationalError: DB-Lib error message 20009, severity 9:
> Unable to connect: Adaptive Server is unavailable or does not exist

pymssql の使い方が悪いのかと調べたり、試してみたりを繰り返してだいぶ時間を浪費してしまった。Microsft SQL Server Management Studio からはつながるので、mssql ライブラリの使い方か、ライブラリ自体が悪いのかと調査の方向を間違えたのが失敗だった。

最終的には下記の stackoverflow に記載の通りの内容だった。

<https://stackoverflow.com/questions/19348255/pymssql-operationalerror-db-lib-error-message-20009-severity-9>

ようするに、SQL Server は初期インストールでは TCP/IP が「有効」になっていないのが原因。

stackoverflow に記載の通り、Sql Server Configuration Manager を開き、SQL Server ネットワークの構成 → MSSQLSERVER　のプロトコル → TCP/IP が無効になっているのを有効にすればよい。
