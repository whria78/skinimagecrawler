# Skin Image Crawler

This is Skin Image Crawler script written in Python 3. 

It was developed to collect training images for deep learning by Han Seung Seog (whria78@gmail.com).
This script helps to download dermatologic images from google.com and bing.com using 172 keywords of various languages. The keywords in Korean were validated by Han, however, the rest keywords were translated by Google Translator (http://translate.google.com). We need contribution of the translation. Thank you.


## Requirement

Python 3 (Anaconda 3) : https://www.anaconda.com/distribution/#download-section


## How to use

<pre><code>
pip install icrawler xlwt six

python skin.py melanoma
python skin.py "acanthosis nigricans"
python skin.py -l
python skin.py 0
cf) ABNOM = 0
</code></pre>

or

<pre><code>
pip3 install icrawler xlwt six

python3 skin.py melanoma
python3 skin.py "acanthosis nigricans"
python3 skin.py -l
python3 skin.py 0
cf) ABNOM = 0
</code></pre>

## Check the result
Check the result at "url_filepath.xls" and "/images".

This script collect with English keyword first, and then with other languages. Images with the same file size are discarded.

For the example of "melanoma", check "melanoma_google" folder first. And then check "melanoma_bing". And chek results with other languages later. 


## Options
<pre><code>
max_crawling_num=1000
max_thread=3
use_Korean=True
use_Other_Lang=False
prohibit_site=['dermnet.com'] 
</code></pre>

*** If website does not allow the use of images for any purpose, add the site to the option (prohibit_site).


## Result (2019-10-31)

With a single keyword "melanoma", 683 images were available in 2019-10-31. If you set "Use_Other_Lang=True", you can get over 5000 images. However, the results included a lot of non-clinical images. Because diagnosis cannot be confirmed by search keyword, all images should be annotated manually based on image findings. 
#### https://raw.githubusercontent.com/whria78/skinimagecrawler/master/url_filepath_melanoma_eng_kor_20191031.csv
#### https://raw.githubusercontent.com/whria78/skinimagecrawler/master/url_filepath_melanoma_all_20191031.csv

There are some duplicated images with different resolution. Try to use Duplicate Photo Finder (https://www.duplicatephotocleaner.com) or other algorithm (resize tiny, and convert to binary, and compare the binary) to remove the duplicate images.

