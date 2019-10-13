# Skin Image Crawler

This is Skin Image Crawler script written in Python 3.
This script helps to download dermatologic images from google.com and bing.com using 214 keywords of various languages. The keywords in Korean was validated, however, the rest keywords were translated by Google translator (http://translate.google.com). 
It was developed to collect training images for deep learning by Han Seung Seog (whria78@gmail.com).

## Requirement

Python 3 (Anaconda 3) : https://www.anaconda.com/distribution/#download-section


## How to use

<pre><code>
pip install icrawler xlwt six

python skin.py melanoma
python skin.py "acanthosis nigricans"
python skin.py -l
</code></pre>

or

<pre><code>
pip3 install icrawler xlwt six

python3 skin.py melanoma
python3 skin.py "acanthosis nigricans"
python3 skin.py -l
</code></pre>

## Check the result
Check the result at "url_filepath.xls" and "/images".
This script collect with English keyword first, and then with other languages. Images with the same file size are discarded.
For the example of "melanoma", check "melanoma_google" folder first. And then check "melanoma_bing". And results with other languages later. 


## Options
<pre><code>
max_crawling_num=1000
max_thread=3
prohibit_site=['dermnet.com'] 
</code></pre>

*** If website does not allow the use of image even for personal, non-commercial, and reserach purpose, modify line 16 (prohibit_site).


## Result (2019-10-10)

With a single keyword "melanoma", a total of 3034 images are available in 2019-10-10. 
#### https://github.com/whria78/skinimagecrawler/blob/master/result_20191010.csv

There are some duplicated images with different resolution. Try to use Duplicate Photo Finder (https://www.duplicatephotocleaner.com) or other applications to remove the duplicate images.
