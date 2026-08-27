# Buku Konsep Jaringan Komputer — TI043102 (PENS)

Modul ajar Markdown yang mengikuti **RPS Konsep Jaringan (TI043102)**, D4 Teknik Informatika PENS.

## Isi paket (batch 1)

| File | Bab | Isi |
|---|---|---|
| `00-pengantar-dan-peta-rps.md` | — | Kata pengantar, peta RPS→bab, pemetaan CPMK/CPL, daftar pustaka master |
| bab-01-pengantar-jaringan-internet.md| 1 | Definisi, LAN/MAN/WAN, metrik kinerja, sejarah, tata kelola |
| `bab-02-model-osi-tcpip.md` | 2 | Model berlapis, OSI vs TCP/IP, **enkapsulasi** (CPMK-3) |
| `bab-03-physical-layer.md` | 3 | Sinyal, Nyquist/Shannon, encoding, media transmisi |
| `bab-04-data-link-layer.md` | 4 | Framing, MAC, switch, **ARP**, **VLAN 802.1Q**, Wi-Fi |
| `bab-05-network-layer-ip.md` | 5 | Header IPv4, pengalamatan, CIDR, ICMP, **IPv6** |
| `bab-06-ip-subnetting.md` | 6 | Meminjam bit, rumus, **VLSM**, subnetting IPv6 |
| `bab-07-static-routing.md` | 7 | Konsep routing, tabel routing, **static route**, default gateway |
| `bab-08-dynamic-routing.md` | 8 | **DV vs LS** (RIP/OSPF), IGP/EGP, BGP, konvergensi |
| `bab-09-transport-tcp.md` | 9 | Port, **3-way handshake**, keandalan, flow/congestion control |
| `bab-10-transport-udp.md` | 10 | UDP (header 8 byte), TCP vs UDP, **DHCP DORA** |
| `bab-11-application-layer.md` | 11 | Client-server, **HTTP**, **DNS**, SMTP/SSH, socket |
| `bab-12-advanced-terkini.md` | 12 | **Capstone**: peta teknologi 2026 per layer, PQC, Ultra Ethernet |
| `asset/*.svg` (11 gambar) | — | Gambar 2.1–12.1 (native) |
| `asset/osi-tcpip-stack.svg` | — | Gambar 2.1 (native) |
| `asset/enkapsulasi.svg` | — | Gambar 2.2 (native) |

## Status pengerjaan

- ✅ **Batch 1:** Front matter + Bab 1–3
- ✅ **Batch 2:** Bab 4 (Data Link/VLAN), 5 (Network/IP), 6 (Subnetting) — selaras **RPS terkoreksi**
- ✅ **Batch 3:** Bab 7 (Static Routing), 8 (Dynamic Routing), 9 (TCP)
- ✅ **Batch 4:** Bab 10 (UDP), 11 (Application Layer), 12 (Advanced/Terkini)
- ✅ **BUKU LENGKAP — Bab 1–12 selesai.**

Buku sengaja dibangun **bertahap per batch** demi menjaga kedalaman tiap bab (satu buku jaringan lengkap = ratusan halaman; menulis sekaligus mengorbankan mutu).

## Cara render diagram

Diagram memakai **Mermaid** (mindmap, flowchart, sequence, timeline). Ter-render otomatis di:
- **GitHub** (langsung di preview `.md`)
- **VS Code** + ekstensi *Markdown Preview Mermaid Support*
- **Obsidian**, **Typora**

> Catatan: tipe `mindmap` & `timeline` butuh Mermaid ≥ v9.4. Bila viewer lama, upgrade ekstensi. Gambar `.svg` di `asset/` render di browser & GitHub.

## Konversi ke PDF/DOCX

Markdown murni + Mermaid → bisa diproses dengan pipeline yang sudah dipakai (pandoc / soffice). Untuk PDF dengan Mermaid ter-render, gunakan `mermaid-cli` (mmdc) untuk pra-render diagram ke SVG/PNG sebelum pandoc, atau ekspor dari VS Code.

## Prinsip penyusunan (di-flag eksplisit)

- Konten teknis diturunkan dari **sumber terverifikasi** (Forouzan, Tanenbaum, Kurose–Ross, Cisco CCNAv7, MIT OCW, RFC).
- Bagian **"Teknologi Internet Terkini"** = snapshot **Agustus 2026** (diverifikasi via web); angka adopsi bergerak → **verifikasi ulang** sebelum dipakai resmi.
- **Tidak ada IK** yang diarang (RPS TI043102 tak punya layer IK).
- Gambar SVG **orisinal/native**, bukan salinan figur ber-hak cipta.
- Beberapa **tension pemetaan RPS** (drift kolom mingguan; VLAN di Minggu 3) di-*surface*, bukan ditutupi.
