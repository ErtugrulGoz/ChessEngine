# ChessEngine

Merhabalar, train.ipynb dosyasında model eğitiliyor, predict.ipynb dosyasında eğitilen model çalıştırılıyor.

Uyarı: train.ipynb dosyasında "LIMIT_OF_FILES = min(len(files), 16)" şeklinde bir satır var. Burada ram'iniz boyutuna göre 16'yı artırıp azaltabilirsiniz. Eğer ram'iniz yetmezse hata veriyor. O yüzden iyice hesaplayın ilk denememde ram'in kapasitesinin üstünde bir limit verdim ve 4 saat çalışıp hata verdi.


** Satranç Botuyla Nasıl Oynayabilirim? **

1- predict.ipynb dosyasını açın.

2- "board = Board()
    board"  bloğunu çalıştırın. (satranç tahtasını sıfırlar.)
    
3- Bu kod bloğunun altında iki adet kod bloğu var bunlar:

    "board.push_uci("e2e4")
    
     board" (A)
     
     ve
     
    "best_move = predict_move(board)
    
     board.push_uci(best_move)
     
     board" (B)
     
     bu bloklardan A kendi oynayacağınız hamle. örnek olarak yazan e2e4: e2'deki taşı e4'e oyna anlamına geliyor.
     
     B ise satranç botuna sıra hangi renkte ise o renk için 1 hamle yaptırıyor.
     
     Yani beyaz ile oynamak istiyorsanız A ile hamlenizi oynayın sonra B'yi çalıştırın.
     
     Siyah ile oynayacaksanız da önce B ile bota 1 hamle oynatın sonra A ile hamlenizi oynayın.
     
     Eğer botu kendi kendine oynatmak istiyorsanız B'yi devamlı çalıştırın.
     
Not: her maçtan sonra tahtayı sıfırlamazsanız son oynanan oyundaki tahta ile hamle yapar.
