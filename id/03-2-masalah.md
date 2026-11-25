# 2 Masalah

## 2.1 Risiko Kustodian pada Bursa Terpusat (Centralized Exchange)

Bursa terpusat (centralized exchange / CEX) memang menawarkan likuiditas order book yang dalam dan eksekusi berkecepatan tinggi, tetapi mewajibkan pengguna menyetorkan aset ke dompet yang dikendalikan sepenuhnya oleh operator bursa. Sentralisasi penyimpanan aset ini menciptakan titik kegagalan tunggal (single point of failure) yang menjadi target utama peretasan di industri kripto:

* **Februari 2025 · Bybit: $1,5 Miliar** — Peretasan cold wallet yang mengakibatkan pencurian aset ETH senilai $1,5 miliar [1].
* **Sepanjang 2025 · Akumulasi Industri: $2,7 Miliar** — Rekor total nilai aset kripto yang hilang akibat insiden peretasan sepanjang tahun [2].
* **29 Oktober 2026 · Binance: $6,3 Miliar** — Insiden keamanan terbesar yang pernah tercatat; berdampak pada aset klien serta memaksa penghentian layanan deposit dan penarikan [3][4].

Dalam seluruh insiden tersebut, pengguna tidak memiliki kendali langsung atas pemulihan aset mereka. Keputusan mengenai pembekuan, kerugian, maupun kompensasi dana sepenuhnya bergantung pada kebijakan internal operator bursa. Selain itu, pengguna tidak dapat memverifikasi secara real-time bahwa saldo mereka didukung oleh cadangan penuh (full reserve). Prinsip "Not your keys, not your coins" bukan sekadar slogan komunitas, melainkan refleksi dari risiko struktural yang nyata.

{% hint style="info" %}
**Solusi Arsitektur Oxly:** Protokol Oxly mengeliminasi keberadaan dompet terpusat yang rentan terhadap peretasan. Seluruh dana pengguna tetap berada di dalam dompet mandiri (self-custodial wallet) masing-masing atau terkunci secara terisolasi pada smart contract escrow untuk order aktif, dan dapat ditarik kapan saja cukup dengan membatalkan order terkait.
{% endhint %}

## 2.2 Keterbatasan Struktural DEX Berbasis Liquidity Pool (AMM) bagi Trader

Sebagian besar aktivitas perdagangan terdesentralisasi saat ini beroperasi melalui mekanisme Automated Market Maker (AMM). Meskipun AMM memfasilitasi perdagangan tanpa perantara (permissionless), arsitekturnya memiliki keterbatasan mendasar bagi kebutuhan trader aktif maupun institusional:

* **Ketiadaan Limit Order Bawaan.** Trader tidak dapat menempatkan order pada titik harga spesifik dan menunggu hingga order tersebut terisi secara otomatis oleh pasar.
* **Penentuan Harga Bergantung pada Kurva Pool.** Harga eksekusi ditentukan oleh rasio likuiditas di dalam pool, bukan oleh kesepakatan langsung antar-trader. Akibatnya, transaksi bervolume besar rentan mengalami slippage yang signifikan.
* **Absennya Transparansi Order Book.** Trader tidak dapat mengamati kedalaman likuiditas (market depth) pada setiap level harga maupun mengeksekusi strategi market making tradisional secara presisi.
* **Kerentanan terhadap Front-Running dan MEV.** Transaksi swap yang disiarkan ke mempool publik sangat rentan menjadi target eksploitasi Maximal Extractable Value (MEV), termasuk serangan sandwich yang merugikan harga eksekusi pengguna.

## 2.3 Biaya Gas sebagai Hambatan Masuk (Onboarding Barrier)

Setiap interaksi on-chain memerlukan token native dari jaringan terkait. Pengguna baru yang menerima suatu token tidak dapat langsung memperdagangkannya sebelum memiliki saldo BNB, ETH, maupun SOL untuk membayar biaya transaksi. Pada sistem order book, beban biaya gas ini muncul berulang kali pada setiap pemasangan maupun pembatalan order, sehingga menghambat aktivitas trading aktif serta strategi market making.

## 2.4 Distribusi Token yang Menguntungkan Pihak Internal

Banyak token bursa diluncurkan dengan porsi alokasi presale, modal ventura (venture capital), dan tim internal yang mendominasi supply. Pelepasan (unlock) alokasi tersebut ke pasar secara bertahap menimbulkan tekanan jual berkelanjutan. Selain itu, sering kali tidak terdapat mekanisme yang mengikat secara langsung antara pendapatan operasional platform dengan peningkatan nilai pada tokennya.

## 2.5 Keterbatasan Opsi Listing bagi Proyek Baru

* **Bursa Terpusat (CEX):** Pihak bursa menentukan sepenuhnya token mana yang diizinkan untuk listing. Prosesnya memerlukan persetujuan manual, memakan waktu lama, dan membebankan biaya yang umumnya melampaui kemampuan finansial proyek tahap awal.
* **DEX Berbasis AMM:** Meskipun bersifat tanpa izin (permissionless), perdagangan hanya berlangsung terhadap liquidity pool. Untuk menjaga price impact tetap rendah, proyek diwajibkan mengunci modal dalam jumlah besar pada pasangan dua aset sekaligus, yang membuat modal tersebut terpapar risiko impermanent loss.
* **Bursa Order Book Konvensional:** Protokol order book yang mengizinkan listing mandiri masih sangat jarang. Pada sebagian besar platform, pembukaan pasar baru tetap bergantung pada verifikasi dan penambahan manual oleh tim internal bursa.
