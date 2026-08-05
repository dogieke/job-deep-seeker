# 简历模板包（resume-modern）

> **来源**：基于 [Open Design](https://github.com/nexu-io/open-design)（nexu-io，Apache-2.0）的官方 `resume-modern` 模板 + 6 个设计系统（风格），已脱敏并占位符化。**版权说明见文末。**

## 模板 + 风格分离（核心设计）

**模板与风格是两层，用户先选模板再选风格：**

```
① 选模板：resume-modern（本包，唯一的简历模板）
② 选风格：styles/ 目录下的 6 种风格（苹果/极简/小红书/复古/商务/创意）
③ 组合：模板结构 + 所选风格的令牌（颜色/字体）→ 生成简历
```

**默认 = 苹果风**（resume.html 已内置）；用户可换风格（见下）。

## 风格可选层（styles/）

| 风格 | 文件 | 特征 |
|---|---|---|
| **apple**（默认） | apple-DESIGN.md + tokens.json + tokens.css | 黑白灰+蓝 accent、SF Pro、大留白 |
| **minimal** | minimal-* | 极简、白底黑字、克制 |
| **xiaohongshu** | xiaohongshu-* | 小红书风、年轻化 |
| **retro** | retro-* | 复古、暖色 |
| **enterprise** | enterprise-* | 商务、稳重 |
| **creative** | creative-* | 创意、大胆 |

**换风格方法**：把 `styles/{风格}-tokens.css` 的 CSS 变量应用到 resume.html（替换颜色/字体），结构不动。
**更多风格**：Open Design 官方有 152 个设计系统（https://github.com/nexu-io/open-design/tree/main/design-systems），可按需下载 `DESIGN.md + design-tokens.json + tokens.css` 三个文件放进 styles/。

## 模板策略（必读）

**先问用户，二选一：**
1. **默认模板**（推荐）：直接用 `resume.html` 结构+苹果风，只填占位符
2. **自定义偏好**：用户提视觉风格/布局偏好 → 在模板基础上调整（换风格/栏目）

```
用户偏好确认流程：
① 问用户：用「默认模板」还是「自定义偏好」？
② 默认 → 用 resume.html，填占位符
③ 自定义 → 问风格（苹果/极简/小红书/复古/商务/创意）→ 套用对应 tokens.css → 调整布局
④ 内容永远按用户提供的真实素材组织（不虚构、不拼装）
```

## 文件清单

| 文件 | 说明 |
|---|---|
| `resume.html` | **默认模板**（A4 单页、苹果风、占位符版） |
| `SKILL.md` | Open Design 官方 resume-modern 模板规范 |
| `styles/` | 6 个风格（各含 DESIGN.md + tokens.json + tokens.css） |
| `style-apple.json` | Apple 风格令牌（与 styles/apple-tokens.json 等价，旧版保留） |
| `photo.jpg` | **占位头像**（几何抽象图，非真人；仅供展示头像位置。用户替换为自己的照片——**必须同名覆盖本文件**，resume.html 用相对路径引用）；**用户无照片/不想放 → 删除 header 里的照片块**（`.header-photo` div），布局自动适应 |

## 使用流程

1. 用户提供信息（姓名/学校/邮箱/城市/电话/经历/项目/技能）
2. 确认模板 + 风格
3. 按模板结构组织内容（Header → 教育 → 项目 → 经历 → 技能）
4. **内容纪律**：只用真实素材（用户确认），不虚构、不拼装
5. 导出 PDF（HTML → 单页 A4，方案 agent 自选）

## 版权

- **Open Design**：模板结构与 SKILL.md 来自 [nexu-io/open-design](https://github.com/nexu-io/open-design)，**Apache-2.0 许可证**
- **6 个风格**：提取自 Open Design design-systems 目录（Apple/小红书等商标归原公司），仅供简历视觉参考
- 本项目衍生使用，遵守 Apache-2.0；若开源本 skill 包，保留上述来源声明
