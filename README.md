#  Sürücüsüz Metro Simülasyonu

Bu proje, sürücüsüz bir metro sisteminde en verimli rotaları hesaplamak için geliştirilmiştir. Verilen metro ağı üzerinde **en az aktarma yapan rota** ve **en hızlı rota** hesaplanmaktadır.

##  Kullanılan Teknolojiler ve Kütüphaneler

Proje **Python** dili ile geliştirilmiştir ve aşağıdaki kütüphaneler kullanılmıştır:

- **`heapq`**: A* algoritmasında öncelikli kuyruğu yönetmek için kullanılır.
- **`collections.deque`**: BFS algoritmasında verimli kuyruk işlemleri için kullanılır.

##  Algoritmaların Çalışma Mantığı

### BFS (Breadth-First Search) Algoritması

BFS, **en az aktarma yapan** rotayı bulmak için kullanılır. Algoritma, **katmanlı tarama** prensibiyle çalışarak her istasyonu sırayla genişleyerek inceler.

1. Başlangıç istasyonundan itibaren tüm komşu istasyonlar kuyrukta saklanır.
2. Daha önce ziyaret edilmemiş istasyonlar kuyruğa eklenerek tarama genişletilir.
3. Hedef istasyona ulaşıldığında en kısa (aktarması en az) yol döndürülür.

✅ **Neden BFS?**
BFS, ağı **katmanlar halinde** taradığı için en kısa (en az aktarmalı) yolu garanti eder.

-------------------------------------------------------------------------------------------------------------------------------------------------------------

### A* (A-Star) Algoritması

A* algoritması, **en hızlı rotayı** bulmak için kullanılır. Bir **heuristic (sezgisel)** fonksiyon ile en kısa sürede ulaşılabilecek yolu tahmin eder.

1. **Öncelikli kuyruk** kullanılarak en düşük maliyetli (en hızlı) düğüm öncelikli işlenir.
2. Her istasyonun **tahmini toplam süresi (g + h)** hesaplanarak sıraya eklenir.
3. Hedef istasyona en düşük maliyetle ulaşıldığında en hızlı yol döndürülür.

✅ **Neden A*?** 
A*, Dijkstra’ya kıyasla **daha hızlı** çalışır çünkü yalnızca **en umut verici yolları** genişletir.

##  Örnek Kullanım ve Test Sonuçları
!(images.png)

## Projeyi Geliştirme Fikirleri
Görselleştirme için bir arayüz geliştirilebilir.


