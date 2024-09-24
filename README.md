![image](https://github.com/user-attachments/assets/2d97e2d6-1dae-4296-ac16-0f67448a74d1)


 [Website](https://nesa.ai/)<br>
 [Discord](https://discord.gg/nesa)<br>
 [Twitter](https://twitter.com/nesaorg/)<br>
 [Docs](https://docs.nesa.ai/nesa)<br>



# System Requirements
| Components | Minimum Requirements | 
| ------------ | ------------ |
| CPU | 4 Core - 	4 Core - The more cores you have, the better your performance will be |
| RAM | Minimum 4 GB RAM |
| Storage | 50 GB SSD - More space may be needed for future operations |
| GPU | CUDA-enabled GPUs are recommended. CPU mining is available but not valid for all models |


# Let's update the server


```
sudo apt update && sudo apt upgrade -y
sudo apt install jq -y
```



# Docker Installation

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



 *  We need to create an account on [HugginFace](https://huggingface.co/) and get a key
 
 `Settings > Access Tokens > Create New Token > Write`
 
 `(Key'i bir yere kaydedelim, sayfadan çıktıktan sonra bir daha göremezsiniz)`


# Şimdi Script'i çalıştıralım

```
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
