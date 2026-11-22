# Catatan untuk Claude

Aplikasi ini satu file besar: `index.html` (~258 KB, ~200 fungsi JS). Jangan baca seluruh file.

## Cari kode lewat codebase-memory (hemat token)

Jika tool MCP `codebase-memory` tersedia, pakai itu dulu sebelum Read/Grep:

1. `index_repository` sekali per sesi jika project belum terindeks (`list_projects`).
2. `search_code` (teks, mis. `localStorage`) atau `search_graph` (nama fungsi) untuk menemukan lokasi.
3. `get_code_snippet` untuk membaca satu fungsi; `trace_path` untuk pemanggil/yang dipanggil.
4. Baru gunakan Read dengan `offset`/`limit` pada baris yang ditemukan bila perlu konteks lebih.

Jika tool itu tidak tersedia, pakai `grep -n` lalu Read per rentang baris, bukan seluruh file.
