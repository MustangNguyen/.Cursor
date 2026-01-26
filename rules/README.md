# Unity Rules - Optimized Version

## 📊 Token Savings

**Trước:** 10 files, ~15,000-20,000 tokens  
**Sau:** 4 files, ~5,000-7,000 tokens  
**Tiết kiệm:** ~65-70% tokens

## 📁 Cấu trúc Rules

### Core Rules (4 files)

```
rules/
├── 00-overview.mdc              # Project overview & architecture
├── 01-scripts.mdc               # C# scripts + No Fallback principle
├── 02-assets-performance.mdc    # Assets import + Performance optimization
└── 03-workflow.mdc              # Debug + MCP + Git + Comments + Testing + Build
```

### Backup (11 files cũ)

```
rules/.old-backup/
├── 00_unity-project-overview.mdc
├── 01_unity-script-standards.mdc
├── 01a_no-fallback-game-logic.mdc
├── 02_unity-asset-standards.mdc
├── 03_unity-performance-standards.mdc
├── 04_unity-testing-standards.mdc
├── 05_unity-build-standards.mdc
├── 06_unity-debug-standards.mdc
├── 07_mcp-priority-standards.mdc
├── 08_git-commit-standards.mdc
└── 09_better-comments-standards.mdc
```

## 🎯 Nguyên tắc tối ưu

### 1. Gộp files liên quan
- **Scripts:** Gộp 01 + 01a (No Fallback vào Scripts)
- **Assets/Performance:** Gộp 02 + 03 (cùng về optimization)
- **Workflow:** Gộp 04 + 05 + 06 + 07 + 08 + 09 (cùng về quy trình làm việc)

### 2. Principle over Example
- **70% principles, 30% examples**
- Chỉ giữ ví dụ quan trọng nhất
- Loại bỏ ví dụ lặp lại

### 3. Metadata tối giản
```yaml
---
id: unity-scripts
alwaysApply: true
priority: 20
globs: ["**/*.cs"]
---
```

### 4. DRY (Don't Repeat Yourself)
- Không lặp lại Best Practices
- Link tham chiếu thay vì copy/paste
- Tập trung vào core principles

## 📚 Nội dung từng file

### 00-overview.mdc
- Cấu trúc thư mục project
- Naming conventions (C#, Assets)
- Kiến trúc (DI, Event, State Machine)
- Domain separation

### 01-scripts.mdc
- Cấu trúc script chuẩn
- Quy tắc đặt tên chi tiết
- Performance (cache, reuse, pooling)
- **NO FALLBACK principle** (Fail Fast)
- Checklist refactor

### 02-assets-performance.mdc
- Import settings (Texture, Model, Audio)
- Asset organization
- Performance targets (FPS, Draw calls, Memory)
- CPU/Memory/Graphics optimization
- Pooling systems (Object, Audio)
- Data-driven levels

### 03-workflow.mdc
- **Debug:** IDebugLogger, tag format, define symbols
- **MCP Tools:** Priority list, Unity MCP operations
- **Git:** Commit types, format, best practices
- **Comments:** Better Comments tags (!, ?, //, todo, *, ^)
- **Testing:** Unit/Integration/Performance tests
- **Build:** CI pipeline, versioning

## 🔄 Migration từ Rules cũ

Nếu cần rollback về rules cũ:

```bash
# Xóa rules mới
rm 00-overview.mdc 01-scripts.mdc 02-assets-performance.mdc 03-workflow.mdc README.md

# Restore rules cũ
cd .old-backup
move *.mdc ..
cd ..
rmdir .old-backup
```

## ✅ Checklist sử dụng

- [ ] Đọc `00-overview.mdc` để hiểu tổng quan project
- [ ] Tham khảo `01-scripts.mdc` khi viết C# code
- [ ] Check `02-assets-performance.mdc` khi import assets hoặc optimize
- [ ] Follow `03-workflow.mdc` cho debug, git, comments, testing

## 📝 Notes

- **Always Apply:** Tất cả rules có `alwaysApply: true`
- **Priority:** 00 (10) > 01 (20) > 03 (25) > 02 (30)
- **Language:** Tiếng Việt
- **Format:** Markdown với YAML frontmatter

---

**Version:** 2.0 Optimized  
**Last Updated:** 2026-01-26  
**Author:** AI Assistant with devgo2003
