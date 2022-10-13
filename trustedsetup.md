## Ön Bilgi
- Manta Network kısaca gizlilik odaklı bir proje ve yakın zamanda bir Trusted Setup etkinliği başlattılar ve form kapanana kadar kayıtlar devam edecek. 2 aşamadan oluşacak etkinlikte tamamlayanlara NFT gönderilecek. Bu NFT ileride bizlere ayrıcalık tanıyabilir. Zaten işlemleri de çok uzun sürmüyor.

### Sistem Gereksinimleri
 - Kurulumun kısa sürmesini istiyorsanız yazdığım özelliklerden daha düşük sistem kullanmayın. Zaten işlemi yapıp vps'i sileceğiz. 
 - Ubuntu 20.04
 - 2 CPU
 - 4GB RAM
 - HDD Boyutu Önemli Değil
 
 ### Kayıt Adımı için Kurulum Kodları
 - Tmux kullanacağım, standart ekranda kurulum uzun sürerse Putty bağlantıyı koparıp işlemi yarıda bırakabilir.
 ```
 sudo apt install tmux
 tmux
 ```
 
 ```
 sudo apt update
 sudo apt install pkg-config build-essential libssl-dev curl jq
 curl https://sh.rustup.rs/ -sSf | sh -s -- -y
 source $HOME/.cargo/env
 git clone https://github.com/Manta-Network/manta-rs.git
 cd manta-rs
 cargo run --release --package manta-trusted-setup --all-features --bin groth16_phase2_client register
```
- Bu kodları sırayla girdikten sonra en son bize twitter ve mail adresimizi soruyor. Bunları yazdıktan sonra otomatik olarak bize belirli bilgilerin yer aldığı çıktılar veriyor. Bunların hepsini mutlaka bir not defteri vs. kaydediyorsnuz. Polkadot JS kurup cüzdan oluşturup (https://www.youtube.com/watch?v=xYXrP5dL_hU&t=629s) [BURADAN](https://polkadot.js.org/apps/#/settings/metadata) KMA karşılığı adresinizi öğrenebilirsiniz. Daha sonra [BU FORMU](https://mantanetwork.typeform.com/TrustedSetup) dolduruyoruz. Form doldurulmazsa kayıt tamamlanmaz. Bu işlem bittikten sonra kayıt adımını tamamlamış oluyor ve vps'i silebilirsiniz. 2. adım olan 'Contribution/Katkı' adımı daha başlamadı.
- Manta Network'ün Discord kanalına katılmayı unutmayın: https://discord.gg/rJS2JTxgTb
