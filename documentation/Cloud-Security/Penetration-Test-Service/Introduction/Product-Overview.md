# 产品概述
渗透测试服务是对现有系统不造成任何损害的前提下，以攻击者视角，模拟黑客入侵的技术手段对用户指定系统进行全面深入的攻击测试，发现系统中潜在的风险威胁，帮助用户降低因黑客入侵带来的经济损失。


## 相关概念
京东云渗透测试服务能够为用户检测出系统中潜在的风险威胁，可覆盖常规的漏洞如下：

#### 信息泄露
•	常规信息泄露的自动化检测主要是针对某些已知的威胁类型进行的，如：返回的页面中包含路径信息、某目录存在匿名浏览目录、某文件存在自动备份文件等等。

•	某些信息泄露漏洞往往需要人工介入进行判断，如，返回信息中存在与目标系统业务具有极大相关性的数据，这些数据的泄露十分危险，但却无法被自动化扫描工具识别，需要人工对此类信息泄露进行挖掘和验证。

#### 注入漏洞
•	注入漏洞有多种注入方式，如：SQL 注入、XPath 注入、LDAP 注入等等。

•	不同类型的注入漏洞在利用方式和原理上是相似的，但后台存储的数据内容和用户权限决定了注入漏洞所能获得的收益大小。

•	测试人员手动测试注入漏洞时，除验证注入漏洞是否真实存在外，还需对该注入漏洞产生危害的深度与广度进行分析判断，并结合其影响为该注入漏洞设置合理的危险等级。

#### XSS与CSRF深度利用
•	多数 Web 扫描器对 XSS 与 CSRF 的识别与测试方式单一，一般情况下，扫描器只能从理论层面验证这类漏洞存在，但这类漏洞所带来的安全风险，需由人工辅助来完成鉴别与评估。

#### 重定向检测与利用
•	重定向漏洞往往与其他漏洞一起被结合利用。在传统的自动化评估过程中，难以对重定向漏洞进行识别和深度测试，但通过人工检测的方式，可对重定向漏洞的利用方式及其影响进行重新评估与定义。

#### 参数错误
•	参数错误分为多种类型，其中涉及到逻辑及权限的错误就难以通过扫描器实现自动识别，对这类错误，往往需要借助渗透工程师的丰富测试经验来进行识别和测试。

#### 认证错误
•	认证错误包含多层含义，最简单的理解便是用户登录入口暴露（尤其是敏感用户的登录入口，如：管理登录入口），且存在弱口令或暴力破解的可能（如：无验证码的登录页面即可借助暴力破解的方式通过验证）。除此之外，还有某些认证错误是自动化程序无法识别的，例如，登录某系统之后，不再对用户身份进行校验，用户在系统内进行任意操作，或是当用户修改口令时候不对原始口令进行校验，这些漏洞都可能导致普通用户的越权行为。



### 相关参考

 - [产品优势](../Introduction/Benefits.md)
 - [产品功能](../Introduction/Features.md)
 - [入门指南](../Getting-Started/Getting-Started.md)

### 计费

目前京东云漏洞扫描服务提供线下购买的方式。

详细说明请参见“[计费概述](../Pricing/Billing-Overview.md)”。详细收费标准请提交工单咨询