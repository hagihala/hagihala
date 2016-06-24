```
W: GPG error: http://jp.archive.ubuntu.com xenial InRelease: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY 40976EAF437D05B5 NO_PUBKEY 3B4FE6ACC0B21F32
```

keyserver に鍵がある場合、以下のようにして取得すればいいらしい。どういうプロトコルか知らない。

```sh
 sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 40976EAF437D05B5 3B4FE6ACC0B21F32
```
