## Reflection 1
Dalam pembuatan fitur edit dan delete product, terdapat beberapa prinsip clean code dan secure coding practices.
Ada penggunaan **meaningful names** seperti method findbyId, update, dan delete. Lalu juga ada prinsip **function**
yang hanya melakukan 1 hal (**Do One Thing**). Terdapat juga penggunaan POST untuk fitur delete sehingga lebih aman dibandingkan
menggunakan GET. Untuk hal-hal yang bisa diimprove, ada tambahan beberapa comment di source code. Juga belum adanya validasi
input merupakan hal yang bisa dilakukan sehingga lebih aman.

## Reflection 2
Dalam penentuan jumlah unit test, tidak terdapat _set rules_ berapa unit test yang perlu ditulis. Namun, terdapat indicator
cukup baik untuk menentukan jumlah unit test melalui _code coverage_. Code coverage itu sendiri adalah suatu persentase
banyak baris kode yang dijalankan oleh test dibagi oleh jumlah baris kode sebenarnya. Sebagai _rule of thumb_, 80 hingga 90% 
code coverage dapat dibilang sebagai unit test yang efektif. Walaupun code coverage dapat menjadi indicator, code coverage 100%
belum berarti code tidak memiliki bug atau error. Ini karena mungkin saja test yang kita buat sebenarnyaa kurang tepat dengan
ekspektasi yang diinginkan oleh user.

Jika membuat functional test baru yang menggunakan _setup procedure_ dan _instance variables_ yang persis sama akan menurunkan _code quality_.
Ini karena terdapat pelanggaran aspek Clean Code dalam bagian Code Duplication serta melanggar prinsip DRY (Don't Repeat Yourself). Duplikasi code
terjadi diakibatkan penggunaan _setup_ yang sama dalam kedua functional test. Agar tidak terjadi duplikasi code, menggunakan abstract class dan inheritance.
Kita dapat membuat abstract class yang memiliki variabel umum seperti serverPort dan baseUrl serta method setup (yang ditandai @BeforeEach).
Lalu, Class functional test lainnya hanya perlu meng-extends dari abstract class tersebut untuk menggunakan setupnya. Dengan ini,
duplikasi code tidak terjadi.
