tclip
=====

��Ҫ
---------------
����ͼƬ�ü����������ص㣺 <br/>
1.�ܽ�������ʶ��ͼƬ�������������Զ���Ϊ��������Ϊ��Ҫ���򣬽����ᱻ�ü����� <br/>
2.�Զ�ʶ��������Ҫ�������ͼƬ��δʶ��������������������ֲ������������ <br/>
�ܶ���֮���Զ�ʶ��ͼƬ�е���Ҫ���򣬲�����ͼƬ�ü�ʱ������Ҫ���� <br/>
Ŀǰ���Ѿ���ʽ���Ա�һ�������ʹ�á�[wanke.etao.com](http://wanke.etao.com) <br/>
<br/>

Ч����ʾ
-----------------------
###����Ч����ʾ
ԭͼ<br/>
![github](https://raw.github.com/exinnet/tclip/master/demo_images/a1.jpg "github")
<br/><br/>
������մ��м��ȡΪ 400 * 225 ��С��ͼƬ��Ч�����£�<br/>
![github](https://raw.github.com/exinnet/tclip/master/demo_images/a2.JPG "github")
<br/><br/>
ʹ��tclip�ü�ͼƬЧ�����£�<br/>
![github](https://raw.github.com/exinnet/tclip/master/demo_images/a3.jpg "github")
<br/>
###����Ч����ʾ
ԭͼ<br/>
![github](https://raw.github.com/exinnet/tclip/master/demo_images/b1.jpg "github")
<br/><br/>
������մ��м��ȡ��Ч�����£�<br/>
![github](https://raw.github.com/exinnet/tclip/master/demo_images/b2.JPG "github")
<br/><br/>
ʹ��tclip�ü�ͼƬЧ�����£�<br/>
![github](https://raw.github.com/exinnet/tclip/master/demo_images/a3.jpg "github")
<br/>

��װ���裺
--------------
###Դ������<br/>
opencv2 ���ص�ַ  [http://www.opencv.org.cn/index.php/Download](http://www.opencv.org.cn/index.php/Download)
<br/>
###��װopencv2 <br/>
����չ������opencv2.0 ֮�ϰ汾����˰�װǰ�Ȱ�װopencv��opencv�İ�װ��������<br/>
yum install gtk+ gtk+-devel pkgconfig libpng zlib libjpeg libtiff cmake <br/>
���� opencv2 ��װ�� <br/>
��ѹ��װ�� <br/>
cd ���밲װ���ļ����ڡ�<br/>
cmake CMakeLists.txt <br/>
make && make install <br/>
vim /etc/profile <br/>
�� unset i ǰ���� <br/>
export PKG_CONFIG_PATH=/usr/lib/pkgconfig/:/usr/local/lib/pkgconfig:$PKG_CONFIG_PATH <br/>
�����˳���ִ���������� <br/>
source /etc/profile <br/>
echo "/usr/local/lib/" > /etc/ld.so.conf.d/opencv.conf <br/>
ldconfig <br/>
<br/>
###��װtclip��չ<br/>
cd ��Դ����Ŀ¼�е�php_ext�ļ��� <br/>
phpize <br/>
./configure <br/>
make <br/>
cp modules/tclip.so �� extension Ŀ¼ <br/>
�޸�php.ini������ extension=tclip.so <br/>
����fpm <br/>
###��װ������<br/>
�����ʹ�������з�ʽ�����Խ������°�װ<br/>
cd ���밲װ��soft�ļ�����<br/>
chmod +x ./tclip.sh <br/>
./tclip.sh <br/>
<br/>

ʹ�÷���˵��
---------------------
��һ�֣���php��ʹ�ø�ʽ��<br/>
tclip(�ļ�ԭ·�����ü����ͼƬ����·�����ü����ͼƬ��ȣ��ü����ͼƬ�߶�)  <br/>
ʾ���� <br/>
$source_file = "/tmp/a.jpg";  <br/>
$dest_file = "/www/a_dest.jpg";  <br/>
$width = 400;  <br/>
$height = 200;  <br/>
tclip($source_file, $dest_file, $width, $height);  <br/>
�ڶ��֣������� <br/>
����˵���� <br/>
-s ԭͼ·�� <br/>
-d �ü����ͼƬ����·�� <br/>
-w �ü����ͼƬ��� <br/>
-h �ü����ͼƬ�߶� <br/>
./tclip -s a.jpg -d a_dest.jpg -w 400 -h 200 <br/>
