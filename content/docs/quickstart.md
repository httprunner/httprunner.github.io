---
title: ๐ ๅฟซ้ไธๆ
weight: 2
description: 10 ๅ้ๅๅฟซ้ไธๆ HttpRunner
---

HttpRunner ็้ฆ่ฆๆ ธๅฟ็ฎๆ ๅฐฑๆฏใ็ฎๅๆ็จใ๏ผๅณไฝฟไฝ ๆฏๆฐ็จๆท๏ผไฝ ไนๅฏไปฅๅจ 10 ๅ้ไนๅๅฟซ้ไธๆ HttpRunnerใ

้ฃๆไปฌ่ฎกๆถๅผๅงๅง๏ผ๐

## ๅฎ่ฃ้จ็ฝฒ

`HttpRunner v4` ้็จ Golang ๅผๅ๏ผๅทฒ้ๅฏนไธปๆตๆไฝ็ณป็ป้ข็ผ่ฏไบไบ่ฟๅถๆไปถ๏ผๅช้ๅจ็ณป็ป็ป็ซฏไธญๆง่กไธๆกๅฝไปคๅณๅฏๅฎๆๅฎ่ฃ้จ็ฝฒใ

```bash
$ bash -c "$(curl -ksSL https://httprunner.com/script/install.sh)"
```

ๅฎ่ฃๆๅๅ๏ผไฝ ๅฐ่ทๅพไธไธช `hrp` ๅฝไปค่กๅทฅๅท๏ผๆง่ก `hrp -h` ๅณๅฏๆฅ็ๅฐๅๆฐๅธฎๅฉ่ฏดๆใ

```text
$ hrp -h

โโโ  โโโโโโโโโโโโโโโโโโโโโโโโโโโโ โโโโโโโ โโโ   โโโโโโโ   โโโโโโโ   โโโโโโโโโโโโโโโโโโ
โโโ  โโโโโโโโโโโโโโโโโโโโโโโโโโโโโโโโโโโโโโโโ   โโโโโโโโ  โโโโโโโโ  โโโโโโโโโโโโโโโโโโโ
โโโโโโโโ   โโโ      โโโ   โโโโโโโโโโโโโโโโโโโ   โโโโโโโโโ โโโโโโโโโ โโโโโโโโโ  โโโโโโโโ
โโโโโโโโ   โโโ      โโโ   โโโโโโโ โโโโโโโโโโโ   โโโโโโโโโโโโโโโโโโโโโโโโโโโโโ  โโโโโโโโ
โโโ  โโโ   โโโ      โโโ   โโโ     โโโ  โโโโโโโโโโโโโโโ โโโโโโโโโ โโโโโโโโโโโโโโโโโ  โโโ
โโโ  โโโ   โโโ      โโโ   โโโ     โโโ  โโโ โโโโโโโ โโโ  โโโโโโโโ  โโโโโโโโโโโโโโโโ  โโโ

HttpRunner is an open source API testing tool that supports HTTP(S)/HTTP2/WebSocket/RPC
network protocols, covering API testing, performance testing and digital experience
monitoring (DEM) test types. Enjoy! โจ ๐ โจ

License: Apache-2.0
Website: https://httprunner.com
Github: https://github.com/httprunner/httprunner
Copyright 2017 debugtalk

Usage:
  hrp [command]

Available Commands:
  boom         run load test with boomer
  completion   generate the autocompletion script for the specified shell
  convert      convert JSON/YAML testcases to pytest/gotest scripts
  har2case     convert HAR to json/yaml testcase files
  help         Help about any command
  pytest       run API test with pytest
  run          run API test with go engine
  startproject create a scaffold project

Flags:
  -h, --help               help for hrp
      --log-json           set log to json format
  -l, --log-level string   set log level (default "INFO")
  -v, --version            version for hrp

Use "hrp [command] --help" for more information about a command.
```

HttpRunner ่ฟๆฏๆๅค็งๅฎ่ฃ้จ็ฝฒๆนๅผ๏ผ่ฏฆ่ง็จๆทๆๅ็[ๅฎ่ฃ่ฏดๆ]้จๅใ

## ่ๆๆถๅๅปบ้กน็ฎ

HttpRunner ๆฏๆไฝฟ็จ่ๆๆถๅๅปบ็คบไพ้กน็ฎใ

ๆง่ก `hrp startproject` ๅฝไปค๏ผๅณๅฏๅๅงๅๆๅฎๅ็งฐ็้กน็ฎๅทฅ็จใ

```bash
$ hrp startproject demo
10:13PM INF Set log to color console other than JSON format.
10:13PM ??? Set log level
10:13PM INF create new scaffold project force=false pluginType=py projectName=demo
10:13PM INF create folder path=demo
10:13PM INF create folder path=demo/har
10:13PM INF create file path=demo/har/.keep
10:13PM INF create folder path=demo/testcases
10:13PM INF create folder path=demo/reports
10:13PM INF create file path=demo/reports/.keep
10:13PM INF create file path=demo/.gitignore
10:13PM INF create file path=demo/.env
10:13PM INF create file path=demo/testcases/demo_with_funplugin.json
10:13PM INF create file path=demo/testcases/demo_requests.yml
10:13PM INF create file path=demo/testcases/demo_ref_testcase.yml
10:13PM INF start to create hashicorp python plugin
10:13PM INF create file path=demo/debugtalk.py
10:13PM INF ensure python3 venv packages=["funppy==v0.4.3"] python=/Users/debugtalk/.hrp/venv/bin/python
10:13PM INF python package is ready name=funppy version=0.4.3
10:13PM INF create scaffold success projectName=demo
```

ๅฆไธๆฏ้กน็ฎๅทฅ็จ็็ฎๅฝ็ปๆ๏ผ

```text
$ tree demo -a
demo
โโโ .env
โโโ .gitignore
โโโ debugtalk.py
โโโ har
โ   โโโ .keep
โโโ reports
โ   โโโ .keep
โโโ testcases
    โโโ demo_ref_testcase.yml
    โโโ demo_requests.yml
    โโโ demo_with_funplugin.json

3 directories, 8 files
```

ๅถไธญ๏ผtestcases ๆไปถๅคนไธญๅๅซไบๅคไธช็คบไพๆต่ฏ็จไพใๅณไบ HttpRunner ๆต่ฏๅทฅ็จ็็ฎๅฝ็ปๆ่ฏดๆ๏ผๅฏๆฅ็็จๆทๆๅ็[ๆต่ฏๅทฅ็จ็ฎๅฝ็ปๆ]้จๅใ

HttpRunner ๅๅปบ่ๆๆถ้กน็ฎๆถ้ป่ฎค้ๆฉ Python ๆไปถๆจกๅผ๏ผๅผๅฎน v4 ไปฅๅ็็ๆฌ๏ผ๏ผไฝๅๆถ่ฟๆฏๆๅค็งๅถๅฎๆจกๅผ๏ผๅฏๆฅ็็จๆทๆๅ็[่ๆๆถๅๅปบ้กน็ฎ]้จๅไบ่งฃๆดๅค่ฏฆๆใ

## ๅ่งๆต่ฏ็จไพ

ๆฅไธๆฅๆไปฌไปฅ `demo_requests.yml` ไธบไพ๏ผๅๆญฅ้ข่งไธ HttpRunner ็ๆต่ฏ็จไพ็ปๆใ

```yaml
config:
    name: "request methods testcase with functions"
    variables:
        foo1: config_bar1
        foo2: config_bar2
        expect_foo1: config_bar1
        expect_foo2: config_bar2
    base_url: "https://postman-echo.com"
    verify: False
    export: ["foo3"]

teststeps:
-
    name: get with params
    variables:
        foo1: bar11
        foo2: bar21
        sum_v: "${sum_two(1, 2)}"
    request:
        method: GET
        url: /get
        params:
            foo1: $foo1
            foo2: $foo2
            sum_v: $sum_v
        headers:
            User-Agent: HttpRunner/${get_httprunner_version()}
    extract:
        foo3: "body.args.foo2"
    validate:
        - eq: ["status_code", 200]
        - eq: ["body.args.foo1", "bar11"]
        - eq: ["body.args.sum_v", "3"]
        - eq: ["body.args.foo2", "bar21"]
-
    name: post raw text
    variables:
        foo1: "bar12"
        foo3: "bar32"
    request:
        method: POST
        url: /post
        headers:
            User-Agent: HttpRunner/${get_httprunner_version()}
            Content-Type: "text/plain"
        data: "This is expected to be sent back as part of response body: $foo1-$foo2-$foo3."
    validate:
        - eq: ["status_code", 200]
        - eq: ["body.data", "This is expected to be sent back as part of response body: bar12-$expect_foo2-bar32."]
-
    name: post form data
    variables:
        foo2: bar23
    request:
        method: POST
        url: /post
        headers:
            User-Agent: HttpRunner/${get_httprunner_version()}
            Content-Type: "application/x-www-form-urlencoded"
        data: "foo1=$foo1&foo2=$foo2&foo3=$foo3"
    validate:
        - eq: ["status_code", 200]
        - eq: ["body.form.foo1", "$expect_foo1"]
        - eq: ["body.form.foo2", "bar23"]
        - eq: ["body.form.foo3", "bar21"]
```

HttpRunner ๆต่ฏ็จไพๅๆฌไธไปๆไธค้จๅ๏ผ

- config๏ผๆต่ฏ็จไพ็ๅฌๅฑ้็ฝฎ้จๅ๏ผๅๆฌ็จไพๅ็งฐใbase_urlใๅๆฐๅๆฐๆฎๆบใๆฏๅฆๅผๅฏ SSL ๆ ก้ช็ญ
- teststeps๏ผๆๅบๆญฅ้ชค็้ๅ๏ผ้็จไบ `go interface` ็่ฎพ่ฎก็ๅฟต๏ผๆฏๆ่ฟ่กไปปๆๅ่ฎฎๅๆต่ฏ็ฑปๅ็ๆๅฑ๏ผ็่ณๅๆฌ UI ่ชๅจๅ๏ผ

ๅจไธ้ข็ๆกไพไธญ๏ผๆฏไธช step ้ฝๆฏไธไธช HTTP ่ฏทๆฑ๏ผๅฏไปฅ็ๅฐ๏ผๆ่ฟฐไฟกๆฏไปๅๅซไบ HTTP ่ฏทๆฑๅ็ปๆๆ ก้ช็ๆ ธๅฟ่ฆ็ด ๏ผๆฒกๆไปปไฝ็ดฏ่ต็ๅๅฎนใ

ๅๆถ๏ผ้่ฆ้็นๅณๆณจ็ๆฏ๏ผ่ฝ็ถไธ้ข็็จไพๆฏ YAML ๆๆฌ๏ผไฝๅๆ ทๆฏๆๅผ็จๅ้ๅ่ฐ็จๅฝๆฐใ

- ๅ้ๅผ็จ๏ผ็บฆๅฎ้่ฟ `${}` ๆ `$` ็ๅฝขๅผๆฅๅผ็จๅ้๏ผไพๅฆ `$foo1` ๆ `${foo1}`
- ๅฝๆฐ่ฐ็จ๏ผ็บฆๅฎ้่ฟ `${}` ็ๅฝขๅผๆฅ่ฐ็จๆไปถๅฝๆฐ๏ผไพๅฆ `${sum_two(1, 2)}`

ๅ้็็ณๆๅฎไนๅจ step ๆ config ็ `variables` ไธญ๏ผๅนถไธ้ตๅพชไผๅ็บง็่ฆๆฑใ

ๅฝๆฐ็็ณๆๅฎไนๅจ้กน็ฎๆ น็ฎๅฝ็ `debugtalk.py` ไธญ๏ผๅบไบใ็บฆๅฎๅคงไบ้็ฝฎใ็่ฎพ่ฎก็ๅฟต๏ผๆไปฌๆ ้ๅจๆต่ฏ็จไพไธญ่ฟ่ก้็ฝฎใ

```python
import funppy


def get_httprunner_version():
    return "v4.0.0-alpha"


def sum_two_int(a: int, b: int) -> int:
    return a + b


if __name__ == '__main__':
    funppy.register("get_httprunner_version", get_httprunner_version)
    funppy.register("sum_two", sum_two_int)
    funppy.serve()
```

ๅจ `debugtalk.py` ไธญ๏ผๆไปฌๅฏไปฅ็ผๅๅฎ็ฐไปปๆ่ชๅฎไน้ป่พ็ๅฝๆฐ๏ผๅช้้่ฟ `funppy` ่ฟ่ก `register` ๅ `serve()` ๅณๅฏใ

ๅณไบๅ้ใๅฝๆฐใๆไปถ็ญๆฆๅฟต๏ผๅฏ่ฏฆ็ป้่ฏป[ๆ ธๅฟๆฆๅฟต]ใ

## ่ฟ่กๆฅๅฃๆต่ฏ

ๆต่ฏ็จไพๅฐฑ็ปชๅ๏ผ้่ฟ `hrp run` ๅฝไปคๅณๅฏๆง่กๆๅฎ็ๆต่ฏ็จไพ๏ผๅฆ้็ๆ HTML ๆต่ฏๆฅๅ๏ผๅฏ้ๅธฆ `--gen-html-report` ๅๆฐใ

```bash
$ hrp run demo/testcases/demo_requests.yml demo/testcases/demo_ref_testcase.yml --gen-html-report
```

<details>
<summary>ๆฅ็่ฟ่กๆฅๅฟ</summary>

```text
$ hrp run demo/testcases/demo_requests.yml demo/testcases/demo_ref_testcase.yml --gen-html-report
11:28PM INF Set log to color console other than JSON format.
11:28PM ??? Set log level
11:28PM INF [init] SetFailfast failfast=true
11:28PM INF [init] SetSaveTests saveTests=false
11:28PM INF [init] SetgenHTMLReport genHTMLReport=true
11:28PM INF [init] SetRequestsLogOn
11:28PM INF load file path=testcases/demo_requests.yml
11:28PM INF load testcases successfully count=1
11:28PM INF init session runner
11:28PM INF run testcase start testcase="request methods testcase with functions"
11:28PM INF init session runner
11:28PM INF python3 venv is ready funppyVersion=0.4.2 venvDir=/Users/debugtalk/.hrp/venv
11:28PM INF load hashicorp go plugin success path=/Users/debugtalk/MyProjects/HttpRunner-dev/httprunner.github.io/demo/debugtalk.py
11:28PM INF run step start step="get with params" type=request-GET
11:28PM INF function GetNames called on host side
11:28PM INF call function via gRPC funcArgs=[1,2] funcName=sum_two
11:28PM INF call function success arguments=[1,2] funcName=sum_two output=3
11:28PM INF function GetNames called on host side
11:28PM INF call function via gRPC funcArgs=[] funcName=get_httprunner_version
11:28PM INF call function success arguments=[] funcName=get_httprunner_version output=v4.0.0-alpha
-------------------- request --------------------
GET /get?foo1=bar11&foo2=bar21&sum_v=3 HTTP/1.1
Host: postman-echo.com
User-Agent: HttpRunner/v4.0.0-alpha


==================== response ===================
HTTP/1.1 200 OK
Content-Length: 335
Connection: keep-alive
Content-Type: application/json; charset=utf-8
Date: Sun, 10 Apr 2022 15:28:26 GMT
Etag: W/"14f-7Gzvv7hBEzQUyUYoNokC4etN280"
Set-Cookie: sails.sid=s%3ArupBebwxLVsoyG0nCfHMNjM-4u_aPEYs.tfgPzcR7kRyd2zuJqv7Vb%2FxlUJKFilYWoOtxXu7QsxA; Path=/; HttpOnly
Vary: Accept-Encoding

{"args":{"foo1":"bar11","foo2":"bar21","sum_v":"3"},"headers":{"x-forwarded-proto":"https","x-forwarded-port":"443","host":"postman-echo.com","x-amzn-trace-id":"Root=1-6252f79a-0e1cf4283dee310914d69da1","user-agent":"HttpRunner/v4.0.0-alpha","accept-encoding":"gzip"},"url":"https://postman-echo.com/get?foo1=bar11&foo2=bar21&sum_v=3"}
--------------------------------------------------
11:28PM INF extract value from=body.args.foo2 value=bar21
11:28PM INF set variable value=bar21 variable=foo3
11:28PM INF validate status_code assertMethod=eq checkExpr=status_code checkValue=200 expectValue=200 result=true
11:28PM INF validate body.args.foo1 assertMethod=eq checkExpr=body.args.foo1 checkValue=bar11 expectValue=bar11 result=true
11:28PM INF validate body.args.sum_v assertMethod=eq checkExpr=body.args.sum_v checkValue=3 expectValue=3 result=true
11:28PM INF validate body.args.foo2 assertMethod=eq checkExpr=body.args.foo2 checkValue=bar21 expectValue=bar21 result=true
11:28PM INF run step end exportVars={"foo3":"bar21"} step="get with params" success=true type=request
11:28PM INF run step start step="post raw text" type=request-POST
11:28PM INF call function via gRPC funcArgs=[] funcName=get_httprunner_version
11:28PM INF call function success arguments=[] funcName=get_httprunner_version output=v4.0.0-alpha
-------------------- request --------------------
POST /post HTTP/1.1
Host: postman-echo.com
Content-Type: text/plain
User-Agent: HttpRunner/v4.0.0-alpha

This is expected to be sent back as part of response body: bar12-config_bar2-bar32.
==================== response ===================
HTTP/1.1 200 OK
Content-Length: 441
Connection: keep-alive
Content-Type: application/json; charset=utf-8
Date: Sun, 10 Apr 2022 15:28:26 GMT
Etag: W/"1b9-biNClRDBTZ3yYGizMLRqBbpZaqc"
Set-Cookie: sails.sid=s%3AShiSgikIS1udNVe0IOdEVNf9rL_125st.D6%2Fw%2BIyKg5jeiOs6xwL8wsEht4tcO%2BpwXNqNWoFZQ3o; Path=/; HttpOnly
Vary: Accept-Encoding

{"args":{},"data":"This is expected to be sent back as part of response body: bar12-config_bar2-bar32.","files":{},"form":{},"headers":{"x-forwarded-proto":"https","x-forwarded-port":"443","host":"postman-echo.com","x-amzn-trace-id":"Root=1-6252f79a-75965ac66ae0074d0f1df200","content-length":"83","user-agent":"HttpRunner/v4.0.0-alpha","content-type":"text/plain","accept-encoding":"gzip"},"json":null,"url":"https://postman-echo.com/post"}
--------------------------------------------------
11:28PM INF validate status_code assertMethod=eq checkExpr=status_code checkValue=200 expectValue=200 result=true
11:28PM INF validate body.data assertMethod=eq checkExpr=body.data checkValue="This is expected to be sent back as part of response body: bar12-config_bar2-bar32." expectValue="This is expected to be sent back as part of response body: bar12-config_bar2-bar32." result=true
11:28PM INF run step end exportVars=null step="post raw text" success=true type=request
11:28PM INF run step start step="post form data" type=request-POST
11:28PM INF call function via gRPC funcArgs=[] funcName=get_httprunner_version
11:28PM INF call function success arguments=[] funcName=get_httprunner_version output=v4.0.0-alpha
-------------------- request --------------------
POST /post HTTP/1.1
Host: postman-echo.com
Content-Type: application/x-www-form-urlencoded
User-Agent: HttpRunner/v4.0.0-alpha

foo1=config_bar1&foo2=bar23&foo3=bar21
==================== response ===================
HTTP/1.1 200 OK
Content-Length: 479
Connection: keep-alive
Content-Type: application/json; charset=utf-8
Date: Sun, 10 Apr 2022 15:28:27 GMT
Etag: W/"1df-+YTOdiT8pYPlN+1k+z3s4LiSJJw"
Set-Cookie: sails.sid=s%3A5E7k9yIyZQq2qk-So2GS_h2eCMGeosyg.rmNVhBKq49FZm%2BXaH33KdzEqlPwwveKMO5rxh2%2F%2FvFo; Path=/; HttpOnly
Vary: Accept-Encoding

{"args":{},"data":"","files":{},"form":{"foo1":"config_bar1","foo2":"bar23","foo3":"bar21"},"headers":{"x-forwarded-proto":"https","x-forwarded-port":"443","host":"postman-echo.com","x-amzn-trace-id":"Root=1-6252f79b-3c6359e66dad26597ece3881","content-length":"38","user-agent":"HttpRunner/v4.0.0-alpha","content-type":"application/x-www-form-urlencoded","accept-encoding":"gzip"},"json":{"foo1":"config_bar1","foo2":"bar23","foo3":"bar21"},"url":"https://postman-echo.com/post"}
--------------------------------------------------
11:28PM INF validate status_code assertMethod=eq checkExpr=status_code checkValue=200 expectValue=200 result=true
11:28PM INF validate body.form.foo1 assertMethod=eq checkExpr=body.form.foo1 checkValue=config_bar1 expectValue=config_bar1 result=true
11:28PM INF validate body.form.foo2 assertMethod=eq checkExpr=body.form.foo2 checkValue=bar23 expectValue=bar23 result=true
11:28PM INF validate body.form.foo3 assertMethod=eq checkExpr=body.form.foo3 checkValue=bar21 expectValue=bar21 result=true
11:28PM INF run step end exportVars=null step="post form data" success=true type=request
11:28PM INF run testcase end testcase="request methods testcase with functions"
11:28PM INF create folder path=reports
11:28PM INF generate HTML report path=reports/report-1650809917.html
11:28PM INF quit hashicorp plugin process
```
</details>

ๆต่ฏ็ๆ็ HTML ๆฅๅๅฆไธๆ็คบใ

<img src="/image/demo-html-report.png" alt="HttpRunner html report" width="600">

ๅจ HTML ๆต่ฏๆฅๅไธญ๏ผๅฏไปฅ็นๅปๆฅ็ๅฐ่ฏฆ็ป็่ฏทๆฑๅๅฎนๅๅๅบ็ปๆ๏ผ่ฏฆ่ง [demo-html-report]ใ

## ่ฟ่กๆง่ฝๆต่ฏ

้ๅฏนๅทฒๆ็ๆฅๅฃๆต่ฏ็จไพ๏ผHttpRunner ๆ ้ไปปไฝ้ขๅค็ๅทฅไฝ๏ผๅณๅฏ้่ฟ `hrp boom` ๅฝไปค่ฟ่กๆง่ฝๆต่ฏ๏ผ้่ฟ `--spawn-count` ๅๆฐๅฏๆๅฎๅนถๅ็จๆทๆฐ๏ผ้่ฟ `--spawn-rate` ๅฏๆๅฎ่ตทๅงๅๅๆ็ใ

```bash
$ hrp boom testcases/demo_requests.yml --spawn-count 100 --spawn-rate 10
```

ๅจๅๆต่ฟ่ก่ฟ็จไธญ๏ผๆฏ้ 3 ็งๆๅฐไธๆฌกๆง่ฝๆฑๆปๆฐๆฎ๏ผ้่ฟ `CTRL + C` ็ปๆญขๆต่ฏๅ๏ผไผๆๅฐๆดไธชๅๆต่ฟ็จ็ๆฑๆปๆฐๆฎ๏ผStatistics Summary๏ผใ

<details>
<summary>ๆฅ็่ฟ่กๆฅๅฟ</summary>

```text
$ cd demo/
$ hrp boom testcases/demo_requests.yml --spawn-count 100 --spawn-rate 10
10:19PM INF Set log to color console other than JSON format.
10:19PM INF get current ulimit limit=1048575
10:19PM ??? Set log level
Current time: 2022/04/24 22:19:40, Users: 29, State: spawning, Total RPS: 5.0, Total Average Response Time: 1868.9ms, Total Fail Ratio: 0.0%
Accumulated Transactions: 0 Passed, 0 Failed
+-------------+-----------------+------------+---------+--------+---------+------+------+--------------+------------+-------------+
|    TYPE     |      NAME       | # REQUESTS | # FAILS | MEDIAN | AVERAGE | MIN  | MAX  | CONTENT SIZE | # REQS/SEC | # FAILS/SEC |
+-------------+-----------------+------------+---------+--------+---------+------+------+--------------+------------+-------------+
| request-GET | get with params |         15 |       0 |   1800 | 1868.93 | 1278 | 2778 |          334 |       5.00 |        0.00 |
+-------------+-----------------+------------+---------+--------+---------+------+------+--------------+------------+-------------+

Current time: 2022/04/24 22:19:43, Users: 59, State: spawning, Total RPS: 18.8, Total Average Response Time: 1068.4ms, Total Fail Ratio: 0.0%
Accumulated Transactions: 21 Passed, 0 Failed
+--------------+-----------------+------------+---------+--------+---------+------+------+--------------+------------+-------------+
|     TYPE     |      NAME       | # REQUESTS | # FAILS | MEDIAN | AVERAGE | MIN  | MAX  | CONTENT SIZE | # REQS/SEC | # FAILS/SEC |
+--------------+-----------------+------------+---------+--------+---------+------+------+--------------+------------+-------------+
| request-GET  | get with params |         37 |       0 |    890 |  943.57 |  511 | 2283 |          334 |      12.33 |        0.00 |
| request-POST | post raw text   |         40 |       0 |    890 |  979.08 |  510 | 2225 |          440 |      13.33 |        0.00 |
| request-POST | post form data  |         21 |       0 |    830 |  886.43 |  486 | 1439 |          478 |       7.00 |        0.00 |
| transaction  | Action          |         21 |       0 |   3500 | 3613.71 | 2346 | 5448 |            0 |       7.00 |        0.00 |
+--------------+-----------------+------------+---------+--------+---------+------+------+--------------+------------+-------------+

Current time: 2022/04/24 22:19:46, Users: 89, State: spawning, Total RPS: 36.8, Total Average Response Time: 1036.6ms, Total Fail Ratio: 0.0%
Accumulated Transactions: 79 Passed, 0 Failed
+--------------+-----------------+------------+---------+--------+---------+------+------+--------------+------------+-------------+
|     TYPE     |      NAME       | # REQUESTS | # FAILS | MEDIAN | AVERAGE | MIN  | MAX  | CONTENT SIZE | # REQS/SEC | # FAILS/SEC |
+--------------+-----------------+------------+---------+--------+---------+------+------+--------------+------------+-------------+
| request-GET  | get with params |         90 |       0 |    770 | 1036.70 |  385 | 2643 |          334 |      30.00 |        0.00 |
| request-POST | post form data  |         58 |       0 |    760 | 1052.45 |  386 | 2867 |          478 |      19.33 |        0.00 |
| request-POST | post raw text   |         70 |       0 |    730 |  972.26 |  334 | 2454 |          440 |      23.33 |        0.00 |
| transaction  | Action          |         58 |       0 |   3100 | 3175.78 | 1798 | 5490 |            0 |      19.33 |        0.00 |
+--------------+-----------------+------------+---------+--------+---------+------+------+--------------+------------+-------------+

Current time: 2022/04/24 22:19:49, Users: 100, State: running, Total RPS: 49.3, Total Average Response Time: 989.6ms, Total Fail Ratio: 0.0%
Accumulated Transactions: 167 Passed, 0 Failed
+--------------+-----------------+------------+---------+--------+---------+------+------+--------------+------------+-------------+
|     TYPE     |      NAME       | # REQUESTS | # FAILS | MEDIAN | AVERAGE | MIN  | MAX  | CONTENT SIZE | # REQS/SEC | # FAILS/SEC |
+--------------+-----------------+------------+---------+--------+---------+------+------+--------------+------------+-------------+
| request-GET  | get with params |         91 |       0 |    700 |  940.93 |  385 | 4030 |          334 |      30.33 |        0.00 |
| request-POST | post raw text   |         82 |       0 |    790 |  959.46 |  348 | 2990 |          440 |      27.33 |        0.00 |
| request-POST | post form data  |         88 |       0 |    680 |  891.30 |  359 | 2826 |          478 |      29.33 |        0.00 |
| transaction  | Action          |         88 |       0 |   2900 | 3092.40 | 1494 | 6534 |            0 |      29.33 |        0.00 |
+--------------+-----------------+------------+---------+--------+---------+------+------+--------------+------------+-------------+

Current time: 2022/04/24 22:19:52, Users: 100, State: running, Total RPS: 66.5, Total Average Response Time: 862.9ms, Total Fail Ratio: 0.0%
Accumulated Transactions: 300 Passed, 0 Failed
+--------------+-----------------+------------+---------+--------+---------+------+------+--------------+------------+-------------+
|     TYPE     |      NAME       | # REQUESTS | # FAILS | MEDIAN | AVERAGE | MIN  | MAX  | CONTENT SIZE | # REQS/SEC | # FAILS/SEC |
+--------------+-----------------+------------+---------+--------+---------+------+------+--------------+------------+-------------+
| request-GET  | get with params |        130 |       0 |    570 |  632.65 |  336 | 2651 |          334 |      43.33 |        0.00 |
| request-POST | post raw text   |        143 |       0 |    540 |  692.20 |  288 | 5288 |          440 |      47.67 |        0.00 |
| request-POST | post form data  |        133 |       0 |    560 |  707.69 |  289 | 5225 |          478 |      44.33 |        0.00 |
| transaction  | Action          |        133 |       0 |   1800 | 2364.09 | 1287 | 6991 |            0 |      44.33 |        0.00 |
+--------------+-----------------+------------+---------+--------+---------+------+------+--------------+------------+-------------+

Current time: 2022/04/24 22:19:55, Users: 100, State: running, Total RPS: 79.6, Total Average Response Time: 805.1ms, Total Fail Ratio: 0.0%
Accumulated Transactions: 445 Passed, 0 Failed
+--------------+-----------------+------------+---------+--------+---------+-----+------+--------------+------------+-------------+
|     TYPE     |      NAME       | # REQUESTS | # FAILS | MEDIAN | AVERAGE | MIN | MAX  | CONTENT SIZE | # REQS/SEC | # FAILS/SEC |
+--------------+-----------------+------------+---------+--------+---------+-----+------+--------------+------------+-------------+
| request-GET  | get with params |        143 |       0 |    560 |  743.29 | 284 | 3582 |          334 |      47.67 |        0.00 |
| request-POST | post raw text   |        147 |       0 |    430 |  635.65 | 294 | 4109 |          440 |      49.00 |        0.00 |
| request-POST | post form data  |        145 |       0 |    480 |  639.61 | 287 | 2945 |          478 |      48.33 |        0.00 |
| transaction  | Action          |        145 |       0 |   2100 | 2214.16 | 997 | 7045 |            0 |      48.33 |        0.00 |
+--------------+-----------------+------------+---------+--------+---------+-----+------+--------------+------------+-------------+

Current time: 2022/04/24 22:19:58, Users: 100, State: running, Total RPS: 85.4, Total Average Response Time: 781.9ms, Total Fail Ratio: 0.0%
Accumulated Transactions: 566 Passed, 0 Failed
+--------------+-----------------+------------+---------+--------+---------+------+------+--------------+------------+-------------+
|     TYPE     |      NAME       | # REQUESTS | # FAILS | MEDIAN | AVERAGE | MIN  | MAX  | CONTENT SIZE | # REQS/SEC | # FAILS/SEC |
+--------------+-----------------+------------+---------+--------+---------+------+------+--------------+------------+-------------+
| request-GET  | get with params |        122 |       0 |    690 |  821.39 |  289 | 2697 |          334 |      40.67 |        0.00 |
| request-POST | post raw text   |        118 |       0 |    440 |  570.67 |  284 | 1886 |          440 |      39.33 |        0.00 |
| request-POST | post form data  |        121 |       0 |    570 |  674.20 |  281 | 1956 |          478 |      40.33 |        0.00 |
| transaction  | Action          |        121 |       0 |   1900 | 2184.42 | 1085 | 5591 |            0 |      40.33 |        0.00 |
+--------------+-----------------+------------+---------+--------+---------+------+------+--------------+------------+-------------+

Current time: 2022/04/24 22:20:01, Users: 100, State: running, Total RPS: 89.8, Total Average Response Time: 772.1ms, Total Fail Ratio: 0.0%
Accumulated Transactions: 686 Passed, 0 Failed
+--------------+-----------------+------------+---------+--------+---------+-----+------+--------------+------------+-------------+
|     TYPE     |      NAME       | # REQUESTS | # FAILS | MEDIAN | AVERAGE | MIN | MAX  | CONTENT SIZE | # REQS/SEC | # FAILS/SEC |
+--------------+-----------------+------------+---------+--------+---------+-----+------+--------------+------------+-------------+
| request-GET  | get with params |        121 |       0 |    450 |  692.89 | 277 | 4343 |          334 |      40.33 |        0.00 |
| request-POST | post raw text   |        120 |       0 |    450 |  766.39 | 289 | 2768 |          440 |      40.00 |        0.00 |
| request-POST | post form data  |        120 |       0 |    390 |  710.49 | 281 | 2358 |          478 |      40.00 |        0.00 |
| transaction  | Action          |        120 |       0 |   2300 | 2387.42 | 944 | 6530 |            0 |      40.00 |        0.00 |
+--------------+-----------------+------------+---------+--------+---------+-----+------+--------------+------------+-------------+

Current time: 2022/04/24 22:20:04, Users: 100, State: running, Total RPS: 92.2, Total Average Response Time: 771.1ms, Total Fail Ratio: 0.0%
Accumulated Transactions: 794 Passed, 0 Failed
+--------------+-----------------+------------+---------+--------+---------+------+------+--------------+------------+-------------+
|     TYPE     |      NAME       | # REQUESTS | # FAILS | MEDIAN | AVERAGE | MIN  | MAX  | CONTENT SIZE | # REQS/SEC | # FAILS/SEC |
+--------------+-----------------+------------+---------+--------+---------+------+------+--------------+------------+-------------+
| request-GET  | get with params |        117 |       0 |    420 |  820.98 |  288 | 9068 |          334 |      39.00 |        0.00 |
| request-POST | post raw text   |        109 |       0 |    420 |  696.28 |  285 | 3644 |          440 |      36.33 |        0.00 |
| request-POST | post form data  |        108 |       0 |    420 |  773.34 |  277 | 4349 |          478 |      36.00 |        0.00 |
| transaction  | Action          |        108 |       0 |   1700 | 2283.30 | 1023 | 5632 |            0 |      36.00 |        0.00 |
+--------------+-----------------+------------+---------+--------+---------+------+------+--------------+------------+-------------+

Current time: 2022/04/24 22:20:07, Users: 100, State: quitting, Total RPS: 92.9, Total Average Response Time: 772.6ms, Total Fail Ratio: 1.9%
Accumulated Transactions: 882 Passed, 54 Failed
+--------------+-----------------+------------+---------+--------+---------+-----+-------+--------------+------------+-------------+
|     TYPE     |      NAME       | # REQUESTS | # FAILS | MEDIAN | AVERAGE | MIN |  MAX  | CONTENT SIZE | # REQS/SEC | # FAILS/SEC |
+--------------+-----------------+------------+---------+--------+---------+-----+-------+--------------+------------+-------------+
| request-GET  | get with params |         75 |       0 |    410 |  967.80 | 268 |  7825 |          334 |      25.00 |        0.00 |
| request-POST | post raw text   |        110 |      28 |    360 |  682.74 | 410 |  4683 |          328 |      36.67 |        9.33 |
| request-POST | post form data  |        114 |      26 |    360 |  764.04 | 437 |  8487 |          368 |      38.00 |        8.67 |
| transaction  | Action          |        142 |      54 |   2100 | 2593.81 | 317 | 11008 |            0 |      47.33 |       18.00 |
+--------------+-----------------+------------+---------+--------+---------+-----+-------+--------------+------------+-------------+

=========================================== Statistics Summary ==========================================
Current time: 2022/04/24 22:20:07, Users: 100, Duration: 30s, Accumulated Transactions: 882 Passed, 54 Failed
+-------+------------+---------+--------+---------+-----+------+--------------+------------+-------------+
| NAME  | # REQUESTS | # FAILS | MEDIAN | AVERAGE | MIN | MAX  | CONTENT SIZE | # REQS/SEC | # FAILS/SEC |
+-------+------------+---------+--------+---------+-----+------+--------------+------------+-------------+
| Total |       2788 |      54 |    590 |  772.65 | 437 | 9068 |          407 |      92.93 |        1.80 |
+-------+------------+---------+--------+---------+-----+------+--------------+------------+-------------+
```
</details>

## ๆป็ป

้่ฟไธ่ฟฐๆผ็คบ๏ผ็ธไฟกๅคงๅฎถๅทฒ็ปๅฏน HttpRunner ๆไบไธไธชๅๆญฅ็ๅฐ่ฑก๏ผๅนถไธๅบ่ฏฅๅฏไปฅๅๆญฅๅฐ HttpRunner ไธๆ่ท่ตทๆฅไบใ

้ไบ็ฏๅน๏ผๆฌๆไปๅฑ็คบไบ HttpRunner ๆๅบ็ก็ๅ่ฝ๏ผๅคงๅฎถๅฏไปฅ้่ฟ่ฟไธๆญฅ้่ฏป[็จๆทๆๅ]ๆข็ดข HttpRunner ็ๅจ้จๅ่ฝ็นๆงใ



[ๅฎ่ฃ่ฏดๆ]: /docs/user-guide/installation/
[ๆต่ฏๅทฅ็จ็ฎๅฝ็ปๆ]: /docs/introduction/concepts/#%E6%B5%8B%E8%AF%95%E5%B7%A5%E7%A8%8B%E7%9B%AE%E5%BD%95%E7%BB%93%E6%9E%84
[่ๆๆถๅๅปบ้กน็ฎ]: /docs/user-guide/scaffold/
[ๆ ธๅฟๆฆๅฟต]: /docs/introduction/concepts/
[demo-html-report]: /reports/demo-report.html
[็จๆทๆๅ]: /docs/user-guide/
