# DNShe域名配置指南 - 2026-01-30 03:05

## 准备工作
✅ 独立站MVP代码已开发
✅ Git仓库已初始化
⏳ 等待用户推送GitHub仓库
⏳ 准备DNShe域名配置

---

## GitHub Pages自定义域名步骤

### 步骤1：推送GitHub仓库
```bash
cd ~/clawd/feifei-resource-station
git remote add origin https://github.com/YOUR_USERNAME/feifei-resource-station.git
git branch -M main
git push -u origin main
```

### 步骤2：启用GitHub Pages
1. 打开仓库页面：https://github.com/YOUR_USERNAME/feifei-resource-station
2. 点击【Settings】标签
3. 滚动到【Pages】部分
4. 点击【Build and deployment】下的【Branch】选择：main
5. GitHub会自动构建，等待5-10分钟

### 步骤3：配置DNShe域名
1. 登录DNShe
2. 找到你的免费域名（或者申请新的免费域名）
3. 点击【域名解析】或【DNS管理】
4. 添加以下记录：

**如果使用主域名（例如：example.dnshe.com）：**
- 记录类型：CNAME
- 记录名称：@（留空）
- 记录值：YOUR_USERNAME.github.io

**如果使用子域名（例如：feifei.example.dnshe.com）：**
- 记录类型：CNAME
- 记录名称：feifei
- 记录值：YOUR_USERNAME.github.io

### 步骤4：等待DNS生效
- DNS生效时间：10分钟-24小时
- 可以通过`nslookup YOUR_USERNAME.github.io`检查是否生效

---

## 验证配置
### 等DNS生效后
1. 访问：https://feifei.example.dnshe.com（换成你的域名）
2. 应该显示霏霏数字资源站首页
3. 顶部状态：https://github.com/YOUR_USERNAME/feifei-resource-station/deployments

---

## 备注
⚠️ DNShe免费域名需要实名认证
⚠️ GitHub Pages免费域名：YOUR_USERNAME.github.io
⚠️ CNAME记录生效时间可能长达24小时

---

准备就绪！等待老板推送GitHub仓库后开始配置！💋
