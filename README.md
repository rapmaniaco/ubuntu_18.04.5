<h3>#Formatar com o cabo de rede desconectado</h3>

<h4>Brave</h4>

<ul>
<li>https://www.edivaldobrito.com.br/navegador-brave-no-linux-via-snap/</li>
</ul>

```
sudo snap install brave
```

<h4> OBS Studio</h4>

```
sudo add-apt-repository ppa:obsproject/obs-studio
sudo add-apt-repository ppa:kirillshkrogalev/ffmpeg-next
sudo apt-get update
sudo apt-get install obs-studio
```
<h4>VLC</h4>

```
sudo snap install vlc
```

<h4> NVIDIA e TensorFlow</h4>

<ul>
<li>https://github.com/escoladeestudantes/tensorflow_2.0/tree/main/00_instalar_cuda_10.0_cudnn_7.6.4_suporte_gpu</li>
</ul>

<h4> OpenCV com suporte a GPU</h4>

<ul>
<li>https://github.com/escoladeestudantes/opencv/tree/main/15_OpenCV_Install_gpu_support</li>
</ul>

<h4>DLIB - seta suporte a AVX e GPU automaticamente, no segundo caso se CUDA e cuDNN estiverem instalados</h4>

```
git clone https://github.com/davisking/dlib.git
ls
cd dlib-master
python setup.py install
```

<h4>Excluir ambiente virtual</h4>

```
rmvirtualenv my_env
```

<h4>LibreOffice</h4>

```
wget http://tdf.c3sl.ufpr.br/libreoffice/stable/6.4.7/deb/x86_64/LibreOffice_6.4.7_Linux_x86-64_deb.tar.gz -O libreOffice.tar.gz
tar -vzxf libreOffice.tar.gz
cd LibreOffice_*
cd DEBS
sudo dpkg -i *.deb
```

<h4>Kdenlive</h4>

```
sudo add-apt-repository ppa:kdenlive/kdenlive-stable
sudo apt-get update
sudo apt-get install kdenlive
```

<p>Renderizar com GPU.</p>
<ul>
<li>https://www.youtube.com/watch?v=w1jGeJonIxg</li>
</ul>


<h4>Gimp</h4>

```
sudo add-apt-repository ppa:otto-kesselgulasch/gimp
sudo apt update
sudo apt install gimp
```

<h4>Spotify</h4>

<ul>
<li>https://diolinux.com.br/2019/08/como-instalar-o-spotify-no-linux.html</li>
</ul>

```
sudo snap install spotify
```

<h4>Dropbox</h4>

```
wget "http://www.dropbox.com/download/?plat=lnx.x86_64" -O dropbox.tar.gz
sudo tar -xvf dropbox.tar.gz -C /opt/
sudo mv /opt/.dropbox-dist/ /opt/dropbox
sudo ln -sf /opt/dropbox/dropboxd /usr/bin/dropbox
echo -e '[Desktop Entry]\n Version=1.0\n Name=dropbox\n Exec=/opt/dropbox/dropboxd\n Icon=/ \n Type=Application\n Categories=Application' | sudo tee /usr/share/applications/dropbox.desktop

```

<h4>Ativar filtro de ruído no microfone</h4>
<ul>
<li>https://diolinux.com.br/2020/06/cancelamento-de-eco-e-ruido-no-linux.html</li>
</ul>

```
load-module module-echo-cancel aec_args="analog_gain_control=0 digital_gain_control=0" source_name=noiseless
set-default-source noiseless
```

<h4>Corrigir cortes no microfone</h4>
<ul>
<li>https://www.youtube.com/watch?v=1ORKzOr7K1o&t=75s</li>
</ul>

```
sudo nano /etc/pulse/default.pa
```

<p>Procurar essa linha: load-module module-udev-detect</p>
<p>Acrescentar esse comando tsched=0 na mesma.</p>

<h4>Ativar Alt + Tab</h4>
<ul>
<li>https://qastack.com.br/ubuntu/1036248/how-to-separate-opened-windows-in-alttab-switcher-in-ubuntu-18-04</li>
</ul>

Em teclado (Keyboard)
Seção Navegação (navigation)
Desabilitar Switch applications
e Setar como atalho Alt + Tab
Switch windows


<h4>Oracle Virtual Box</h4>
<ul>
<li>https://www.edivaldobrito.com.br/virtualbox-no-linux/</li>
</ul>

```
sudo sh -c 'echo "deb http://download.virtualbox.org/virtualbox/debian $(lsb_release -cs) contrib" >> /etc/apt/sources.list.d/virtualbox.list'
wget -q https://www.virtualbox.org/download/oracle_vbox_2016.asc -O- | sudo apt-key add -
wget -q https://www.virtualbox.org/download/oracle_vbox.asc -O- | sudo apt-key add -
sudo apt-get update
sudo apt-get install virtualbox
```

<h4>Team Viewer</h4>
<ul>
<li>https://linuxize.com/post/how-to-install-teamviewer-on-ubuntu-18-04/</li>
</ul>

```
wget https://download.teamviewer.com/download/linux/teamviewer_amd64.deb
sudo apt install ./teamviewer_amd64.deb
```

<h4>Compartilhar pastas se houver erro</h4>
<ul>
<li>https://qastack.com.br/ubuntu/150028/you-are-not-the-owner-message-when-trying-to-access-folder#:~:text=Est%C3%A1%20dizendo%20que%20voc%C3%AA%20n%C3%A3o,ser%20executadas%20pelo%20root%20superusu%C3%A1rio%20.</li>
</ul>

```
sudo chown -R username /path/to/directory
```
