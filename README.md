# DraftPilot — Releases

Kênh phát hành **DraftPilot** (tự động hoá làm video CapCut: AI script → ảnh AI → TTS → ráp draft).

- **Mã nguồn**: riêng tư tại [`scodevn2025/draftpilot`](https://github.com/scodevn2025/draftpilot).
- **Repo này** (public) chỉ chứa file phát hành để app tự cập nhật:
  - [`version.json`](version.json) — phiên bản mới nhất + link installer + ghi chú.
  - Installer `.exe` đính kèm trong [Releases](https://github.com/scodevn2025/draftpilot-releases/releases).

## App tự cập nhật thế nào

1. Mở app → bấm logo **DraftPilot** (góc trái) → hộp **Giới thiệu**.
2. Bấm **Kiểm tra cập nhật**. App đọc `version.json` ở repo này.
3. Nếu có bản mới → bấm **Cập nhật ngay**: app tải installer về rồi chạy. Đóng app để cài đè.

App cũng tự kiểm tra lặng lẽ mỗi lần khởi động; có bản mới sẽ hiện chấm **Bản mới** cạnh số phiên bản.

## Phát hành bản mới (cho tác giả)

1. Bump version ở `src/lib/version.ts`, `src-tauri/tauri.conf.json`, `src-tauri/Cargo.toml`.
2. `npx tauri build` → `src-tauri/target/release/bundle/nsis/DraftPilot_<ver>_x64-setup.exe`.
3. `gh release create v<ver> <installer> -R scodevn2025/draftpilot-releases`.
4. Cập nhật `version.json` (version + url tag mới) rồi push lên `main`.

---

© 2026 ScodeVN · github.com/scodevn2025
