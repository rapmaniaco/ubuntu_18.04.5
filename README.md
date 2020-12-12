<h3>#Formatar com o cabo de rede desconectado</h3>

<h4>Brave</h4>

```
echo "deb [arch=amd64] https://brave-browser-apt-release.s3.brave.com/ $UBUNTU_CODENAME main" | sudo tee /etc/apt/sources.list.d/brave-browser-release-${UBUNTU_CODENAME}.list
wget -q -O - https://brave-browser-apt-release.s3.brave.com/brave-core.asc | sudo apt-key add -
sudo apt-get update
sudo apt-get install brave-browser brave-keyring
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
add-apt-repository ppa:kdenlive/kdenlive-stable
sudo add-apt-repository ppa:kdenlive/kdenlive-stable
sudo apt-get update
sudo apt-get install kdenlive
```

<h4>Gimp</h4>

```
sudo add-apt-repository ppa:otto-kesselgulasch/gimp
sudo apt update
sudo apt install gimp
```

<h4>Spotify</h4>

```
sudo sh -c "echo 'deb http://repository.spotify.com stable non-free' >> /etc/apt/sources.list.d/spotify.list"
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 931FF8E79F0876134EDDBDCCA87FF9DF48BF1C90
sudo apt-get update
sudo apt-get install spotify-client
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

<h4>Ativar Alt + Tab</h4>
<ul>
<li>https://qastack.com.br/ubuntu/1036248/how-to-separate-opened-windows-in-alttab-switcher-in-ubuntu-18-04</li>
</ul>

Em teclado (Keyboard)
Seção Navegação (navigation)
Desabilitar Switch applications
e Setar como atalho Alt + Tab
Switch windows





