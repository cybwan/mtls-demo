# mtls-demo

## 本地域名解析

```
echo 127.0.0.1 bookstore-v1.bookstore.cluster.local >> /etc/hosts
```

## 启动服务端

```
go run bookstore.go
```

## 启动客户端

```
go run bookbuyer.go
```

## 客户端回显

```
2022/06/26 15:08:46 Load key pairs -  ./certs/bookbuyer.crt ./certs/bookbuyer.key
Hello, world!
```

## 服务器端回显

```
(HTTPS) Listen on :8443
(HTTP) Listen on :8080
2022/06/26 15:08:46 >>>>>>>>>>>>>>>> Header <<<<<<<<<<<<<<<<
2022/06/26 15:08:46 User-Agent:Go-http-client/1.1
2022/06/26 15:08:46 Accept-Encoding:gzip
2022/06/26 15:08:46 >>>>>>>>>>>>>>>> State <<<<<<<<<<<<<<<<
2022/06/26 15:08:46 Version: 304
2022/06/26 15:08:46 HandshakeComplete: true
2022/06/26 15:08:46 DidResume: false
2022/06/26 15:08:46 CipherSuite: 1301
2022/06/26 15:08:46 NegotiatedProtocol: 
2022/06/26 15:08:46 NegotiatedProtocolIsMutual: true
2022/06/26 15:08:46 Certificate chain:
2022/06/26 15:08:46  0 s:/C=[]/ST=[]/L=[]/O=[Open Service Mesh]/OU=[]/CN=bookbuyer.bookbuyer.cluster.local
2022/06/26 15:08:46    i:/C=[US]/ST=[]/L=[CA]/O=[Open Service Mesh]/OU=[]/CN=osm-ca.openservicemesh.io
2022/06/26 15:08:46 >>>>>>>>>>>>>>>>> End <<<<<<<<<<<<<<<<<<
```

