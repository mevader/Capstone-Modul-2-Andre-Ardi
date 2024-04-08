# Capstone-Modul-2-Andre-Ardi
Tugas Purwhadika
# **PENENTUAN LOKASI IDEAL INVESTASI SEWA  PROPERTI AIRBNB BANGKOK**

# **Latar Belakang Masalah**

Pada project data analysis ini kita akan membantu investor asing yang akan menanamkan modalnya pada bisnis penyewaan properti di kelas premium di daerah Bangkok dengan menggunakan aplikasi airbnb. 

Air Bed & Breakfast (Airbnb) menyediakan APP/online market place untuk mengkoneksikan PROPERTY HOST and PEOPLE yang mencari HOMESTAY di lokasi tertentu. Ini bisnis dimasa depan.

Keputusan investor untuk menanamkan modal tersebut akan didasarkan beberapa faktor seperti: harga sewa, lokasi, tingkat hunian, dan popularitas lokasi.

Untuk itu masalah yang harus dijawab adalah:
Dimana lokasi yang paling ideal bagi investor untuk berinvestasi? 

Selain itu harus dijawab juga beberapa pertanyaan tambahan ini:
1. bagaimana klasifikasi daerah berdasarkan tingkat harga sewa,
1. bagaimana klasifikasi daerah berdasarkan tingkat rata-rata listing airbnb,
1. bagaimana klasifikasi daerah berdasarkan occupancy rate, 
1. bagaimana klasifikasi daerah berdasarkan popularitas review penyewa,
1. bagaimana strategi investor dalam penentuan harga sewa,
1. bagaimana strategi investor dalam menentukan type properti yang akan disewakan,
1. Bagaimana strategi kompetisi dalam penyewaan properti yang akan dihadapi oleh investor.

Metode yang digunakan untuk menganalisis data adalah melalui tahapan:
1. Data collecting: di samping data yang telah tersedia juga diperlukan data lain seperti koordinat map dan keterangan umum mengenai lokasi neighbourhood,
1. Data understanding: menggunakan deskriptif untuk memahami data secara umum, seperti: dimensi dataset, standar deviasi, normalitas data, mean, median, data kosong dan sebagainya,
1. Data cleaning: pembersihan data yang dilakukan dengan merapihkan format penulisan, dan penanganan data kosong bila diperlukan,
1. data analisis: yaitu menganalisis data yang telah dipersiapkan guna dapat menjawab pertanyaan utama dari project ini yaitu menentukan lokasi mana yang paling ideal bagi investor untuk berinvestasi properti AirBNB di Bangkok
1. Kesimpulan dan Rekomendasi

Deskripsi Kolom:

* id: Airbnb's unique identifier for the listing 
* name: Name of the listing.
* host_id: Airbnb's unique identifier for the host/user.
* host_name: Name of the host
* neighborhood: The neighborhood is geocoded using the latitude and longitude against neighborhoods as defined by open or public digital shapefiles.
* latitude: Uses the World Geodetic System (WGS84) projection for latitude and longitude.
* longitude: Uses the World Geodetic System (WGS84) projection for latitude and longitude.
* room_type: [Entire home/apt |Private room| Shared room| Hotel]
* price: Daily price in local currency
* minimum_nights: The minimum number of night stays for the listing (calendar rules may differ).
* number_of_reviews: The number of reviews the listing has.
* last_review: The date of the last/newest review.
* calculated_host_listings_count: The number of listings the host has in the current scrape in the city/region geography.
* availability_365: avaliability_x. The calendar determines the availability of the listing x days in the future. 
* number_of_reviews_ltm: The number of reviews the listing has (in the last 12 months).

# **DATA CLEANING**
Data kosong:
‘last_review’ & ‘review_per_month’ saling terkait (MaR)
Kosong karena tidak ada review jadi dibiarkan saja. 
Namun review_per_month: NaN diganti 0

‘name’ & ‘host_name’ dibiarkan saja kosong karena dipandang tidak akan mempengaruhi analisis

Outliers:
Outliers ‘price’ dihapus dengan cara Inter Quartil Range (IQR)
‘minimun_nights’, ‘number_of_reviews’, ‘review_per_month’, ’number_of_reviews_ltm’, dan ‘calculated_host_listings_count’ dipandang sebagai natural outliers sehingga dibiarkan

Distribusi Data:
Tidak ada data numerikal yang berdistribusi normal
Untuk pengujian Statistik menggunakan NON-PARAMETRIS

# **ANALISIS DATA**

##  **ANALISIS 1: KLASIFIKASI LOKASI**

Lakukan klasifikasi daerah berdasarkan kriteria:
1. tingkat harga sewa,
2. bagaimana klasifikasi daerah berdasarkan tingkat rata-rata listing airbnb,
3. bagaimana klasifikasi daerah berdasarkan occupancy rate, 
4. bagaimana klasifikasi daerah berdasarkan popularitas review penyewa,
   

REKOMENDASI LOKASI INVESTASI: VADHANA (PRIORITAS 1) KHLONG TOEI (PRIORITAS 2)

## **ANALISIS 2: STRATEGI HARGA BAGI SI INVESTOR**

Lakukan uji korelasi berdasarkan lokasi, tipe properti, tingkat review, dan tingkat booking masing-masing terhadap harga

INSIGHT for INVESTOR:

1. Patokan penentuan harga sewa:
  a. lokasi
  b. tipe properti
  c. tingkat booking (perhatikan season)
2. Harga di Vadhana start from 1.732 THB
3. Khlong Toei start from 1581 THB

## **ANALISIS 3: STRATEGI PENENTUAN TIPE PROPERTI BAGI INVESTOR**

INSIGHT for INVESTOR
1. Pilihan tawaran properti di Vadhana atau Khlong Toei:
   a. Entire home/apt > 60%
   b. Private Room >20%
2. Untuk investasi premium maka opsi terbaik adalah Entire home/apt
3. Home vs Apartemen?
Secara situasional home (prioritas 1) dapat disewakan sebagai private room
Namun untuk ketersediaan properti, apartemen (prioritas 2) jelas lebih tersedia suplainya dengan harga lebih kompetitif

## **ANALISIS 4: STRATEGI KOMPETISI INVESTOR**

INSIGHT for INVESTOR
1. Vadhana dan Khlong Toei terpadat kompetitornya
2. Kompetitor serius area Bangkok (benchmark=221 listing): Curry (listing terbanyak di Bangkok dan beberapa neighbourhood) dan Noons
3. Kompetitor serius di Vadhana (benchmark=41 listing): Lek Boonsiri & Ludoping 
4. Kompetitor serius di Khlong Toei (benchmark=45 listing): Curry, Summer, dan Noons
5. Terapkan strategi ‘ME TOO’ yaitu menempel lokasi kompetitor untuk mengambil porsi pasar dan menutup ekspansi

## **ACTION!**

1. Pilih lokasi investasi premium: Vadhana (prioritas) dan/atau Khlong Toei (prioritas 2)
    a. Pilih Vadhana bila harga tidak menjadi masalah, supply tersedia, dan siap menghadapi kompetitor
    b. Khlong Toei memiliki daerah slum yang bisa dikembangkan (wikipedia)
2. Tetapkan harga sewa di Vadhana (kisaran 1.732 THB) dan Khlong Toei (kisaran 1581 THB) (perhatikan tingkat booking season,  tipe properti, dan lokasi)
3. Pilih tipe: home (bisa displit per kamar) dan/atau apartemen (lebih tersedia suplainya)
4. Terapkan strategi ‘ME TOO’ (mengikuti kemana kompetitor pergi) guna menikmati porsi pasar yang selama didominasi kompetitor. Dalam jangka panjang akan menutup peluang ekspansi kompetitor.
5. Jadi pemain utama. Kompetisi akan menjadikan pasar berkembang. Benchmark untuk menjadi pemain utama:
    a. Di pasar Bangkok = 221 listing properti
    b. Di pasar Vadhana = 41 listing properti
    c. Di pasar Khlong Toei = 45 listing properti
