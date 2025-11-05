🌳 TreeToken Smart Contract
TreeToken is an Algorand-based smart contract (using ARC4) that enables the creation, management, and trading of digital trees within a blockchain ecosystem. This contract simulates the lifecycle of a digital tree, from planting and watering to trading the tree token.
Application ID : 748956158
Application Address : KLKR7IEP23HBQSGNY332MITJWMTLUXIK6GJM52I5STX5UPK7D7BZDQXOAM
Application Name : TreeToken
01⚡ Key Features
 * Plant Tree (Penanaman Pohon)
   Only the owner (contract creator) can plant a tree. Each planting records the last time the tree was watered via a timestamp.
 * Water Tree (Penyiraman Pohon)
   The owner or the system can update the last watered timestamp, indicating the tree remains alive.
 * Tree Tracking (Pelacakan Pohon)
   * get_last_watered() – Retrieves the timestamp of the last time the tree was watered.
   * get_owner() – Retrieves the current owner (default: creator).
 * Tree Trading (Perdagangan Pohon)
   * list_for_sale(price) – Marks the tree for sale at a specific price.
   * buy_tree(buyer, payment) – Transfers tree ownership if the payment is sufficient.
02 🛠️ Technology
 * Language: Python with Algopy (ARC4 Framework)
 * Blockchain: Algorand
 * Standard: ARC4 (Algorand smart contract standard)
03 📄 How It Works
 * Contract Initialization
   When the contract is created, the tree is not yet planted (is_planted = False) and is not listed for sale.
 * Planting the Tree (Menanam Pohon)
   The owner calls plant_tree(). The last watered timestamp is set to the current time.
 * Watering the Tree (Menyiram Pohon)
   The owner calls water_tree() to update the watering timestamp.
 * Selling and Buying the Tree (Menjual dan Membeli Pohon)
   The owner can call list_for_sale(price) to sell. A buyer can purchase it with buy_tree(buyer, payment) if the price is met.
🌱 Notes
 * This contract simulates a digital tree and can be further developed for:
   * Integration of rewards for tree maintenance
   * Unique NFTs for each tree token
   * Timestamp-based tree growth tracking
Would you like me to elaborate on a specific feature, like the ARC4 standard or how the trading functions work?
