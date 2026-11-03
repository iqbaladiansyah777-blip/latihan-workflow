# Contributing Guide

## Branch Convention
Format: `<type>/<short-description>`

| Type | Kegunaan | Contoh |
| --- | --- | --- |
| `feature/` | Fitur baru | `feature/123-user-login` |
| `fix/` | Bug fix | `fix/cart-total` |
| `hotfix/` | Darurat production | `hotfix/payment-down` |
| `refactor/` | Refactor kode | `refactor/order-service` |
| `docs/` | Dokumentasi | `docs/api-reference` |
| `test/` | Test | `test/checkout-flow` |
| `chore/` | Maintenance | `chore/update-deps` |

**Aturan:**
- Huruf kecil semua
- Gunakan hyphen (-), bukan spasi
- Sertakan nomor tiket bila ada
- Maksimal 50 karakter

## Commit Convention
Format: `<type>(<scope>): <subject>`

**Type:** `feat`, `fix`, `docs`, `style`, `refactor`, `perf`, `test`, `build`, `ci`, `chore`, `revert`

**Contoh:**
- `feat(auth): add JWT refresh token`
- `fix(cart): correct total when discount applied`
- `docs(readme): update installation steps`

**Aturan:**
- Subject lowercase, imperative mood, tanpa titik
- Maksimal 50 karakter untuk subject
- Body dipisah 1 baris kosong
- Reference issue: `Closes #123`

## Pull Request
- Judul PR mengikuti format commit message
- Ukuran PR < 400 baris
- Wajib 1 reviewer approval
- Wajib lolos CI
- Gunakan Squash Merge

## Code Review
Label komentar:
- `blocking:` harus diperbaiki
- `nit:` saran kecil, opsional
- `question:` butuh klarifikasi
- `praise:` apresiasi

## Workflow
1. `git checkout main && git pull`
2. `git checkout -b feature/xxx`
3. Kerjakan, commit atomik
4. `git push -u origin feature/xxx`
5. Buat PR di GitHub
6. Tunggu review & CI
7. Squash merge
8. Hapus branch

## Yang Dilarang
- Push langsung ke `main`
- Commit message tidak jelas (`wip`, `test`, `asdf`)
- Commit file `.env`, `node_modules/`, credentials
- Rebase branch yang sudah di-push & dipakai orang lain