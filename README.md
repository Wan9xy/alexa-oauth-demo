
### Web App
需要您自行准备https域名及证书，并且使用nginx或caddy等程序代理443端口转发到您的程序中，
程序默认运行在3000端口，如果您想要更改端口，请在程序中修改

 - `sudo apt-get update`
 - `sudo apt-get upgrade -y`
 - `sudo apt-get install -y mongodb`
 - `curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -`
 - `sudo apt-get install -y nodejs`
 - `cd alexa-oauth-test`
 - `node index.js`


访问 [[your_ip_address:3000]](:3000) 查看结果,
最后您可以编辑目录中的
 `create-oauth-application.sh`里的账号和密码来注册设备.


 - `./create-oauth-application.sh`


### Alexa Skill


下方是对应skill auth需要填写的数据，您可以在您的skill中查看。 
 - Authorization URL -> https://[domain name]/auth/start
 - ClientId -> 2
 - Scope "access_devices"
 - Access Token URI -> https://[domain name]/auth/exchange
 - Client Secret -> "password"
 - Client Authentication Scheme -> "Credentials in request body" 

