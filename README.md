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
- 在 <code>[mitm]</code> hostname后加上以下代码

      -*snssdk.com, -*amemv.com

    
    
### 说明:
- 香港印度节点不可用，刷不出来，建议换节点 。
- 建议看完视频，并按照视频步骤来操作
