# 8 Ekonomi Token OXLY (Tokenomics) dan Proposisi Nilai

## 8.1 Parameter Dasar Token

### Ringkasan Metrik Utama

* **Supply Maksimal (Max Supply): 1.000.000.000** — OXLY (batas tetap dan permanen)
* **Supply Beredar saat TGE (Initial Circulating Supply): ≈ 0** — OXLY (tanpa alokasi pre-mint)
* **Alokasi Presale & Modal Ventura (VC): 0%** — Tanpa putaran pendanaan tertutup / private round
* **Alokasi Ekosistem & Komunitas: 65%** — Dari total supply

### Spesifikasi Teknis Token

| Parameter | Spesifikasi Protokol |
|---|---|
| Nama & Simbol Ticker | Oxly / **OXLY** |
| Standar Kontrak | BEP-20 pada jaringan BNB Smart Chain · 18 desimal · Mendukung standar otorisasi tanpa biaya gas EIP-2612 (`permit`) |
| Model Mint | Mint sesuai kebutuhan (on-demand minting) berdasarkan pos alokasi masing-masing, dikontrol secara ketat oleh smart contract yang menegakkan batas kuota dan jadwal vesting |
| Mekanisme Burn | Terbuka bagi siapa saja untuk melakukan burn atas saldo OXLY miliknya secara permanen; setiap eksekusi burn secara otomatis mengurangi `totalSupply()` dan mengakumulasi catatan pada variabel `totalBurned` |

### Prinsip Peluncuran (Fair Launch Manifesto)

{% hint style="info" %}
**No presale. No VCs. Fixed supply. Community-owned. Market-priced.**<br>Tanpa alokasi presale. Tanpa investor modal ventura. Supply maksimal tetap. Dimiliki oleh komunitas. Valuasi harga ditentukan sepenuhnya oleh mekanisme pasar.
{% endhint %}

## 8.2 Utilitas Ekosistem Token OXLY

| Kategori Utilitas | Mekanisme Penggunaan |
|---|---|
| **Diskon Biaya Trading** | Staking OXLY pada Oxly Gas Staking memberikan potongan biaya trading spot sebesar 5% hingga 100% pada jaringan BNB Smart Chain. |
| **Trading Tanpa Biaya Gas** | Staking OXLY pada Oxly Gas Staking menghasilkan alokasi kapasitas OXG untuk mengeksekusi transaksi trading di BNB Smart Chain tanpa memerlukan BNB; kapasitas OXG juga dapat didelegasikan kepada bot trading atau dompet sekunder. |
| **Imbal Hasil Staking (Yield)** | Pengguna memperoleh reward hingga 24% APY melalui kontrak Oxly Staking tanpa periode penguncian aset (no lock-up). |
| **Instrumen Pembayaran Listing** | Merupakan satu-satunya mata uang yang diterima untuk pengajuan listing token di ketiga jaringan utama dengan tarif sebesar 50.000 OXLY. |
| **Mata Uang Utama Oxly Live** | Digunakan sebagai biaya penyelenggaraan siaran Live Developer (15.000 OXLY), pengiriman apresiasi digital (gift), serta distribusi insentif kepada penonton valid dan host. |
| **Kompensasi Kekurangan Gas (OXG Shortfall)** | Berfungsi sebagai alat pembayaran otomatis apabila kapasitas OXG tidak mencukupi saat penempatan order, di mana seluruh OXLY yang dibayarkan akan di-burn secara permanen. |
| **Distribusi Airdrop** | Digunakan untuk distribusi alokasi bagi peserta program Fairlaunch. |

## 8.3 Sepuluh Keunggulan Struktural Token

1. ****Bebas Alokasi Orang Dalam (Zero Insider Allocation)**.** Tidak terdapat penjualan presale, putaran pendanaan tertutup (private round), maupun alokasi khusus bagi investor modal ventura (VC).
2. ****Batas Supply Maksimal Permanen**.** Total supply dikunci secara permanen pada angka 1.000.000.000 OXLY, yang ditegakkan oleh smart contract sebagai akumulasi mutlak dari seluruh pos kuota alokasi.
3. ****Tanpa Pre-Mint (Mint Berbasis Realisasi)**.** Supply beredar hanya bertambah ketika suatu alokasi benar-benar didistribusikan atau diklaim, sehingga menghilangkan risiko penumpukan dana treasury menganggur yang berpotensi dilepas ke pasar (dump).
4. ****Pemisahan Kuota On-Chain yang Ketat**.** Setiap pos alokasi memiliki batas kuota dan penghitung mint (mint counter) tersendiri di dalam kontrak, memastikan bahwa sub-alokasi ekosistem tidak dapat dicampur maupun dialihkan lintas pos.
5. ****Penguncian Jadwal Vesting Tim yang Tidak Dapat Ditembus**.** Kontrak minter untuk alokasi berjadwal dikunci secara permanen (immutable), sehingga jadwal vesting tidak dapat dipercepat atau dimodifikasi oleh pihak mana pun, termasuk pemilik (owner) kontrak.
6. ****Mekanisme Deflasi Berbasis Pendapatan Protokol**.** Sebesar 80% dari pendapatan biaya trading spot di ketiga jaringan dialokasikan untuk program buyback & burn, yang diperkuat oleh burn 50% biaya listing, sebagian biaya Live Developer, serta 100% pembayaran kekurangan OXG.
7. ****Penurunan Batas Supply Efektif secara Alami**.** Alokasi reward atau airdrop yang tidak diklaim hingga batas waktu berakhir tidak akan pernah di-mint, sehingga supply maksimal efektif hanya dapat bergerak turun di bawah batas 1 miliar token.
8. ****Permintaan Organik dari Seluruh Lini Produk**.** Aktivitas perdagangan spot, pengajuan listing, pemanfaatan kapasitas OXG, hingga ekosistem siaran Oxly Live secara langsung mendorong permintaan maupun penguncian token OXLY.
9. ****Distribusi Awal yang Adil (Merit-Based Distribution)**.** Porsi distribusi awal terbesar dialokasikan langsung kepada pengguna aktif berdasarkan kontribusi nyata melalui aktivitas trading, partisipasi sosial, dan program referral.
10. ****Transparansi On-Chain Menyeluruh**.** Metrik mint per alokasi, total token yang telah di-burn (`totalBurned`), dan supply beredar (`totalSupply`) dapat diverifikasi secara langsung dari smart contract, di mana setiap peristiwa burn dipublikasikan beserta hash transaksinya.
