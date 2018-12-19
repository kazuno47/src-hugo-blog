---
title: "Requests"
date: 2018-12-19T16:16:14+09:00
draft: true
---

# Requests

## memo

### API のレスポンスタイム計測

<pre>
response.elapsed.total_seconds()
</pre>

参考: <http://docs.python-requests.org/en/latest/api/?highlight=elapsed#requests.Response.elapsed>

### HTTPS アクセス時の証明書の警告無視と、warning 抑制

#### 証明書の警告無視

<pre>
requests.get(url, verify=False)
</pre>


#### warning 抑制

警告無視すると、コンソールにログが出続ける。邪魔な場合には下記で消す。

<pre>
import urllib3
urllib3.disable_warnings(urllib3.exceptions.InsecureRequestWarning)
</pre>

参考: <https://stackoverflow.com/questions/27981545/suppress-insecurerequestwarning-unverified-https-request-is-being-made-in-pytho>

### logger 設定

上記の InsecureReqjestWarning には聞かないようだが、ログレベルの変更方法は下記。

<pre>
logging.getLogger("requests").setLevel(logging.WARNING)
logging.getLogger('urllib3').setLevel(logging.WARNING)
</pre>
