# Manyetik Anahtar

İnsansız sualtı aracının güç sistemini manyetik alan tabanlı olarak güvenli şekilde 
açıp kapatan bir anahtarlama kartıdır. Sistem, bir mıknatısın Hall sensörü üzerindeki 
manyetik alanını algılamasıyla çalışır; mıknatıs yerinde olduğu sürece güç sistemi aktif 
kalır, mıknatıs yerinden ayrıldığında (manyetik alan kaybolduğunda) güç anında kesilir ve 
araç güvenli bir şekilde kapanır.

## Çalışma Mantığı
1. **Hall Sensör** manyetik alan değişimini algılar ve bunu dijital sinyale (D0) dönüştürür
2. Bu sinyal **küçük röleyi** tetikler
3. Küçük röle, **büyük röleyi** (60A anahtarlama kapasiteli) tetikleyerek ana güç hattını kontrol eder
4. Mıknatıs kaldırıldığında sinyal kesilir, röleler devreden çıkar, güç sistemi anında kapanır

Bu tasarım, aracın fiziksel bir temas veya buton gerektirmeden — sadece bir mıknatısla — 
güvenli şekilde açılıp kapatılabilmesini sağlar. Su altı ortamında suya dayanıklı, 
temassız bir açma/kapama çözümüdür.

## Devre Blokları
| Blok | Görevi |
|---|---|
| K1 – LiPo Pil Girişi (XT60) | Ana güç kaynağı girişi |
| F1 – Sigorta | Aşırı akıma karşı hat koruması |
| K2 – Küçük Pil Girişi (XT30) | Hall sensör ve küçük röle için ayrı besleme hattı |
| H1 – Hall Sensör | Manyetik alanı algılayıp dijital sinyale (D0) çevirir |
| R1 – Küçük Röle | Hall sensör sinyaliyle tetiklenir, büyük röleyi sürer |
| R2 – Büyük Röle | Ana güç hattını (60A) anahtarlar |
| K3 – GDK Çıkışı (XT60) | Güç dağıtım kartına giden çıkış |

## Kullanılan Araçlar
Altium Designer 
