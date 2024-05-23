# Git Öğrendim

Bu repo, Git öğrenen insanların katkıda bulunarak isimlerini eklemelerini amaçlamaktadır. Yeni başlayanlar için basit bir Git kullanım pratiği sağlar.

## Nasıl Katkıda Bulunabilirsiniz?

1. Bu repoyu klonlayın:
    ```sh
    git clone https://github.com/alameddinc/git_ogrendim.git
    ```

2. Klonladığınız dizine gidin:
    ```sh
    cd git_ogrendim
    ```

3. Yeni bir branch oluşturun: (branch isminizi github-nickname olarak giriniz)
    ```sh
    git checkout -b <branch-ismi>
    ```

4. `CONTRIBUTORS.md` dosyasını açın ve kendi isminizi ekleyin:
    ```markdown
    - [Adınız Soyadınız](https://github.com/username)
    ```

5. Değişikliklerinizi commit edin:
    ```sh
    git add CONTRIBUTORS.md
    git commit -m "İsmimi CONTRIBUTORS.md dosyasına ekledim"
    ```

6. Değişikliklerinizi yeni branch ile push edin:
    ```sh
    git push origin <branch-ismi>
    ```

7. GitHub üzerinde repo sayfasına gidin ve yeni oluşturduğunuz branch için bir Pull Request (PR) açın.

8. PR'ınız incelendikten sonra merge edilecektir.

## Katkıda Bulunanlar

Katkıda bulunanların listesine [CONTRIBUTORS.md](CONTRIBUTORS.md) dosyasından ulaşabilirsiniz.

## Hata Bildirimi ve Geri Bildirim

Herhangi bir hata veya geri bildirim için lütfen bir Issue açın.

## Lisans

Bu proje [AlameddinC Lisansı](LICENSE) ile lisanslanmıştır.