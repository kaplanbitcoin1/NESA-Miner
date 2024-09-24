![image](https://github.com/user-attachments/assets/2d97e2d6-1dae-4296-ac16-0f67448a74d1)



# Sistem Gereksinimleri
| Bileşenler | Minimum Gereksinimler | 
| ------------ | ------------ |
| CPU | 4 Core - Ne kadar çok çekirdeğe sahipseniz performansınız o denli artacaktır |
| RAM | Minimum 4 GB RAM |
| Storage | 50 GB SSD - İleride işlemler için daha fazla alan gerekebilir |
| GPU | CUDA etkin GPU'lar öneriliyor. CPU madenciliği mevcut fakat tüm modeller için geçerli değil |


# Sunucuyu güncelleyelim


```
sudo apt update && sudo apt upgrade -y
sudo apt install jq -y
```



# Docker yükleyelim

```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io
docker version
```


# Docker Compose

```
VER=$(curl -s https://api.github.com/repos/docker/compose/releases/latest | grep tag_name | cut -d '"' -f 4)
curl -L "https://github.com/docker/compose/releases/download/"$VER"/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

chmod +x /usr/local/bin/docker-compose
docker-compose --version
```



* [HugginFace](https://huggingface.co/) Üzerinden hesap açıp Key almamız gerekiyor. Settings > Access Tokens > Create New Token > Write 
* (Key'i bir yere kaydedelim, sayfadan çıktıktan sonra bir daha göremezsiniz)


# Şimdi Script'i çalıştıralım

```shell
bash <(curl -s https://raw.githubusercontent.com/nesaorg/bootstrap/master/bootstrap.sh)
```

# Sırasıyla

* Wizardy
* Moniker
* Mail adresinizi girin
* Bonus puan almak için: `nesa1pe9wwz9w0hcy54245c0ys6889kekrepf8zkh7f`
* HugginFace üzerinden aldığınız api keyi yazıyoruz
* Keplr cüzdan private key'i girelim ve Yes diyelim, işlem tamamdır

# Node id alıp [Explorer](https://node.nesa.ai/) üzerinden işlemlerinizi kontrol edebilirsiniz.


```
cat ~/.nesa/identity/node_id.id
```


Nesa ufak bir kurulum gif'i hazırlamış göz atabilirsiniz


![gif](https://raw.githubusercontent.com/nesaorg/bootstrap/master/images/bootstrap.gif)
