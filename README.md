# cdntest
自建测速站点
```
CloudflareST.exe -url https://cs.kjkkk.eu.org -sl 3 -tl 200 -dn 10
```
```
CloudflareST.exe -url https://testfiles.itkyou.cf/200mb.zip -dt 5
```
```
CloudflareST.exe -url https://testfiles.newbeer.gq/500mb.zip
```
```
CloudflareST.exe -url https://cf-speedtest.acfun.win/100mb.test
```
```
CloudflareST.exe -url https://uxuan.yohototo.top -sl 3 -tl 200 -dn 10
```

##　自建测速站worker代码
```
addEventListener("fetch", event => {
  let url = new URL(event.request.url);
  if (url.pathname == "/" && url.search == "") {
    url.href="https://cloudflare.cdn.openbsd.org/pub/OpenBSD/7.3/src.tar.gz"
    let request = new Request(url, event.request);
    event.respondWith(fetch(request));
  }
})
```

## [测速软件（win）2.2.4下载](https://github.com/XIU2/CloudflareSpeedTest/releases/tag/v2.2.4)
