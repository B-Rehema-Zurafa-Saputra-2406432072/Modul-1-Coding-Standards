## Reflection 1
Dalam pembuatan fitur edit dan delete product, terdapat beberapa prinsip clean code dan secure coding practices.
Ada penggunaan **meaningful names** seperti method findbyId, update, dan delete. Lalu juga ada prinsip **function**
yang hanya melakukan 1 hal (**Do One Thing**). Terdapat juga penggunaan POST untuk fitur delete sehingga lebih aman dibandingkan
menggunakan GET. Untuk hal-hal yang bisa diimprove, ada tambahan beberapa comment di source code. Juga belum adanya validasi
input merupakan hal yang bisa dilakukan sehingga lebih aman.