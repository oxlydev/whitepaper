# 16 Infrastruktur Pengembang & Integrasi (Developer & Integration Infrastructure)

Untuk mendukung integrasi eksternal, bot perdagangan algoritmik, penyedia likuiditas (market maker), serta aggregator data pasar, Oxly menyediakan rangkaian antarmuka pemrograman dan perangkat pengembangan yang komprehensif:

| Antarmuka & Perangkat | Spesifikasi Teknis & Cakupan Layanan |
|---|---|
| **REST API** | Akses data historis dan snapshot untuk informasi market, ticker, order book, riwayat trade, data candlestick, jadwal tarif biaya (fee), serta endpoint manajemen akun pengguna. |
| **WebSocket API** | Aliran data real-time berlatensi rendah meliputi kedalaman pasar (depth bid/ask per tingkat harga), ticker 24 jam, eksekusi trade, kline/candlestick (interval 1 menit hingga 1 minggu), serta pembaruan status order pengguna secara langsung. |
| **GraphQL API** | Kueri fleksibel untuk data on-chain yang telah terindeks (indexed data), mencakup riwayat market, order, trade, saldo aset terkunci (escrow), serta registri token. |
| **Datafeed TradingView** | Endpoint yang kompatibel sepenuhnya dengan standar UDF (Universal Data Feed) untuk integrasi grafik interaktif TradingView. |
| **API Agregator Pasar** | Endpoint standar yang kompatibel dengan spesifikasi integrasi CoinMarketCap dan CoinGecko untuk pelaporan volume dan likuiditas otomatis. |
| **Smart Contract Terverifikasi** | Kode sumber smart contract yang telah terverifikasi secara publik lengkap dengan dokumentasi spesifikasi fungsi, event, dan kode error. |
| **SDK & Lingkungan Testnet** | Pustaka pengembangan resmi dalam bahasa JavaScript/TypeScript, Python, dan Go, dilengkapi akses penuh ke jaringan uji (testnet) beserta layanan faucet untuk pengujian integrasi. |

### Otomatisasi Bot Tanpa Biaya Gas (Delegated Gasless Bot Trading)

Sistem bot perdagangan otomatis maupun market maker dapat mengeksekusi transaksi tanpa biaya gas pada jaringan BNB Smart Chain dengan memanfaatkan kuota kapasitas OXG yang didelegasikan (delegated OXG) dari akun utama maupun penyedia likuiditas.
