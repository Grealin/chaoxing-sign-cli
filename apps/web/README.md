# chaoxing-sign-ui

## 命令

- `pnpm install` ，安装依赖，如果时间太长请尝试挂代理或使用淘宝源。
- `pnpm serve` ，启动开发服务器，不要忘记把接口服务也运行起来。
- `pnpm build` ，构建项目，输出到 dist 文件夹。

## 配置

`src/config/api.ts` ：该文件中配置 `baseUrl` 变量为接口地址，默认 `http://localhost:5000` 。若接口部署在服务器，不要忘记将接口地址改为服务器IP或绑定的域名。

`src/pages/DashBoard/Helper.ts` ：若使用腾讯云的通用文字识别服务，二维码识别成功率极高，支持PNG、JPG、JPEG、PDF等格式，图片大小不能超过7M。查看此源码文件中的 parseEnc 函数，可注释掉默认函数，使用推荐函数，同时需要在 `apps/server` 项目中的 `env.json` 中配置 `secretId` 和 `secretKey`。

## 使用

### 添加用户
在首页，点击 ＋ 号按钮，输入手机号和密码即可登录，登陆成功后你的卡片将会出现在首页。

### 移除用户
右键你想要移除的用户卡片，点击移除。

### 手动签到
点击用户卡片，然后点击开始，根据提示签到即可。

### 配置监听
右键你想要配置的用户卡片，点击监听配置，在弹出的窗口中填写签到信息、邮件信息配置、QQ机器人配置，确认即可保存。保存后，即可点击卡片上的监听，运行监听模式。