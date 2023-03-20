# TorWebSite
<h2>Tor Ağında Web Sitesi Oluşturma</h2>
<h3>1. Adım:</h3>
<p>İlk olarak, gerekli paketleri yüklemek için aşağıdaki komutları kullanın:</p>
<pre><code>sudo apt-get update
sudo apt-get install tor nginx apache2 git</code></pre>
<p>Ardından, Tor konfigürasyon dosyasını açmak için aşağıdaki komutu kullanın:</p>
<pre><code>sudo nano /etc/tor/torrc</code></pre>
<p>Açılan dosyada aşağıdaki satırların başındaki "#" işaretlerini kaldırın:</p>
<pre><code>HiddenServiceDir /var/lib/tor/hidden_service/
HiddenServicePort 80 127.0.0.1:80</code></pre>
<img src="https://user-images.githubusercontent.com/72278651/226324171-838c7a10-e1ef-452b-9003-60e13d2a6e44.png" width="550" />
<p>Dosyayı kaydedin ve kapatın.</p>
<hr>
<h3>2. Adım:</h3>
<p>Tor hizmetini yeniden başlatmak ve .onion uzantılı web sitenizin adresini almak için aşağıdaki komutları kullanın:</p>
<pre><code>sudo service tor stop
sudo service tor start
sudo cat /var/lib/tor/hidden_service/hostname</code></pre>
<p>Çıktıda belirtilen adres, .onion uzantılı web sitenizin adresidir.</p>
<p>Web sitenizi oluşturmak için, Apache sunucusunun varsayılan web dizinine dosyalarınızı yükleyebilirsiniz:</p>
<pre><code>sudo cp -r /path/to/your/files/* /var/www/html/</code></pre>
<p>Artık web sitenize Tor ağı üzerinden erişebilirsiniz.</p>
<hr>
<b>Youtube Video:</b>

<p>https://www.youtube.com/watch?v=WmjYg11B1hA</p>
<b style='color:red;'>NOT: Bu kaynak eğitim amaçlıdır. Kötü amaçlarla kullanmayınız. Yapılan işlemlerden kişi sorumludur!</b>

<hr>
