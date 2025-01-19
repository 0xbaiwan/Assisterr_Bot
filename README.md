# [Assisterr Bot](https://github.com/0xbaiwan/Assisterr_Bot)
自动为assisterr.ai签到获取每日积分，支持多账户和代理使用

## 所需工具和组件
1. 注册: [https://build.assisterr.ai](https://build.assisterr.ai/?ref=677ac8bd0fed0714db3d6dc7) (连接Twitter、Discord并完成任务)
2. 代理 (可选)
3. VPS或RDP (可选)
4. NodeJS 安装指南：
   - Linux用户参考 [这里](https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-22-04)
   - Windows用户参考 [这里](https://www.youtube.com/watch?v=La6kH33-AVM&ab_channel=TheCodeCity)
   - Termux用户参考 [这里](https://www.youtube.com/watch?v=5NceYSU4uFI&ab_channel=VectorM%3A)

### 购买代理
- 免费静态住宅代理：
   - [WebShare](https://www.webshare.io/?referral_code=gtw7lwqqelgu)
   - [ProxyScrape](https://proxyscrape.com/)
   - [MonoSans](https://github.com/monosans/proxy-list)
- 付费高级静态住宅代理：
   - [922proxy](https://www.922proxy.com/register?inviter_code=d6416857)
   - [Proxy-Cheap](https://app.proxy-cheap.com/r/Pd6sqg)
   - [Infatica](https://dashboard.infatica.io/aff.php?aff=580)

## 凭证设置

### 获取凭证
1. 获取Solana钱包私钥：
   - 使用 [Phantom钱包](https://www.youtube.com/watch?v=xS5VllDRyMc)
   - 使用 [Soflare](https://www.youtube.com/watch?v=HYNKAhQjwLU)，然后使用 [此脚本](https://gist.github.com/im-hanzou/bb5569806875168b47458a56334bbe60) 转换私钥
2. 获取账户令牌：
   - 打开 [https://build.assisterr.ai](https://build.assisterr.ai/?ref=677ac8bd0fed0714db3d6dc7) 并确保已登录并完成任务
   - 按F12或Ctrl+Shift+I打开浏览器开发者工具，导航到控制台选项卡
   - 运行以下命令：
```bash
function getCookieValue(cookieName) {
    const cookies = document.cookie.split('; ');
    for (let cookie of cookies) {
        const [name, value] = cookie.split('=');
        if (name === cookieName) {
            return decodeURIComponent(value);
        }
    }
    return null
}
const accessToken = getCookieValue('accessToken');
const refreshToken = getCookieValue('refreshToken');
console.log('Access Token:', accessToken);
console.log('Refresh Token:', refreshToken);
```
3. 将凭证按以下格式插入到``accounts.txt``：
```bash
accessToken:refreshToken:privatekey
```
> 如果运行多个账户，请每行插入一个
4. 将代理按以下格式插入到``proxies.txt``：
```bash
http://127.0.0.1:8080
http://user:pass@127.0.0.1:8080
```
> 目前仅支持http代理

## 模块安装
- 手动下载脚本 [点击这里](https://github.com/0xbaiwan/Assisterr_Bot/archive/refs/heads/main.zip) 或使用git：
```bash
git clone https://github.com/0xbaiwan/Assisterr_Bot
```
- 打开终端并确保在机器人文件夹中：
```bash
cd Assisterr_Bot
```
- 安装模块：
```bash
npm install
```
- 运行机器人：
```bash
node index.js
```

## 购买代理（可选）

- 免费静态住宅代理：
   - [WebShare](https://www.webshare.io/?referral_code=gtw7lwqqelgu)
   - [ProxyScrape](https://proxyscrape.com/)
   - [MonoSans](https://github.com/monosans/proxy-list)
- 付费高级静态住宅代理：
   - [922proxy](https://www.922proxy.com/register?inviter_code=d6416857)
   - [Proxy-Cheap](https://app.proxy-cheap.com/r/Pd6sqg)
   - [Infatica](https://dashboard.infatica.io/aff.php?aff=580)
