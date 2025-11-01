# 🌳 TreeToken Smart Contract

**TreeToken** adalah smart contract berbasis Algorand (menggunakan ARC4) yang memungkinkan pembuatan, pengelolaan, dan perdagangan pohon digital dalam ekosistem blockchain. Kontrak ini mensimulasikan siklus hidup pohon digital, mulai dari penanaman, penyiraman, hingga perdagangan token pohon.

Application ID : 748956158

Application Address : KLKR7IEP23HBQSGNY332MITJWMTLUXIK6GJM52I5STX5UPK7D7BZDQXOAM

Application Name : TreeToken

**01**⚡ Fitur Utama

* **Penanaman Pohon (Plant Tree)**
  Hanya owner (pembuat kontrak) yang bisa menanam pohon. Setiap penanaman mencatat timestamp terakhir pohon disiram.

* **Penyiraman Pohon (Water Tree)**
  Owner atau sistem dapat memperbarui timestamp terakhir pohon disiram, menunjukkan pohon tetap hidup.

* **Pelacakan Pohon**

  * `get_last_watered()` – Mendapatkan timestamp terakhir pohon disiram.
  * `get_owner()` – Mendapatkan pemilik saat ini (default: creator).

* **Perdagangan Pohon (Buy/Sell)**

  * `list_for_sale(price)` – Menandai pohon untuk dijual dengan harga tertentu.
  * `buy_tree(buyer, payment)` – Memindahkan kepemilikan pohon jika pembayaran mencukupi.
**02** 🛠️ Teknologi

* **Bahasa**: Python dengan Algopy (Framework ARC4)
* **Blockchain**: Algorand
* **Standar**: ARC4 (Algorand smart contract standard)

**03** 📄 Cara Kerja

1. **Inisialisasi Kontrak**
   Saat kontrak dibuat, pohon belum ditanam (`is_planted = False`) dan tidak dijual.

2. **Menanam Pohon**
   Owner memanggil `plant_tree()`. Timestamp terakhir pohon disiram diset ke waktu saat ini.

3. **Menyiram Pohon**
   Owner memanggil `water_tree()` untuk memperbarui timestamp penyiraman.

4. **Menjual dan Membeli Pohon**
   Owner dapat memanggil `list_for_sale(price)` untuk menjual. Pembeli dapat membeli dengan `buy_tree(buyer, payment)` jika harga cukup.

🌱 Notes
* Kontrak ini mensimulasikan pohon digital dan bisa dikembangkan lebih lanjut untuk:
  * Integrasi reward untuk perawatan pohon
  * NFT pohon unik untuk tiap token
  * Pelacakan pertumbuhan pohon berbasis timestamp
