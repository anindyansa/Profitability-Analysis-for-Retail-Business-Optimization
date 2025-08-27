# judul 
## Table of Contents


### Project Overview
Power BI dashboard analyzing profit and revenue across Home Appliances, Groceries, Apparel, and Electronics. Includes data cleaning, formatting, and visualization to turn raw sales data into actionable business insights.

<img width="901" height="505" alt="image" src="https://github.com/user-attachments/assets/7b84bf62-311f-4868-9747-6b3fe815e560" />

### Data Sources 
Untuk analisis profitabilitas ini, kami menggunakan tiga dataset utama yang mendukung tujuan bisnis dalam mengidentifikasi faktor profitabilitas berdasarkan produk dan kategori. Berikut adalah deskripsi setiap dataset:

**a.) Sales_Data** : Dataset ini mencakup informasi terkait penjualan produk pada berbagai kategori dan wilayah. Dataset ini berisi 100 entri dengan rincian mengenai produk, kategori, wilayah, serta jalur distribusi. Data ini berfokus pada detail penjualan produk yang digunakan untuk menghitung pendapatan.

**b.) Cost_Profit_Data** : Dataset ini mencakup data terkait biaya produksi, biaya d istribusi, dan profit netto. Data ini berfungsi untuk menghitung dan menganalisis margin profitabilitas produk setelah mempertimbangkan berbagai komponen biaya.

**c.) Additional_Info** : Dataset ini berisi data tambahan terkait musim penjualan, tanggal penjualan, dan demografi pelanggan. Data ini membantu dalam memahami tren musiman serta segmentasi pelanggan yang relevan dalam profitabilitas.

Berikut adalah kolom dataset keseluruhan beserta deskripsinya :

|heading1|heading2|
|--------|--------|
|Product_ID|ID unik untuk setiap produk|
|Product_Category|Kategori produk (misalnya, Elektronik, Pakaian, Peralatan Rumah Tangga)|
|Region|Wilayah penjualan produk (misalnya, Jakarta, Surabaya, Bali)|
|Sales_Channel|	Saluran penjualan (misalnya, Online, Toko Fisik)|
|Unit_Price|	Harga jual per unit produk|
|Units_Sold|	Jumlah unit terjual|
|Total_Revenue|	Total pendapatan dari produk tersebut|
|Production_Cost|	Biaya produksi per unit|
|Distribution_Cost|	Biaya distribusi per unit|
|Discount_Percentage|	Persentase diskon yang diberikan|
|Net_Profit|	Keuntungan bersih setelah dikurangi biaya produksi, distribusi, dan diskon|
|Season|	Musim atau kuartal penjualan (misalnya, Q1, Q2, dst)|
|Date_Sold|	Tanggal penjualan produk|
|Customer_Age_Group|	Kelompok umur pelanggan (misalnya, 18-25, 26-35, 36-45)|

### Data Cleaning/Data Preparation 
Tahapan persiapan dan pembersihan data bertujuan untuk memastikan kualitas dan konsistensi data yang akan dianalisis. Proses ini melibatkan beberapa langkah penting yang dirancang untuk menangani data yang tidak lengkap, tidak sesuai format, atau tidak konsisten. Adapun tahapan yang dilakukan meliputi:

**1. Penanganan Data Hilang (Missing Values)** 
- Kolom Discount_Percentage :
Dalam kolom ini, jika terdapat nilai yang kosong atau tidak diisi, diasumsikan bahwa tidak ada diskon yang diberikan untuk entri tersebut. Oleh karena itu, nilai kosong diisi dengan “0%” untuk menghindari ketidaksesuaian dalam analisis.
- Kolom Net_Profit :
Nilai yang bersifat 'null' atau kosong pada kolom ini dihapus dari dataset untuk menjaga integritas data, mengingat profit netto merupakan metrik penting yang harus tersedia dalam setiap entri produk.

**2.	Konsistensi Format Tanggal**
- Kolom Date_Sold : Untuk menjaga konsistensi data, kolom Date_Sold diselaraskan dengan format standar (misalnya, YYYY-MM-DD). Standarisasi ini bertujuan untuk mempermudah proses analisis yang melibatkan dimensi waktu, seperti identifikasi tren musiman atau perhitungan penjualan bulanan.

### Results/Findings 
The analysis results are summarized as follows :
**1. Net Profit Overview – KPI Card**
   
   <img width="201" height="222" alt="image" src="https://github.com/user-attachments/assets/535d49bb-b5b6-4fe0-86fd-64318955855d" />

***Data*** : `Total_Revenue`, `Net_Profit` 

***Insight*** :
- Provides a concise overview of the company’s real financial condition by highlighting the differences between gross revenue, costs, and net profit. This allows management to quickly understand the overall actual profitability after all expenses are taken into account.
- Analysis period: January–April 2024, covering all regions and product categories.
- By region, Surabaya recorded the highest net profit of Rp268K, while Bali posted the lowest at Rp80K.
- Initial findings indicate that high revenue does not always translate into high net profit, making cost efficiency in each region a critical factor.
  
***Managerial Implementation*** : 
- Net profit can serve as a key indicator of the company’s financial health during January–April 2024.
- Comparing revenue, costs, and net profit helps identify the proportion of expenses relative to gross revenue.
- The difference shown (in terms of marginal cost) can be used as a basis to evaluate whether distribution, production, and discount policies remain efficient or instead create unnecessary burdens.
- The highest-contributing region (Surabaya) can serve as a benchmark, while underperforming regions (Bali) require cost and sales strategy evaluation to improve profitability.

**2. Category Comparison Performance – Table with Slicer**

   <img width="327" height="226" alt="image" src="https://github.com/user-attachments/assets/7642ada3-ba3b-4e96-aed9-2ef041975c7d" />
   
***Data*** : `Product_Category`, `Units_Sold`  ,  `Units_Sold` , `Total_Revenue`  ,`Net_Profit` ,  `Region` , `Date_Sold`   

***Insight*** :
- This visualization presents sales performance in terms of revenue, net profit, operating costs, and margins. Data is segmented by product category, region, and period, allowing management to assess each dimension’s contribution to profitability and to identify both strengths and underperforming areas.
- Overall Performance: From a total revenue of $3,000,191, the company achieved $765,955 net profit with a 25.5% margin. While healthy, profit distribution across categories is uneven.
- Home Appliances delivered the highest profit ($257,709 | 33.6%) with a 28.3% margin.
- Groceries contributed strongly ($226,309 | 29.5%) and achieved the highest efficiency with a 31.5% margin.
- Apparel generated moderate profit ($164,244 | 21.4%) with a 28.9% margin, acting as a balancing category.
- Electronics recorded the highest revenue ($814,995) but the lowest profit ($117,693 | 15.4% margin) due to high cost/distribution burdens.
- Surabaya achieved the highest profit ($267,888), mainly from Electronics and Groceries. However, Home Appliances showed weak margins despite strong sales volume. Notably, no sales were recorded in April, signaling distribution or seasonal demand issues. Bali posted the lowest profit ($79,556) with heavy reliance on Home Appliances, causing volatility. In April, Electronics sales led to a major loss (- $41,302), turning overall profit negative.

***Managerial Implementation*** : 
- Groceries act as a cash cow with high margins and low risk, making them a top priority for expansion due to consistent contribution.
- Home Appliances, despite large profits, remain inefficient as high sales volume does not align with margins. Distribution and production need evaluation to boost effectiveness.
- Electronics face pressured margins; cost reviews, discount strategies, supplier renegotiation, or price adjustments are necessary to improve profitability.
- Apparel serves as a stabilizer but requires product and pricing differentiation to avoid recurring losses.
- The company can strengthen high-profit categories (Groceries) while addressing inefficiencies in Home Appliances & Electronics.
- Surabaya risks losing momentum; improving Home Appliances’ profitability is key for regional stability.
- Bali is overly dependent on Home Appliances; diversification into Groceries and cost efficiency in Electronics & Apparel are crucial for mid-term growth.

3. Discount Effectiveness Analysis – Line & Stacked Bar Chart

  <img width="324" height="222" alt="image" src="https://github.com/user-attachments/assets/8fc08f33-940d-424b-8079-1812d00cfa41" />

***Data*** : `Product_Category` , `Total_Revenue` , `Net_Profit` , `Discount_Percentage` 

***Insight*** :
- This visualization analyzes the relationship between discount levels, revenue, and net profit across product categories. The objective is to measure the effectiveness of discounts in driving profitability while identifying whether current discount strategies are optimal or instead burden overall performance.
- Electronics: Lowest average discount (8%) but also the smallest profit contribution ($117,693). This suggests that lower discounts do not necessarily ensure profitability, likely due to thin margins or relatively high cost of goods sold.
- Groceries: Highest discount rate (13%) yet still delivers substantial profit ($226,309). This indicates that high sales volume can offset aggressive discounting, keeping profitability intact.
- Home Appliances: Highest profit ($257,709) with a moderate discount rate (9%). This reflects an effective discount strategy—moderate in size, yet able to generate high revenue ($912,539) while sustaining strong margins.
- Apparel: Medium profit contribution ($164,244) with a 10% discount. Compared to categories with similar revenue, Apparel is less efficient in leveraging discounts to improve profit, suggesting the need for revised promotion strategies and product positioning.

Managerial Implementation : 
- Home Appliances: Maintain moderate discounts (7–10%) to safeguard profitability, position as a cash cow, and prioritize long-term promotional investments.

Groceries: Apply aggressive yet controlled discounts (max 12%). Alternatives include bundling or subscription models (e.g., monthly packages) to sustain sales volume without eroding margins.

Electronics: Reassess cost structure in production and logistics. Priorities include supplier renegotiation and supply chain efficiency. If discounts prove ineffective, consider price repositioning or reducing category focus.

Apparel: Avoid excessive discounting outside peak seasons. Instead, emphasize product differentiation or limited-edition campaigns to add value without relying heavily on discounts.

Selective Discounting: Apply a loss leader strategy only to highly competitive categories or new products, while retaining premium pricing in high-margin categories to preserve brand value.

Cross-Subsidizing: Utilize profits from high-margin categories (Home Appliances, Groceries) to support categories that require deeper discounts as market entry levers.

Marketing Targeting: Position discount-sensitive categories for seasonal promotions, while profitable categories without discount reliance should focus on brand building.

4. Sales Volume Dynamics – Clustered Bar Chart
   
   <img width="369" height="226" alt="image" src="https://github.com/user-attachments/assets/eb08c5de-bee3-4692-abbb-bbff7ed6a526" />

***Data*** : `Product_Category` , `Units_Sold` 

***Insight*** :
•	Visualisasi ini memberikan gambaran mengenai dinamika jumlah unit terjual (unit sold) per bulan untuk masing-masing kategori produk. Analisis ini bermanfaat untuk menilai konsistensi permintaan, mengidentifikasi faktor pendorong maupun penghambat penjualan, serta memahami bagaimana volume penjualan memengaruhi capaian revenue dan profitabilitas perusahaan.
•	Januari menjadi periode dengan performa awal yang kuat (8,098 unit), menghasilkan profit $482,085. Hampir semua kategori mencatatkan kontribusi positif, terutama Apparel ($145,310) dan Electronics ($131,363). Tingginya volume di bulan ini menandakan momentum awal tahun yang produktif.
•	Februari mencatat jumlah unit tertinggi sepanjang periode (8,678 unit), namun profit justru turun signifikan menjadi $326,262. Hal ini menunjukkan bahwa kenaikan volume tidak otomatis diikuti profitabilitas, diduga karena tekanan biaya distribusi maupun strategi diskon yang kurang tepat, terutama pada Electronics yang hanya menyumbang $20,058 meski terjual 1,133 unit.
•	Maret mengalami penurunan volume (7,294 unit) tetapi justru profit meningkat tajam menjadi $451,834. Pola ini mengindikasikan adanya perbaikan efisiensi biaya atau penyesuaian strategi harga. Groceries menjadi penyumbang terbesar ($146,503) meski tidak mencatat volume tertinggi, yang menunjukkan efektivitas pengelolaan margin.
•	April menunjukkan penurunan tajam (3.041 unit) dan profit terendah ($175,384). Hampir seluruh kategori melemah, terutama Apparel yang hanya mencatat 474 unit dengan profit $17,036. Situasi ini merefleksikan kerentanan permintaan di akhir periode, sehingga konsistensi pasar menjadi tantangan utama.

***Managerial Implementation*** :
•	Optimalkan efisiensi biaya distribusi dan promosi terutama pada periode dengan volume tinggi (seperti Februari), agar peningkatan unit terjual dapat selaras dengan profitabilitas. Evaluasi struktur biaya per kategori menjadi prioritas.
•	Fokus pada kategori resilient seperti Home Appliances dan Groceries yang tetap mencatatkan profit bahkan di kondisi melemah (April). Strategi promosi jangka panjang dapat diarahkan pada kategori ini untuk menjaga kestabilan pendapatan.
•	Kendalikan kerugian kategori rentan (Electronics dan Apparel) melalui peninjauan ulang strategi diskon, renegosiasi pemasok, atau diferensiasi produk. Tanpa intervensi, kategori ini berisiko menjadi beban struktural saat volume menurun.
•	Perkuat monitoring musiman: pola Januari–Maret menunjukkan perbedaan signifikan antara volume dan profit, sehingga sistem peringatan dini berbasis indikator volume dan margin perlu dikembangkan untuk mengantisipasi periode pelemahan.
•	Diversifikasi strategi pemasaran antar-bulan: pada periode puncak penjualan, strategi volume dapat diprioritaskan, sementara pada periode lesu, fokus pada margin melalui harga premium atau bundling lebih relevan.

**5. Donut Chart**  

<img width="158" height="225" alt="image" src="https://github.com/user-attachments/assets/a1362b7c-0c08-4e51-95a6-99322d24060e" />

***Data*** : `Sales_Channel`  

***Insight*** : 
•	Visualisasi ini bermanfaat untuk memahami distribusi dan dinamika channel penjualan dengan melihat tren pertumbuhan, kategori yang dominan, serta perbedaan kontribusi antar wilayah. Dari hasil pengamatan, diperoleh beberapa poin penting:
•	Pertumbuhan Online Channel
Angka pertumbuhan online masih fluktuatif (43 → 46 → 40 → 41). Hal ini menunjukkan belum adanya pertumbuhan stabil, bahkan sempat mengalami penurunan pada bulan Maret. Kondisi ini menegaskan pentingnya strategi digital marketing yang lebih konsisten, misalnya melalui campaign musiman, loyalty program, atau push notification e-commerce.
•	Distribusi Kategori Penjualan
Electronics menjadi kontributor terbesar dengan 50%, menandakan tingginya daya tarik di pasar digital maupun fisik. Sebaliknya, kategori Groceries hanya mencapai 37%, sehingga masih terdapat ruang untuk optimalisasi, misalnya melalui promo bundle online atau kampanye khusus kebutuhan harian.
•	Distribusi Geografis
Surabaya mendominasi dengan kontribusi 55%, menandakan penetrasi channel yang kuat di kota besar. Sementara itu, Bali hanya 37%, yang mengindikasikan potensi pasar yang belum tergarap maksimal, terutama melalui online channel yang dapat menjangkau konsumen wisatawan maupun lokal.

***Manajerial implementasi*** :
•	Meningkatkan stabilitas pertumbuhan online melalui campaign berkesinambungan, seperti program loyalitas dan seasonal campaign.
•	Mengoptimalkan kategori groceries agar lebih kompetitif di online dengan strategi promosi yang lebih menarik (contohnya bundle promo kebutuhan harian).
•	Memperluas penetrasi di daerah non-dominan seperti Bali dengan memanfaatkan kanal online sebagai sarana menjangkau segmen wisatawan dan masyarakat lokal.

**6. Age Group Revenue Distribution – Bar Chart**

<img width="326" height="222" alt="image" src="https://github.com/user-attachments/assets/e845947a-0439-44d4-8bca-f32bef055318" />

***Data*** : `Customer_Age_Group` , `Total_Revenue`  

***Insight*** : 
Visualisasi ini digunakan untuk mengevaluasi kontribusi pendapatan (revenue) berdasarkan kelompok usia, dengan perbandingan terhadap rata-rata keseluruhan melalui garis pembanding horizontal. Analisis ini penting karena mengungkap pola konsumsi spesifik tiap kelompok usia, sehingga manajemen dapat menyesuaikan strategi pemasaran dan penjualan secara lebih presisi.
•	Kelompok Usia 26–35
o	Revenue offline ($465,163) dan online ($480,793) sama-sama berada jauh di atas rata-rata.
o	Menjadi segmen dengan prime spending power: daya beli tinggi, konsumsi stabil, dan adaptif di dua channel.
o	Peran mereka sebagai backbone revenue sangat menonjol, terutama karena konsistensi di seluruh kanal.
•	Kelompok Usia 36–45
o	Offline revenue tertinggi ($473,989), menunjukkan preferensi kuat pada toko fisik.
o	Namun online revenue sangat rendah ($142,512), menandakan adanya kesenjangan digital adoption.
o	Segmen ini menjadi target utama untuk edukasi digital dan perlu didorong transisi ke kanal online.
•	Kelompok Usia 46–55 : Berkontribusi rendah di offline ($205,852), namun justru mendominasi online ($634,251). Fenomena ini menandakan pola selective channeling: mereka beralih ke online untuk pembelian bernilai tinggi, kemungkinan karena faktor kenyamanan dan aksesibilitas.
o	Potensi premium customer kuat, meskipun partisipasi di offline terbatas.
•	Kelompok Usia 18–25
o	Revenue offline ($394,259) sedikit di atas rata-rata, menandakan preferensi terhadap pengalaman langsung di toko.
o	Namun di online hanya $203,373 (jauh di bawah rata-rata), meskipun segmen ini dikenal tech-savvy.
o	Indikasi adanya mismatch strategi (harga, positioning, engagement). Potensi besar, tetapi belum termanfaatkan optimal.

***Managerial Implementation*** : 
•	18–25: Optimalisasi kanal digital dengan strategi promosi berbasis mahasiswa (student discount), gamifikasi, serta bundling produk bernilai rendah. Kanal offline diperkuat melalui pendekatan experiential marketing seperti event interaktif dan demonstrasi produk
•	26–35: Penerapan strategi omnichannel sebagai segmen utama, dengan penekanan pada integrasi program loyalitas lintas kanal, sinkronisasi inventori, serta penyediaan layanan purna jual yang konsisten
•	36–45: Kanal offline diposisikan sebagai sumber pendapatan utama, dengan upaya bertahap untuk mendorong adopsi kanal online melalui strategi edukasi dan pembangunan kepercayaan (trust-building), seperti pemberian garansi, opsi pembayaran COD, serta dukungan purna jual (after-sales). 
•	46–55: Fokus diarahkan pada kanal online dengan pendekatan premium, mencakup penawaran produk eksklusif, layanan pengiriman prioritas, dan konten yang dipersonalisasi, sementara investasi pada kanal offline dapat diminimalkan.





