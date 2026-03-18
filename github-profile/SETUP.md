# GitHub Profile README 使用说明

这里的文件是给你**复制到「与 GitHub 用户名同名的那个仓库」**用的，不是放在 GroovyGG 里。

## 1. 创建 Profile 仓库（若还没有）

- 仓库名 = 你的 GitHub 用户名（例如 `GroovyGG`）
- Public，勾选 Add README，创建

## 2. 复制文件到 Profile 仓库

- 把本目录下的 **README.md** 内容复制过去，替换该仓库的 README
- 把 **.github/workflows/waka-readme.yml** 整份复制到 profile 仓库的 `.github/workflows/` 下

## 3. 修改 README 里的占位

- 把 `GroovyGG` 换成你的 GitHub 用户名（若不同）
- 编辑 **Featured Projects**、**Currently Working On**、**Connect With Me** 里的链接和文案

## 4. 启用 WakaTime 周报（可选）

1. 注册 [WakaTime](https://wakatime.com)，在 [Account Settings](https://wakatime.com/settings/account) 拿到 **API Key**
2. 在 GitHub 创建 [Personal Access Token](https://github.com/settings/tokens)，勾选 `repo` 和 `user`
3. 在 **Profile 仓库** 的 Settings → Secrets and variables → Actions 里添加：
   - `WAKATIME_API_KEY` = 你的 WakaTime API Key
   - `GH_TOKEN` = 你的 GitHub PAT
4. 在编辑器/IDE 安装 [WakaTime 插件](https://wakatime.com/plugins)，开始写代码才会有数据
5. 到 Profile 仓库的 Actions 里运行一次 "Waka Readme" workflow，或等每天定时跑完，README 中的 `<!--START_SECTION:waka-->` 段会被自动替换成周报

## 5. Things I code with

README 里已放了一组 badge 示例，按需增删、替换成你的技术栈即可。

完成以上步骤后，访问 `https://github.com/你的用户名` 就能看到新主页。
