## Ön Bilgi
- Manta Network trusted işleminin 2. aşamasını gerçekleştireceğiz.

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
 cargo run --release --package manta-trusted-setup --all-features --bin groth16_phase2_client contribute
```
- Bu kodları sırayla girdikten sonra en son gelen ekranda önceki aşamadaki yedeklediğimiz kelimeleri soruyor. Bunları girerek işlemi başlatıyoruz. Vidoeda (https://t.co/StxBdV2GRI) işlemler daha açıklamalı bir şekilde bulunmaktadır.
