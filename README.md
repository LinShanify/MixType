# MixType 中英混打

Mac 上的中英文混合输入法：拼音和英文连着打，不用按 Shift 切换。

可以当作 [UnimeType](https://unimetype.com/) 这类「免切换」多语言输入的离线平替：不靠云端 AI，不联网打字，不收集输入内容。

## 能做什么

- **免切换**：`zhege bug` → 这个bug；拼音出中文，英文单词保持英文
- **打错能纠**：`zhogn` → 中，`recieve` → receive；纠错后马上按删除键，退回你打的原样
- **英文撇号**：Today's、don't、I'm 直接打
- **选词和 macOS 自带拼音一样**：一行 9 个候选；↓ 展开成表格；← → 移动高亮，回车选中
- **越用越顺手**：词库里没有的英文词，你照原样打出三次，就记住并排第一；纠错被你退回两次，以后不再纠；同一串字母你连续三次选了别的候选，就把它排第一。学到的词在设置里标「自动」，可以删除，也可以整个关掉
- **自己的词库**：设置里加词、导入、导出。文件每行一个词：`词⇥拼音⇥!`（`!` 表示排第一）
- 目前只支持简体中文和英文

## 完全离线，数据自己掌握

- 打字、选词、词库全部在你的 Mac 上处理，不上传，没有账号，没有统计
- 自动学习只记单个词，不记句子；词库和学习记录都是普通文本文件，放在 `~/Library/Application Support/MixType/`，随时导出、备份、删除
- 唯一会联网的是检查更新：每天一次，只从本仓库下载更新文件，不发送任何输入内容；设置里可以关掉

## 安装

1. 在 [Releases](../../releases/latest) 下载最新的 `MixType-x.x.pkg`，双击安装（装到当前用户，不需要管理员密码）
2. 安装程序会自动添加输入法；如果菜单栏没有「混」，到 系统设置 → 键盘 → 输入法 里添加 MixType
3. 菜单栏「混」→「MixType 设置…」可以改标点、管理词库

如果提示「无法验证开发者」，右键安装包选「打开」。

## 更新

装好以后每天自动检查一次，有新版本在后台下载，输入法下次重启时装上（通常只下载一两百 KB 的补丁）。也可以在菜单栏「混」→「检查更新…」手动检查；两个开关都在设置里。

## 系统要求

macOS 12 或更高，Apple 芯片和 Intel 芯片都可以。

## 用到的开源项目

输入引擎 [librime](https://github.com/rime/librime) 与 librime-lua，自动更新 [Sparkle](https://sparkle-project.org)。词库来自 jieba、THUOCL、HanLP、SCOWL、Tatoeba、pinyin-data、phrase-pinyin-data，许可证随安装包附在 `MixType.app/Contents/Resources/SharedSupport/LICENSES/`。

---

**English**: MixType is a macOS input method for typing Chinese (pinyin) and English together without switching modes. It learns your words and picks over time, on your Mac only. Everything runs offline; the only network access is a daily update check against this repository, which can be switched off. macOS 12+, Apple silicon and Intel.
