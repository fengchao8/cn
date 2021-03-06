# 入门指南

 为便于您快速开通、配置、启用安全加速服务，现对服务开通及配置说明如下：

   **第一步：开通安全加速服务**

  1、 进入安全客户控制台【实例列表】页面，
    根据实际业务情况选择套餐，购买安全加速实例。

   **第二步：添加安全加速域名**

  1、 进入安全加速客户控制台【域名管理】页面。

  2、 点击“添加域名”。

  3、 填写正确的域名信息，然后点击“确定”按钮。

  4、 访问安全加速【域名管理】可看到添加的域名成功。


  **第三步：绑定CNAME 验证TXT记录**

  1、 进入安全加速控制台【域名管理】页面，复制域名的CNAME。

  2、 登录域名DNS服务提供商控制台进行 CNAME 配置。

  CNAME绑定方法如下（以您的域名在京东与云云解析为例）：

  1）登录[京东云](https://www.jdcloud.com/index)，并进入[【域名服务-云解析】](https://dns-console.jdcloud.com/list)页面，点击需要绑定的域名。


  2）选中需要绑定的域名，点击“解析”，进入域名解析界面，点击“添加解析”，记录类型选择为“CNAME”，在记录值中填写京东云客户控制台为该域名分配的CNAME信息，格式为“xx.cdn.jdcloud-scdndns.com”，线路类型设为“默认”即可，然后保存。主机记录填写加速域名前缀，记录值填写加速域名对应的Cname。

  3、验证TXT记录，为了保证安全性，我们建议您验证TXT记录，复制【域名管理】中域名对应的TXT记录字段，在权威解析中增加TXT记录，用于验证域名的所有权。

  4、 修改DNS服务器需要0-72小时的生效时间，如果发现某些地方记录没有生效，并且修改DNS的时间不到72小时，请您耐心等待。

  **第四步：启用安全加速服务**

  域名审核通过后，服务配置会在15分钟后生效。

  在安全加速域名管理，点击域名进入域名解析配置页面，添加域名的源站记录。

  注：在进行切换操作时，建议先切换较小业务流量域名，再切换较大业务流量域名，谨慎操作，避免人为的操作失误。
