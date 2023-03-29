<h1 align="center">Fleek Network Devnet Kurulum Rehberi

## Helo, şuan için devnet aşamasında olan ödülsüz olduğu belirtilen Fleek Network için kurulum yapacağız. Testnet'e geçildiğinde ödüllü olacağı söylenmiş, güncellemeler için bizi takipte kalın. Sağ üstten yıldızlayıp forklamayı unutmayalım. Sorularınız olursa: [LossNode Chat](https://t.me/LossNode)

![image](https://user-images.githubusercontent.com/101462877/228519078-51efde98-f8b9-4e6f-9284-ebcae56d36a5.png)


## Minimum sistem gereksinimleri:
NODE TİPİ | CPU     | RAM      | SSD     |
| ------------- | ------------- | ------------- | -------- |
| Devnet | 4          | 8         | 150GB yeterli  |


## Fleek Network için önemli linkler:
- [Website](https://fleek.xyz/)
- [Twitter](https://twitter.com/fleek_net)
- [Discord](https://discord.gg/fleekxyz)
  
# Kuruluma başlıyoruz. Root yetkisi alın.

```
sudo su
cd $HOME
```
  
## Sunucuyu güncelleyin.

```
sudo apt update && sudo apt upgrade -y
```

## Screen yükleyin.

```
sudo apt install screen -y
```

## Gerekli kütüphaneler.

```
sudo apt-get install build-essential -y
```
```
sudo apt-get install cmake clang pkg-config libssl-dev -y
```
```
sudo apt-get install protobuf-compiler -y
```
```
sudo apt install git -y
```
## Screen açın.

```
screen -S fleek
```

## Rust yükleyin.

```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

![image](https://user-images.githubusercontent.com/101462877/228555170-66d9f8c8-e48b-436c-9d19-2473543fc566.png)

```
source "$HOME/.cargo/env"
```

## Sccache yükleyin.

```
cargo install sccache
```
## Projeyi sunucuya klonluyoruz.
```
git clone https://github.com/fleek-network/ursa.git
cd ursa
```

## Devam.
```
make install
```
