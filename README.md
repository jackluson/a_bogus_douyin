# 抖音a_bogus算法

适用抖音，巨量百应等平台

## 验证(需梯子）

### post接口
设置参数
- url --- 你请求的url参数 // 不包含host、pathname
- ua -- 你的user_agent
- data -- post请求携带数据，get请求为空字符''

```shell
curl 'https://abogus.jackluson.workers.dev/' \
  -H 'Accept: application/json, text/plain, */*' \
  -H 'Accept-Language: zh-CN,zh;q=0.9,en;q=0.8,en-US;q=0.7,en-CA;q=0.6,la;q=0.5' \
  -H 'Cache-Control: no-cache' \
  -H 'Connection: keep-alive' \
  -H 'Content-Type: application/json' \
  -H 'Origin: https://abogus.jackluson.workers.dev' \
  -H 'Pragma: no-cache' \
  -H 'Referer: https://abogus.jackluson.workers.dev' \
  -H 'User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/123.0.0.0 Safari/537.36' \
  --data-raw '{"url":"source_type=force&request_from=&promotion_ids=3676740194222110808%2C3668960113932265483%2C3664932937922698950&verifyFp=verify_ltmpbxrc_yQud5ZMX_PB82_4ol7_8yt0_F4B9MKxKCHdU&fp=verify_ltmpbxrc_yQud5ZMX_PB82_4ol7_8yt0_F4B9MKxKCHdU&msToken=Ji2QTaG2qrt11TCxVRWTYuvnjY9t5csW-8j9jKrGHOsEfAjtqXAHG2s2SjUGCKNlU1RgJ0894AOFCeD6VSoLsJ1FLRplc-nGV0y-98P1ffrlAxDIj5GKt0crxaUJrA%3D%3D","data":"","ua":"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/123.0.0.0 Safari/537.36"}'
```

```python
import requests

data = {
    "url": "source_type=force&request_from=&promotion_ids=3676740194222110808%2C3668960113932265483%2C3664932937922698950&verifyFp=verify_ltmpbxrc_yQud5ZMX_PB82_4ol7_8yt0_F4B9MKxKCHdU&fp=verify_ltmpbxrc_yQud5ZMX_PB82_4ol7_8yt0_F4B9MKxKCHdU&msToken=mBCkvq8nLUXhJt-L37aQTvUaaKt0q4ISULVQ4kjBjkCDQPmkmJ5zHDlGTQRKFrcH_Wu5etCilD_BZTwmunLaOb-avwjv8608dGfJFtMjs4kDvE7PggYRg7EpkPZmQY0%3D",
    "data": "",
    "ua": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/121.0.0.0 Safari/537.36"
}

response = requests.post('https://abogus.jackluson.workers.dev/', json=data)
res_json = response.json()
print("res", res_json)
print(res_json.get('res').get('abogus'))

```

### 预设url
直接点击[https://abogus.jackluson.workers.dev/](https://abogus.jackluson.workers.dev/)
