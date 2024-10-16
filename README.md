# Hotel Booking PowerBI Projesi

Bu proje, ONYX data ile oluşturulan bir POWERBI dashboard örneğidir.

#### Query Editor de Yapılanlar

![image](https://github.com/user-attachments/assets/8b240394-a7e6-4af7-97b7-11c864519167)

arrival_date adında yeni bir merged kolon eklenerek, bu kolonda arrival_date_year, arrival_date_month, arrival_date_day_of_month alanları birleştirildi.

![image](https://github.com/user-attachments/assets/5ccc3b26-a970-4941-a765-5402a0ed7d4b)

With_children adında bir conditinal kolon eklendi. Burada rezervasyon yapanların çocuklu aile mi çocuksuz aile mi olduğuna dair bilgi eklendi.

![image](https://github.com/user-attachments/assets/8e128b1e-b8e4-4bcd-bb7a-138ed7416c9e)

Country isminde yeni bir tablo oluşturuldu ve excele hazırlanan data içine aktarıldı.

![image](https://github.com/user-attachments/assets/965a0f3c-11c5-4d98-a89b-929e71aad76d)

Meal isminde yeni bir tablo oluşturuldu ve excele hazırlanan data içine aktarıldı.

![image](https://github.com/user-attachments/assets/20d36893-4c2c-40d1-ab49-1600e0e0199e)

Data Table ekledim ve bu sayede yıl filtrelerini projeye dahil ettim.

![image](https://github.com/user-attachments/assets/7ef74339-0716-4708-9852-2bf0a2b92eac)

Tablolar arasındaki ilişkiyi düzenledim.


#### DASHBOARD

![image](https://github.com/user-attachments/assets/f29dbf9f-37b7-4bd4-8020-7442f6ec0eaa)


## SAYFA -  OVERVIEW

-	Sağ üstte beyaz olan iki buton navigation bar ile eklendi. Diğer sayfalara erişimi sağlıyor.
-	Yeşil olan Card toolları DAX ile elde edilen sonuçları gösteriyor.


  #### DAX Kodları
  
![image](https://github.com/user-attachments/assets/bb1985b7-5b8f-44d3-81cb-c2c9a9c44e05)

![image](https://github.com/user-attachments/assets/2cfa3c76-896b-4b1e-b6d3-5bb9a1666c28)


```
City Hotel = COUNTROWS(FILTER('hotel_bookings', 'hotel_bookings'[hotel] = "City Hotel" && 'hotel_bookings'[is_canceled]=0))

Resort Hotel = COUNTROWS(FILTER('hotel_bookings', 'hotel_bookings'[hotel] = "Resort Hotel" && 'hotel_bookings'[is_canceled]=0))

```


*is_canceled 0 almamın sebebi iptal olmayan rezervasyonları saymak içindi.

- ikinci sıradaki yıl verisi slicer olarak eklendi. Seçildiğinde raporlar değişiyor.
- alttaki iki rapor da yeni eklediğim meal ve country tabloları kullanılarak görselleştirildi ve kodlar yerine açıklayıcı metinler ile okunabilmesi sağlandı.


## SAYFA – RESORT HOTEL

![image](https://github.com/user-attachments/assets/bf5becea-3eae-47c7-92cb-c6eea377e6af)


-	En üstte yine navigation bar var.
-	İkinci sırada sarı ile gösterilen Card lar DAX formülleri ile elde edilen kısımlar.
-	Grafikler ve yine yıl filtresi.

## SAYFA – CITY HOTEL

![image](https://github.com/user-attachments/assets/a264f4a5-5f9f-4934-8dc2-aefeb8b9cccd)

-	Önceki raporla aynı verileri fakat hotel bilgisini filtreleyerek gösteriyor. Önceki sayfada resort hotele ait bilgiler hesaplanırken, bu sayfada city hotele ait bilgiler hesaplanıyor.

![image](https://github.com/user-attachments/assets/d4f4227c-b7f9-4fc3-a86c-e6f51578641b)

![image](https://github.com/user-attachments/assets/fc0b81f2-df5d-441c-91bf-adc35479d81c)

## ÇIKARIMLAR

![image](https://github.com/user-attachments/assets/a9d3cdc9-7a40-4778-b7ac-37c67a484a12)

Bu grafikten gördüğümüz üzere iki hotelde de oda-kahvaltı tipinde rezervasyonlar çoğunlukla iptal edilmiş. Rezervasyonların daha doğru bir şekilde oluşabilmesi için bu seçeneği konaklama tipinden kaldırabiliriz. Bu şekilde daha doğru rezervasyonlar oluşur.

![image](https://github.com/user-attachments/assets/0dcb4c62-ca56-4c60-a34e-317c06efb9de)

Bu grafikte gördüğümüz üzere ülkelerin rezervasyonlarında değişiklik yapma oranları çok yüksek. Bu grafikten bakılarak %20 nin üzerinde değişiklik yapan ülkelerden misafirler geldiğinde yada rezervasyon yapılırken fiyatları biraz yüksek tutulabilir. Böylece değişiklikler esnasında harcanan emek ve oluşan aksilikler bir nebze giderilebilir.

![image](https://github.com/user-attachments/assets/f4217940-36b5-4835-b928-95bc530651ed)

İki hotelde de çocuksuz ailelerin kalma oranı daha yüksek olduğu görülüyor. Buna bakarak, animasyonlarda yada gece şovlarda yetişkinlere özel aktiviteler artırılabilir. Çocuksuz ailelere özel kampanyalar düzenlenebilir ve misafir sayısı artırılabilir.

![image](https://github.com/user-attachments/assets/fce866c1-da6c-4121-bd91-adbee486a02a)

Yıllık kazanç grafiğine baktığımızda 3 yılda da ağustos ayı en yüksek kazancı sağlamış. Demek ki özellikle ağustos ayında personel arttırılarak ve kampanyalar düzenlenerek daha iyi hizmet anlayışıyla kazançlar artırılabilir.

![image](https://github.com/user-attachments/assets/a0eb5a0a-8494-4f3a-96a4-736096962521)

Yine iki hotelde de ayrı ayrı baktığımızda Haftaiçi kalma oranı daha yüksek. Haftaiçi personelin daha özenli çalışması sağlanarak memnuniyet artırılabilir. 
