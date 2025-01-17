本文档将为您详细介绍如何将腾讯云漏洞扫描服务的监测 IP 加入到白名单。
## 操作场景

漏洞扫描服务通过公网进行资产发现和风险监测时会使用模拟黑客入侵攻击的方式。如果您的服务器有安全防护或监控部署（例如 WAF、SOC），建议您将腾讯云漏洞扫描服务的监测 IP 加入到白名单中，开启扫描访问权限，保证监控服务正常运行，漏洞扫描服务扫描节点 IP 为：
129.211.162.110
129.211.162.87
129.211.163.253
129.211.164.19
129.211.166.123
129.211.167.182
129.211.167.200
129.211.167.70
129.211.162.158
129.211.162.23
129.211.166.134
129.211.167.108
129.211.167.181
129.211.166.142
129.211.166.163
129.211.167.128
129.211.167.166
若您的网站需登录才可以访问，则需要先解除安全策略（即确保所有 IP 都能访问），待您的 cookie 有效性验证通过后再恢复限制。  

## 操作步骤

### 方式1：通过 IP 查询添加白名单

1. 登录 [Web 应用防火墙控制台](https://console.cloud.tencent.com/guanjia/tea-overview)，在左侧导航中，选择**IP 管理** > **IP 查询**，进入 IP 查询页面。
2. 在 IP 查询页面，输入需要查询的 IP 地址，单击**查询**，将展示查询结果。
![](https://main.qcloudimg.com/raw/c2679f4a5009dc7ba837df1308c7fd14.png)
3. 单击**加入黑白名单**，进入“添加黑白 IP” 页面，可手动添加白名单。类别选择“白名单”，IP 地址填写需要添加到白名单的地址，选择白名单有效期的截止时间，设置完成后，单击**添加**，即完成白名单添加。
![](https://main.qcloudimg.com/raw/a1438e6e8acd1f32cc23e388e3809e53.png)

### 方式2：直接添加 IP 白名单
登录 [Web 应用防火墙控制台](https://console.cloud.tencent.com/guanjia/tea-overview)，在左侧导航中，选择**IP 管理**>**IP 黑白名单**，进入 IP 黑白名单页面。
- **方式1**：手动添加白名单。
 1. 在 IP 黑白名单页面，单击**添加黑白名单**，将弹出“添加黑白IP”窗口。
 2. 在“添加黑白 IP”窗口中，类别“白名单”类别，将漏洞扫描服务扫描节点 IP 复制到 IP 地址的输入框内，选择白名单有效期的截止时间，设置完成后，单击**添加**，即完成白名单添加。
>?最多支持输入100个 IP 地址，多个 IP 地址以换行分隔。
>
![](https://main.qcloudimg.com/raw/e2607fd01aee22e84a6f3bdef994ae66.png)
- **方式2**：批量导入白名单。
	1. 在 IP 黑白名单页面，单击**导入数据**，将弹出“导入 IP 名单”窗口。
	2. 在“导入 IP 名单”窗口中，单击**导入**，选择导入白名单文件，上传完成后，单击**确认导入**即可。
>?
>- 导入文件格式：仅支持.xlsx、.xls。
>- 数量：目前只支持单个文件上传。
>- 内容：必须包含类别，IP 地址，截止时间三列，具体可参考导出数据 excel 格式。
>- 截止时间，必须在2033/12/30 23:59:59之前，格式 YYYY/MM/DD HH:MM:SS。
>
	![](https://main.qcloudimg.com/raw/4e49d6eaf18ee86ae033f8aab2f6e7d2.png)
	
### 方式3：将已封堵 IP 添加白名单
1. 登录 [Web 应用防火墙控制台](https://console.cloud.tencent.com/guanjia/tea-overview)，在左侧导航中，选择**IP 管理** > **IP 封堵状态**，进入 IP 封堵状态。
2. 在 IP 封堵状态页面，输入相关信息，单击**查询**，可以查询漏洞扫描服务的相关 IP 信息，即可对已封堵 IP 进行加白操作。
![](https://main.qcloudimg.com/raw/e53da351484d70107246eb1e8c6f641a.png)
