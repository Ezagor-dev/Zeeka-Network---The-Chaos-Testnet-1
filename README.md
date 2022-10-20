## Zeeka-Network---The-Chaos-Testnet-1

Merhabalar,

İlk defa node kuran birisi olarak, yeni node kuracaklara da yardımcı olabileceğini düşündüğüm bu rehberi oluşturmak istedim. 

İlk olarak, node kurarken ve kurduktan sonra da iletişim halinde kalabilmek için, Zeeka Network'un [Discord](https://discord.gg/jbtvXSP3) ve [Telegram](https://t.me/ZeekaNetworkTurkish) gruplarına katılmamız gerekiyor.

Node kurmak için öncelikle sunucu kiralanızı tavsiye ederim. Kendi bilgisayarınızdan node kurmak isterseniz; hem fazla elektrik maliyeti hem de fazla depolama maliyeti ile karşı karşıya kalırsınız. 

## Sunucu kiralamak için: 

* https://contabo.com/en/

* https://www.digitalocean.com/

ikilisini önerebilirim. Ben bu projede contabo kullandım ve gayet memnunum. Bireysel projelerimde de zaman zaman DigitalOcean kullanmaktayım. 

## Contabo üzerinden VPS kiralaması yaparsanız;

İlk kiralamanızda, ödeme yaptıktan sonra yaklaşık olarak 3 - 5 dakika beklemeniz gerekmektedir. Kısa süre sonra, satın alım yaparken vermiş olduğunuz mail adresinize, giriş yapacağınız panelin linki, kullanıcı adınız ve şifreniz gelmektedir. 

Bu mail sonrası, maildeki bilgiler ile Contabo hesabımıza girelim. 

Your services seçeneğine tıklayalım ve kendi VPS'lerimizi görüntüleyelim. 

Az önce kiralamış olduğumuz VPS'imiz görüntüleniyorsa; artık Node kurulumuna başlayabiliriz. 

## Minimum Gereksinimler

* 2 GB CPU
* 4 GB RAM

## İlk Kurulum(Cmake)
```
sudo apt install -y build-essential libssl-dev cmake
```
```
apt install screen
```

## Rust kurulum

Kurulum esnasında;

* 1- Proceed with installation (default)
* 2- Customize installation
* 3- Cancel installation

yazıları karşınıza gelecek.

1 yazıp enterlayarak devam ediyoruz.

<img width="318" alt="image" src="https://user-images.githubusercontent.com/45847677/197010890-bb4e8a4e-7444-4b5c-9067-e647af3e27ca.png">


## Bazuka Yüklemesi

```
apt install git
```
```
git clone https://github.com/zeeka-network/bazuka
```
```
source "$HOME/.cargo/env"
```

## Path Kurulumu

```
cd bazuka
sudo apt install -y g++
cargo install --path .
```

* path sonrası nokta "." koymayı unutmayalım.


## Screen Kurulumu
```
screen -S bazuka
```

## Seed Aşaması ( Önemli )

* Bu komutta `Ezagor` yazdığım yeri, kendi istediğiniz bir isim/nickname ile değiştirin ve kaydedin. Seed, node taşıma işlemlerinde gereklidir.

```
bazuka init --seed Ezagor --network chaos --node 127.0.0.1:8765
```

## Node Kurulumu

* En çok hata yapılan yerlerin başında yer alıyor. Bu nedenle lütfen dikkatli olalım. 

* Aşağıdaki komut satırlarının ilkinde yer alan `123.456.789` yerine, VPS'inize ait olan IP adresi yazılmalıdır. Lütfen IP adresinizi yazarken port numarasını değiştirmeyin.(`8765`)

* Komut satırının en sonunda yer alan `--discord-handle "Ezagor#9245"` içerisinde yer alan tırkak işaretli bölüme(" "), kendi discord isminizi girin.

* Zeeka discord adresine katılmadıysanız lütfen katılıp bu işlemleri öyle gerçekleştirin.  

```
bazuka node --listen 0.0.0.0:8765 --external 123.456.789:8765 \
  --network chaos --db ~/.bazuka-chaos --bootstrap 152.228.155.120:8765 \
  --discord-handle "Ezagor#9245"
```

## Çıktılar

* Node kuran birçok kişinin merakla sordukları ekranları sizinle paylaşmak isterim. 

## "Terminal'e yanlışlıkla yazı yazdım" Durumu

![image](https://user-images.githubusercontent.com/45847677/197014561-01f711d4-789b-44be-ba64-0bb6c390813c.png)

* Korkmanızı gerektiren hiçbir sıkıntı yoktur. Yazınızı, terminal üzerinden silerseniz; loglar aşağıya doğru akmaya devam edecektir.

## ERROR Bazuka Heartbeat Hatası Alıyorum Durumu

![image](https://user-images.githubusercontent.com/45847677/197015069-1fec2b96-579a-4da0-bf67-ea71c03ac9d9.png)

* Korkmanızı gerektiren hiçbir sıkıntı yoktur. Mevcut durumda bu yazıyı görmezden gelebilirsiniz. 

## Tüm Değerler 0 Gözüküyor Durumu

![image](https://user-images.githubusercontent.com/45847677/197015990-d9c02499-986c-40dd-8cbe-abb950dc8a6a.png)


* Bu hatayı alan kullanıcılar, Node kurulumu sırasında kendi IP adresini ve Discord adresini yazdığından emin olmalı ve ayrıca `:8765` port numarasını değiştirmemelilerdir.

## Doğru Node Kurulumu Sonrası Beklenen Output:

![image](https://user-images.githubusercontent.com/45847677/197016098-0f31a12a-ec98-4e64-864f-aeeb58d7c2ab.png)

## Node kurdum ama çalışıyor mu:

* Screen içerisindeyken,  ```bazuka status``` komutunu çalıştırın.

## Komutlar:

* ``` bazuka deposit``` - Deposit 
* ``` bazuka help``` - Prints this message or the help of the given subcommand(s)
* ``` bazuka init``` - Initialize node/wallet
* ``` bazuka node``` - Run node
* ``` bazuka rsend``` - Send funds through a regular-transaction
* ``` bazuka status``` - Get status of a node ```
* ``` bazuka withdraw``` - Withdraw funds from a Zero-Contract
* ``` bazuka zsend``` - Send funds through a zero-transaction



## ps:
* Sorunuz olursa discord üzerinden ya da telegram üzerinden bana ya da grup üzerinden arkadaşlara sorabilirsiniz. 

* Explorer takibi için : http://152.228.155.120:8000/?page=1 linki kullanılabilir.
