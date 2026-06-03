name: 歪麦霸王餐跳转拦截名称：歪麦霸王餐跳转拦截
type: rewrite类型：重写
rules:规则：
# 拦截广告域名
- DOMAIN-SUFFIX,ad,REJECT
- DOMAIN-SUFFIX,ads,REJECT
- DOMAIN-SUFFIX,adx,REJECT
- DOMAIN-SUFFIX,promo,REJECT
# 网页跳转淘宝/抖音/京东/拼多多拦截
- REWRITE,^https?://.*\.taobao\.com.*,REJECT-重写，^https?://.*\.taobao\.com.*,拒绝-重写，^https?://.*\.taobao\.com.\.淘宝\.com.*,拒绝
- REWRITE,^https?://.*\.douyin\.com.*,REJECT-重写，^https?://.*\\.douyin\\.com.*,拒绝-重写，^https?://.*\.douyin\.com.*,拒绝
- REWRITE,^https?://.*\.jd\.com.*,REJECT-重写，^https?://.*\.jd\.com.*,拒绝-重写，^https?://.*\.jd\.com.*,拒绝-重写，^https?://.*\\.jd\\.com.*,拒绝-重写，^https?://.*\.jd\.com.*,拒绝
- REWRITE,^https?://.*\.pinduoduo\.com.*,REJECT-重写，^https?://。*\.pinduoduo\.com。*,拒绝
