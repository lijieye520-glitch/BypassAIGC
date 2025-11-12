# 更新日志 / Changelog

## [未发布] - 2025-11-12

### 新增功能 (Added)
- ✨ GitHub Actions 自动构建 Windows 可执行文件工作流
- 📦 PyInstaller 配置文件用于打包应用
- 🔧 本地构建脚本 (build.bat / build.sh)
- 📝 完整的构建文档 (BUILD.md)
- 🔐 .env.example 配置文件模板

### 改进 (Changed)
- 📚 更新 README.md，添加 Windows 可执行文件使用说明
- 🔒 添加 GitHub Actions workflow 的显式权限配置（安全性增强）
- 🚫 更新 .gitignore 以排除构建产物

### 安全 (Security)
- 🔐 修复 CodeQL 检测到的 GitHub Actions 权限问题
- ✅ 所有安全检查通过

### 技术细节 (Technical Details)
- **构建工具**: PyInstaller 6.0+
- **Python 版本**: 3.11
- **打包模式**: 单文件可执行文件
- **平台支持**: Windows (x64)
- **自动化**: GitHub Actions 自动构建和发布

### 文件清单 (File List)
- `.github/workflows/build-exe.yml` - GitHub Actions 工作流
- `backend/build.spec` - PyInstaller 配置
- `backend/build.bat` - Windows 构建脚本
- `backend/build.sh` - Unix/Linux 构建脚本
- `backend/requirements-build.txt` - 构建依赖
- `backend/BUILD.md` - 构建文档
- `backend/.env.example` - 配置模板

### 代码质量 (Code Quality)
- ✅ 已审查代码中的废弃模式
- ✅ Python 语法验证通过
- ✅ YAML 配置验证通过
- ✅ CodeQL 安全扫描通过
- ✅ 无需删除的旧代码（代码已经是最新的）

### 使用说明 (Usage)
1. **自动构建**: 推送到 main/master 分支或创建版本标签时自动触发
2. **手动构建**: 在 GitHub Actions 页面手动触发工作流
3. **本地构建**: 运行 `backend/build.bat` (Windows) 或 `backend/build.sh` (Unix/Linux)
4. **下载**: 从 GitHub Releases 或 Actions Artifacts 下载预构建的可执行文件

### 下一步 (Next Steps)
- ⏭️ 等待 GitHub Actions 首次构建完成
- ⏭️ 测试生成的可执行文件
- ⏭️ 创建第一个正式版本 (v1.0.0)
