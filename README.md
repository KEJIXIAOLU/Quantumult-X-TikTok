# Quantumult X 解锁 TikTok 代码

### 在 <code>[rewrite_local]</code> 中添加以下重写

    (?<=_region=)CN(?=&) url 307 JP
    (?<=&mcc_mnc=)4 url 307 2
    ^(https?:\/\/(tnc|dm)[\w-]+\.\w+\.com\/.+)(\?)(.+) url 302  $1$3
    (?<=\d\/\?\w{7}_\w{4}=)1[6-9]..(?=.?.?&) url 307 17
    
### 在 <code>[mitm]</code>  中添加

    hostname = *.tiktokv.com, *.byteoversea.com, *.tik-tokapi.com

## 换区
- 在  <code>[rewrite_local] </code> 中添加下句重写，并将JP改为想看的国家/地区的2位大写英文简写US（美国）｜KR（韩国）｜UK（英国）｜TW（台湾）

## 抖音无法观看
- 在hostname中加上以下兩條

      -*snssdk.com, -*amemv.com 
    
    
### 说明:
- 香港印度节点不可用，刷不出来，建议换节点 。
- 为什么要先卸载TikTok，TikTok会在第一次使用时触发限制，并导致之后无法通过MiMt解密
- 所以先配置好规则之后，然后在下载TikTok，减少重定向的请求次数，降低风险，延长规则的寿命
- 为什么配置好之后还是无法使用，请检查软件的证书有没有安装、信任
- 或者是Https解密（MiMt）与重写（Rewrite）有没有开启
- 或者是软件是不是盗版，比如用共享ID下载的Quantumult X，有设备限制，是无法使用重写脚本功能的
