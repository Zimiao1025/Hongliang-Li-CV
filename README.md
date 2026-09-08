# Hongliang Li — CV

这是一份可在 GitHub 和 Overleaf 同步维护的 XeLaTeX 简历。内容来自 `docs/Hongliang-CV.docx`，版式参考 `docs/Shuiabi_s_Resume_v13.pdf`。

## 更新简历

主要内容都在 [`main.tex`](main.tex) 中：

- 文件开头的 “Frequently edited details” 区域集中管理姓名、电话、邮箱和链接。
- 教育、经历、项目和论文可直接修改对应段落。
- Google Scholar 当前使用检索页作为临时链接；建议替换为你的公开个人主页 URL。
- OriBench 的 Platform 和 Documentation 尚未设置 URL；将链接填入 `\OriBenchPlatformURL` 和 `\OriBenchDocsURL` 即可。

## 在 Overleaf 编译

1. 新建 Overleaf 项目并导入此 GitHub 仓库，或上传仓库 ZIP。
2. 打开 **Menu → Settings → Compiler**，选择 **XeLaTeX**。
3. 主文件选择 `main.tex`，点击 **Recompile**。

项目包含 `.latexmkrc`，支持该配置的环境会自动使用 XeLaTeX。

## GitHub ↔ Overleaf 同步

Overleaf 的 GitHub 同步功能通常要求付费方案：在 Overleaf 项目中打开 **Integrations → GitHub**，授权 GitHub 后选择本仓库。此后可在 Overleaf 中 Pull/Push；它不是实时自动同步，操作前先 Pull，编辑完成后再 Push，以减少冲突。

如果账号没有 GitHub 集成功能，可使用 Overleaf 的 Git Bridge，或从 GitHub 下载 ZIP 后重新上传。

## 本地编译

安装 TeX Live（需包含 XeLaTeX 和 TeX Gyre 字体）后运行：

```bash
latexmk -xelatex main.tex
```

生成文件为 `main.pdf`。

## 文件说明

- `main.tex`：简历正文与样式
- `docs/`：原始 Word 内容及参考版式 PDF
- `.github/workflows/build.yml`：每次推送后自动检查 LaTeX 是否可编译，并上传 PDF 构建产物

