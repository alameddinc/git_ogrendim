# Git Kullanımı - Teknik Sunum

## Git'in Temel Kavramları

### Depo (Repository)
- **Tanım:** Git'te projenizin tüm verilerinin saklandığı merkezi konumdur.
- **Teknik Detaylar:** Repository, `.git` klasörü altında tüm versiyon bilgilerini, dalları, commit geçmişini saklar. `git init` komutu ile yeni bir repository oluşturulur.
- **Komutlar:**
  - `git init`
  - `git clone <repository-url>`
  - `git remote add origin <url>`

### Dallar (Branches)
- **Tanım:** Projenizde farklı özellikler üzerinde aynı anda çalışabilmenizi sağlayan bağımsız geliştirme yollarıdır.
- **Teknik Detaylar:** Branch, projede farklı sürümler oluşturmayı sağlar. `git branch` komutu ile dallar oluşturulabilir ve yönetilebilir.
- **Komutlar:**
  - `git branch <branch-name>`
  - `git checkout <branch-name>`
  - `git merge <branch-name>`

### Commit
- **Tanım:** Yaptığınız değişiklikleri deponuza kaydetmek için kullanılan işlemdir.
- **Teknik Detaylar:** Commit, anlık görüntü oluşturur ve bir SHA-1 hash ile tanımlanır. Değişiklikler `staging area`da tutulur ve `git commit` ile kaydedilir.
- **Komutlar:**
  - `git add <file-name>`
  - `git commit -m "commit mesajı"`
  - `git log`

### Pull & Push
- **Tanım:** Kodları uzak ve yerel depo arasında senkronize etmek için kullanılan işlemlerdir.
- **Teknik Detaylar:** `git pull` komutu uzak depodaki değişiklikleri yerel depoya getirir. `git push` ise yerel değişiklikleri uzak depoya gönderir.
- **Komutlar:**
  - `git pull origin <branch-name>`
  - `git push origin <branch-name>`

## Dallanma Stratejileri

### GitFlow
- **Tanım:** Yazılım projesinin stabilitesini artırmak için geliştirilmiş bir dallanma stratejisidir.
- **Teknik Detaylar:** `master` ve `develop` dallarının yanında `feature`, `release`, ve `hotfix` dalları kullanılır.
- **Komutlar:**
  - `git flow init`
  - `git flow feature start <feature-name>`
  - `git flow release start <version>`

### Trunk-Based Development
- **Tanım:** Tüm geliştiricilerin aynı ana dalı (trunk) kullanarak sürekli entegrasyon yapmalarını sağlar.
- **Teknik Detaylar:** Kısa ömürlü dallar kullanılarak değişiklikler hızlıca ana dala entegre edilir.
- **Komutlar:**
  - `git checkout -b <feature-branch>`
  - `git commit -m "message"`
  - `git push origin <feature-branch>`

## Merge ve Çatışmalar (Conflicts)
- **Tanım:** Farklı dallardaki değişikliklerin birleştirilmesi anlamına gelir.
- **Teknik Detaylar:** Çakışmalar, farklı dallardaki değişikliklerin uyumsuz olması durumunda ortaya çıkar ve çözüm gerektirir.
- **Komutlar:**
  - `git merge <branch-name>`
  - `git merge --abort`
  - `git rebase <branch-name>`

### Örnek Senaryo
- **Senaryo:** İki geliştirici aynı dosya üzerinde çalışıyor ve değişikliklerini aynı anda birleştirmeye çalışıyor.
- **Çözüm:** Çatışma çözümleme araçları (`merge tool`) kullanarak manuel müdahale gerektirebilir. `git mergetool` komutu ile çözümleme yapılabilir.
