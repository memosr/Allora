<h1 align="center">Allora</h1>

> Gm, yeni bir Node Point > All ile buluşuyoruz.

> Allora'nın worker/price bot'unu kuruyoruz bugün.

> Benzer içerikler sohbetler ve güncellemler için [telegramdayız](https://t.me/RuesAnnouncement).

<details>
  <summary> <h1> Yatırımı hakkında </summary> </h1>

![image](https://github.com/ruesandora/Allora/assets/101149671/2e54ddbb-d33a-4165-9497-78417dc1c523)

</details>

#

<h1 align="center">Donanım</h1>

> Açıkcası ben sunucu almadım, airchains station'umun içine kurdum.

> Yinede donanım olarak minimum `2 CPU 4 RAM` iyidir.

#

<h1 align="center">Kurulum</h1>

```console
# sunucu güncellememiz
sudo apt update & sudo apt upgrade -y

sudo apt install ca-certificates zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev curl git wget make jq build-essential pkg-config lsb-release libssl-dev libreadline-dev libffi-dev gcc screen unzip lz4 -y

sudo apt install python3
sudo apt install python3-pip

# Dockeri yükleyelim
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io

VER=$(curl -s https://api.github.com/repos/docker/compose/releases/latest | grep tag_name | cut -d '"' -f 4)

curl -L "https://github.com/docker/compose/releases/download/"$VER"/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

chmod +x /usr/local/bin/docker-compose

sudo groupadd docker
sudo usermod -aG docker $USER
```

#

```console
# go kurulumu
sudo rm -rf /usr/local/go
curl -L https://go.dev/dl/go1.22.4.linux-amd64.tar.gz | sudo tar -xzf - -C /usr/local
echo 'export PATH=$PATH:/usr/local/go/bin:$HOME/go/bin' >> $HOME/.bash_profile
echo 'export PATH=$PATH:$(go env GOPATH)/bin' >> $HOME/.bash_profile
source .bash_profile
```

#

<h1 align="center">Allora ve Cüzdan kurulumu</h1>

```console
# allora kurulumu
git clone https://github.com/allora-network/allora-chain.git
cd allora-chain && make all

# cüzdan oluşturma

allorad keys add CÜZDAN_İSMİ
# cüzdanınıza bir isim veriniz
# cüzdan import için
allorad keys add CÜZDAN_İSMİ --recover
ardından önceden aldığınız 24 kelimeyi giriniz
````


> Akabinde keplr'a 24 kelimenizi import ediniz 

> Allora ağını keplr'a [buradan](https://explorer.testnet-1.testnet.allora.network/wallet/keplr) ekleyelim.

> Allora dashboard'a [buradan](https://app.allora.network?ref=eyJyZWZlcnJlcl9pZCI6IjBlNWRhMjlmLTc3YjItNDQ2NS1hYTcxLTk0NWI3NjRhMTA0ZiJ9) bağlanıyoruz.

> Allora cüzdanımıza token [buradan](https://faucet.testnet-1.testnet.allora.network/) alıyoruz. Sıraya alıp gönderme yapabiliyor. Direkt token gelmeyebiliyor.

#
