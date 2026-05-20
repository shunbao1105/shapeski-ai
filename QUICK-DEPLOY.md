# ShapeSki AI - 极速部署指南（简化版）

## 方法一：Netlify Drop（30秒，推荐）

**1. 打开浏览器访问：**
```
https://app.netlify.com/drop
```

**2. 在页面中找到灰色区域**（中间大大的拖拽区域）

**3. 打开文件资源管理器：**
- Win+E 打开我的电脑
- 导航到：`C:\Users\44613\WorkBuddy\2026-05-20-task-1\`
- 找到 **index.html** 文件

**4. 拖入 Netlify 页面！**

**如果拖拽不行：**
- 页面底部有 **"Or click to upload"** 按钮
- 点击它，然后选择 index.html 文件

**5. 完成！获得在线链接**

---

## 方法二：Vercel 命令行（2分钟）

**第1步：安装（已安装请跳过）**
打开命令行（Win+R → 输入 cmd → 回车），运行：
```
npm install -g vercel
```

**第2步：登录**
```
vercel login
```
- 输入你的邮箱（163 邮箱即可）
- 去邮箱点击验证链接

**第3步：部署**
```
cd C:\Users\44613\WorkBuddy\2026-05-20-task-1
vercel --prod
```

- 提示 `Set up and deploy?` → 输入 Y 回车
- `Which scope?` → 选择你的账号
- `Link to existing project?` → 输入 N 回车
- `Project name?` → 输入 `shapeski-ai` 回车
- `Directory?` → 输入 `.` 回车
- `Override settings?` → 输入 N 回车

等待 30 秒左右，你会看到一个链接：`https://shapeski-ai.vercel.app`

---

## 方法三：QQ 邮箱直接分享

如果你只是想让人预览页面：

**1. 把 `shapeski-ai-site.zip` 解压到文件夹**

**2. 邮件发给朋友**（告诉他们打开 index.html 即可预览）

---

## 遇到问题？

| 问题 | 解决方法 |
|------|----------|
| Netlify 页面打不开 | 换个浏览器（Chrome）试试 |
| 拖拽没反应 | 用页面底部的 "click to upload" |
| Vercel 登录不了 | 用 GitHub 账号登录 vercel.com |
| 部署失败 | 把错误信息发给我 |

---

## 部署成功后下一步

1. 把链接发给我验证
2. 在微信/朋友圈/雪友群分享测试
3. 收集 10 个用户的反馈
4. 根据反馈迭代功能和定价
