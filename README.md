# Car-Price-Prediction

Dataset taken from : https://www.kaggle.com/fazilbtopal/auto85?select=auto_clean.csv

# Define Problems :
- Sebagai Produsen Mobil Brand Baru yang ingin menjual produk mobil, agar dapat bersaing dengan harga jual di pasaran.

# Goals :
- Mendapatkan gambaran harga jual untuk mobil.
- Mendapatkan gambaran spesifikasi dan referensi untuk mobil yang dijual di pasaran.

# Deskripsi Kolom
- make : merk/brand mobil
- aspiration : sistem permesinan
- num-of-doors : jumlah pintu
- body-style : tipe mobil berdasarkan body
- drive-wheels : penggerak mobil
- engine-location : lokasi engine mobil
- wheel-base : jarak antara roda depan ke roda belakang
- length : panjang mobil
- width : lebar mobil
- height : tinggi mobil
- curb-weight : berat mobil
- engine-type : tipe engine mobil
- num-of-cylinders : banyaknya silinder
- engine-size : ukuran engine mobil
- fuel-system : sistem injeksi
- bore : diameter silinder
- stroke : tinggi silinder
- compression-ratio : perbandingan volume silinder
- horsepower : tenaga kuda
- peak-rpm : rotasi per menit paling maksimum
- city-mpg : mile per galon (dalam kota)
- highway-mpg : mile per galon (dalam tol)
- price : harga mobil
- city-L/100km : liter per 100 km (dalam kota)
- diesel : mobil yang menggunakan bahan bakar diesel (jika = 1)
- gas : mobil yang menggunakan bahan bakar gas (jika = 1)

# Conclusion Exploratory Data Analysis
- Top 5 Merk dengan tenaga paling tinggi (horsepower/engine-size) yaitu mercury, saab, porsche, volvo dan alfa-romero.
- Top 5 Merk dengan tenaga paling rendah (horsepower/engine-size) yaitu mercedes-benz, jaguar, isuzu, peugot, dan volkswagen.
- Mobil dengan bahan bakar gas memiliki harga mobil yang lebih rendah dibandingkan dengan mobil yang berbahan bakar diesel.
- Dari segi keiritan, mobil dengan bahan bakar diesel lebih irit dibandingkan dengan mobil berbahan bakar gas. Mobil diesel cenderung memiliki compression ratio lebih tinggi (berdasarkan data CR = 22) dibanding mobil bensin sehingga memiliki efisiensi thermal lebih baik dibanding mobil bensin. Mobil bensin memiliki limitasi untuk compression ratio karena jika terlalu tinggi compression ratio nya akan menambah kemungkinan bahan bakar terbakar sebelum waktunya (engine knocking).
- Dari segi tenaga, mobil dengan bahan bakar gas lebih bertenaga dibandingkan dengan mobil berbahan bakar diesel karena mobil berbahan bakar gas cenderung memiliki PEAK RPM lebih tinggi dibanding mobil diesel (horsepower formula = torque x RPM / 5252)
- Mayoritas untuk semakin banyak jumlah silinder yang digunakan pada tiap mobil akan meningkatkan harga mobil.
- Untuk drive-wheels dengan tipe rwd lebih mahal dibandingkan 4wd dan fwd dikarenakan mobil yang menggunakan drive-wheels digunakan oleh mobil-mobil premium, sedangkan untuk mobil yang menggunakan fwd digunakan oleh mobil-mobil yang relatif murah (hatchback)
- Untuk mobil dengan body-style hardtop dan convertible lebih mahal jika dibandingkan dengan hatchback, sedan, dan wagon.
- Untuk mobil dengan engine-location di rear harganya lebih tinggi jika dibandingkan pada lokasi di front.
- Untuk mobil dengan engine-type dohc harganya lebih tinggi jika dibandingkan dengan l, ohc, dan rotor.
- Untuk mobil dengan jumlah pintu 4 harganya lebih tinggi jika dibandingkan dengan jumlah pintu 2.
- Untuk mobil dengan curb-weight semakin berat, maka akan semakin tinggi harganya.
- Untuk spesifikasi mobil dengan length, height, wheel-base yang semakin tinggi dan tidak dipengaruhi oleh harga penjualan
- Untuk mobil dengan aspiration type turbo harganya lebih tinggi jika dibandingkan dengan aspiration type std. Banyak komponen tambahan untuk mendukung peningkatan tekanan pada silinder sehingga biaya untuk mesin yang ber-turbo lebih mahal.
- Untuk mobil dengan aspiration type turbo tenaganya lebih tinggi jika dibandingkan dengan aspiration type std. Karena pada mobil dengan turbo udara yang dihisap lebih banyak dibanding mobil standar sehingga daya yang dihasilkan lebih besar.
- Untuk mobil dengan aspiration type std keiritannya lebih baik jika dibandingkan dengan aspiration type turbo. Udara yang masuk lebih besar harus diimbangi dengan jumlah bahan bakar yang masuk sehingga keiritan mobil turbo menurun.

# Recommendation Exploratory Data Analysis
- Berdasarkan dari pengolahan Exploratory Data Analysis, maka kami mengambil kesimpulan bahwa features yang mempengaruhi harga mobil yaitu make, aspiration, num-of-doors, body-style, drive-wheels, engine-location, curb-weight, engine-type, num-of-cylinders, engine-size, fuel-system, compression-ratio, horsepower, city-mpg, highway-mpg, price, diesel, gas.
- Jika Produk baru ingin bersaing dengan merk-merk lain, maka harus memperhatikan keunggulan dari tiap kompetitor dan mempertimbangkan dari segi spesifikasi dan harga yang dijual, sehingga tidak terlalu menyimpang dari harga pasaran yang dijual oleh kompetitor-kompetitor lainnya.
- Untuk menarik pelanggan dari segi tenaga mobil, diusahakan agar membuat mobil yang tenaganya (horsepower/engine-size) sebanding dengan harga yang dikeluarkan. Karena berdasarkan data yang diperoleh, ada beberapa mobil yang harganya tinggi namun memiliki tenaga yang rendah.

# Conclusion Machine Learning :
## Untuk Model Machine Learning yang memiliki hasil terbaik untuk menebak harga mobil yaitu :
- **Base Model Ridge :**
    - Nilai R2 train : 9.395397e-01 dan R2 test : 9.001467e-01
    - Nilai MAE train : 1.209527e+03 dan MAE test : 2.107464e+03
    - Nilai MSE train : 2.758581e+06 dan MSE test : 1.221673e+07
    - Nilai RMSE train : 1.660898e+03 dan RMSE test : 3.495244e+03
