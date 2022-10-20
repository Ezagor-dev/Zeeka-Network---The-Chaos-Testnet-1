# Zeeka-Network---The-Chaos-Testnet-1

Merhabalar,

İlk defa node kuran birisi olarak, yeni node kuracaklara da yardımcı olabileceğini düşündüğüm bu rehberi oluşturmak istedim. 

İlk olarak, node kurarken ve kurduktan sonra da iletişim halinde kalabilmek için, Zeeka Network'un [Discord](https://discord.gg/jbtvXSP3) ve [Telegram](https://t.me/ZeekaNetworkTurkish) gruplarına katılmamız gerekiyor.

Node kurmak için öncelikle sunucu kiralanızı tavsiye ederim. Kendi bilgisayarınızdan node kurmak isterseniz; hem fazla elektrik maliyeti hem de fazla depolama maliyeti ile karşı karşıya kalırsınız. 

#Sunucu için, 

https://contabo.com/en/

https://www.digitalocean.com/

ikilisini önerebilirim. Ben bu projede contabo kullandım ve gayet memnunum. Bireysel projelerimde de zaman zaman DigitalOcean kullanmaktayım. 

#Contabo üzerinden VPS kiralaması yaparsanız;

İlk kiralamanızda, ödeme yaptıktan sonra yaklaşık olarak 3 - 5 dakika beklemeniz gerekmektedir. Kısa süre sonra, satın alım yaparken vermiş olduğunuz mail adresinize, giriş yapacağınız panelin linki, kullanıcı adınız ve şifreniz gelmektedir. 

Bu mail sonrası, maildeki bilgiler ile Contabo hesabımıza girelim. 

Your services seçeneğine tıklayalım ve kendi VPS'lerimizi görüntüleyelim. 

Az önce kiralamış olduğumuz VPS'imiz görüntüleniyorsa; artık Node kurulumuna başlayabiliriz. 

#Minimum Gereksinimler

2 GB CPU
4 GB RAM

#İlk Kurulum

sudo apt install -y build-essential libssl-dev cmake

apt install screen

