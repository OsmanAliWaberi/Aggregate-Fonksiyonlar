# Aggregate-Fonksiyonlar

## Merhabalar 

Aşağıdaki sorgu senaryolarını **dvdrental** örnek veri tabanı üzerinden gerçekleştiriniz.

1. **film** tablosunda bulunan **rental_rate** sütunundaki değerlerin ortalaması nedir?


2. **film** tablosunda bulunan filmlerden kaç tanesi 'C' karakteri ile başlar?


3. **film** tablosunda bulunan filmlerden rental_rate değeri 0.99 a eşit olan en uzun (length) film kaç dakikadır?


4. **film** tablosunda bulunan filmlerin uzunluğu 150 dakikadan büyük olanlarına ait kaç farklı replacement_cost değeri vardır?


# Cevaplar :


1. 
```sql


select avg(rental_rate) from film 


```


2. 
```sql


select count(title) from film where title ~~* 'C%'


```


3. 
```sql


select max(length) from film where rental_rate = 0.99

```


4. 
```sql


select count(distinct replacement_cost) from film where length > 150

```