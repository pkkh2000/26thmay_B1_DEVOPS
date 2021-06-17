
  ## Install Docker
```
<ul>
   <li>sudo apt-get update</li>
   <li>sudo apt-get install \
      apt-transport-https \
      ca-certificates \
      curl \
      gnupg \
      lsb-release</li>
   <li>curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg</li>
    <li>echo \
    "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
    $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null</li>
    <li>sudo apt-get update</li>
   <li>sudo apt-get install docker-ce docker-ce-cli containerd.io</li>
</ul>
```
