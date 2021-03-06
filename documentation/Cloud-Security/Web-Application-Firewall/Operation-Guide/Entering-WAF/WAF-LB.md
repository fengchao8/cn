## **WAF源站负载均衡**

  如果您的源站有多个服务器，在将域名接入WAF时，您可以配置多个源站IP。WAF支持最多20个源站IP。

如果您配置了多个源站IP，WAF在将过滤后的访问请求回源时，将按照IP Hash或轮询的方式去做负载均衡。同时，WAF也会对多个源站进行健康检查，对所有回源IP进行接入状态检测，如果某个回源IP没有响应，将不再将请求转发到这个回源IP，直到其接入状态回复正常。

假设源站IP有3个（1.1.1.1、2.2.2.2、3.3.3.3），您可以按照下图所示进行配置。

**说明：** 如果WAF前面已使用代理（如CDN、DDOS之类的服务），务必勾选**是否已使用代理**下的**是**。

否则，配置完成

![img](https://github.com/jdcloudcom/cn/blob/edit/image/waf-img/WAF%E6%BA%90%E7%AB%99%E8%B4%9F%E8%BD%BD%E5%9D%87%E8%A1%A1-1.png)

添加源站IP后，您需要指定负载均衡算法：IP hash、轮询。
