# Content-Based-Recommender-System-With-Similarity-Function
Dengan dataset diambil dari IMDb Datasets yang berisikan data data film, saya membuat recommender system yang menggunakan Content/feature dari film/entitas tersebut, kemudian melakukan perhitungan terhadap kesamaannya satu dan yang lain sehingga ketika menunjuk ke satu film, akan mendapat beberapa film lain yang memiliki kesamaan dengan film tersebut. Hal ini biasa disebut sebagai Content Based Recommender System. Dengan membandingkan kesamaan plot yang ada dan genre yang ada, ketika audience lebih menyukai film Narnia, maka content based recommender system ini akan juga merekomendasikan film seperti Harry Potter atau The Lords of The Rings yang memiliki genre yang mirip.


# Checking Datasets
Dataset yang kami gunakan yaitu IMDb Datasets yang dapat didownload pada link https://datasets.imdbws.com/ . Dataset tersedia untuk akses ke pelanggan untuk penggunaan pribadi dan non-komersial. Dataset yang kami gunakan adalah sebagai berikut:

**title.basics.tsv** - Berisi informasi berikut :

* tconst (string) - pengenal unik alfanumerik dari judul
* titleType (string) - jenis / format judul (misalnya film, pendek, tvseries, tvepisode, video, dll)
* primaryTitle (string) - judul yang lebih populer / judul yang digunakan oleh pembuat film pada materi promosi pada saat peluncuran
* originalTitle (string) - judul asli, dalam bahasa aslinya
* isAdult (boolean) - 0: judul non-dewasa; 1: gelar dewasa
* startYear (YYYY) - mewakili tahun rilis suatu judul. Dalam kasus Serial TV, ini adalah tahun mulainya serial
* endYear (YYYY) - Tahun akhir serial TV. '\ N' untuk semua jenis judul lainnya
* runtimeMinutes - runtime utama dari judul, dalam menit
* genre (string array) - mencakup hingga tiga genre yang terkait dengan judul
* averageRating - rata-rata peringkat Judul
* numVotes - jumlah suara yang diterima judul

**title.crew.tsv** – Berisi informasi sutradara dan penulis untuk semua judul di IMDb.

* tconst (string) - pengenal unik alfanumerik dari judul
* directors (array of nconsts) - sutradara dari judul
* writers (array of nconsts) – penulis dari judul

**name.basics.tsv** - Berisi informasi nama berikut:

* nconst (string) - pengenal unik alfanumerik dari nama / orang
* primaryName (string) - nama orang
* birthYear - dalam format YYYY
* deathYear - dalam format YYYY jika ada, lain '\ N'
* primaryProfession (array of string) - 3 profesi teratas orang tersebut
* knownForTitles (array of tconsts) - keterikatan orang tersebut dengan judul
