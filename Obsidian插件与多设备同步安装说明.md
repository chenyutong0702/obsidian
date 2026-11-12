# Obsidian 插件与多设备同步 —— 安装说明（另一台电脑照做）

> 用途：当你换新电脑/平板，要把这个知识库（含下面 4 个插件）完整搬过去时，按本文操作。
> 仓库地址：`https://github.com/chenyutong0702/obsidian.git`

---

## 一、本库已装好的 4 个插件（会自动随仓库同步，不用从市场一个个搜）

| 插件 ID | 名称 | 版本 | 作用 | 特殊注意 |
|---|---|---|---|---|
| `obsidian-git` | Git | 2.43.0 | 多设备自动同步（commit/push/pull） | 同步核心，必启用 |
| `custom-sort` | Custom File Explorer sorting | 3.2.0 | 文件/文件夹自然数字排序 | 修复"12 去哪了"乱序 |
| `calendar` | Calendar | 1.5.10 | 日记日历视图（点日期写当天日记） | — |
| `execute-code` | Execute Code | 2.1.2 | 笔记里直接运行 Python 等代码块 | **仅桌面端能跑**，手机/平板只能看 |

> 插件文件都在仓库的 `.obsidian/plugins/` 里，已被 git 跟踪。新设备 clone 后文件就在本地，只需「启用」即可，不用重新下载。

---

## 二、另一台电脑（桌面端）安装步骤

### 第 1 步：装 Obsidian
- Windows / macOS：官网 https://obsidian.md 下载安装。
- 打开后**新建一个空仓库**（名字随意，比如 `obsidian`），先进入这个空仓库。

### 第 2 步：装 obsidian-git 插件（用来把云仓库搬下来）
1. 左下角「设置」→「社区插件」→ 关掉「安全模式」（或点「启用社区插件」）。
2. 点「浏览」→ 搜 **obsidian-git** → 安装并启用。
3. 打开命令面板（快捷键 `Ctrl/Cmd + P`，或左下角搜索图标）→ 搜 **`Git: Clone an existing remote repo`**。
4. 粘贴仓库地址：`https://github.com/chenyutong0702/obsidian.git`
5. 登录认证：用户名填你的 GitHub 账号，**密码填 PAT（个人访问令牌，不是账号密码）**。
6. 克隆完成后，仓库内容（笔记 + 4 个插件文件）就全部到本地了。

### 第 3 步：启用另外 3 个插件
1. 设置 →「社区插件」，你会看到列表里已经有 `custom-sort` / `calendar` / `execute-code`（因为文件随仓库下来了）。
2. 逐个把开关打开即可。
   - 若提示「插件未通过官方市场安装 / 是否信任」，点「信任并启用」。
3. 完成后 4 个插件全部启用，状态栏会出现 obsidian-git 的同步图标。

### 第 4 步：让 Execute Code 能真正跑 Python（桌面端可选）
- 在你这台新电脑上单独装 Python：官网 https://www.python.org → 安装时**务必勾选「Add Python to PATH」**。
- 装好后，笔记里 ` ```python ` 代码块旁会出现「运行」按钮，点一下就在本机运行。
- 手机/平板没有 Python 环境，那边只能看笔记、不能跑代码，属正常。

---

## 三、平板 / 手机安装步骤

1. 应用商店装 **Obsidian**。
2. 新建空仓库 → 同上方「第 2 步」装 obsidian-git 并 clone 同一个 GitHub 地址（用 PAT 登录）。
3. 同「第 3 步」启用 `custom-sort` / `calendar`（手机端也支持）。
4. **`execute-code` 在移动端无法启用/运行**（它是桌面专用插件），忽略即可，不影响其他功能。
5. 加日历面板：命令面板搜 **`Calendar: Open`**，把它固定到侧边栏（每台设备只需加一次，视图布局不随 git 同步）。

---

## 四、验证同步成功

- 在 A 设备改任意笔记/写一篇日记 → 等状态栏变绿（已自动 push）。
- 在 B 设备打开命令面板 → **`Git: Pull`**（或等自动拉取）→ 刚才的改动出现。
- 说明多设备同步已通。

---

## 五、重要提醒

- **GitHub 登录一律用 PAT（个人访问令牌）当密码**，不要用账号密码。
- 旧的明文 PAT（`ghp_bwz...`）曾暴露，**建议立刻去 GitHub → Settings → Developer settings → Personal access tokens 里 revoke 掉旧的**，重新 Generate new token（勾 `repo` 权限）再用。
- 遇到「同一篇笔记两边各改了」的冲突：obsidian-git 会弹窗让你选保留哪边/两边都留，按提示点即可，不必慌。
- 改完一台设备，等同步完成（状态栏变绿）再去碰另一台，可 99% 避免冲突。
