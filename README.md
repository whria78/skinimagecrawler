# Skin Image Crawler

This is Skin Image Crawler script written in Python 3.
This script helps to download dermatologic images from google.com and bing.com using 214 keywords of various languages. The keywords in Korean was validated, however, the rest keywords were translated by Google translator (http://translate.google.com). 
It was developed to collect training images for deep learning.

## Requirement

Python 3 (Anaconda 3) : https://www.anaconda.com/distribution/#download-section


## How to use

<pre><code>
pip install icrawler xlwt six

python skin.py
</code></pre>

or

<pre><code>
pip3 install icrawler xlwt six

python3 skin.py
</code></pre>

Check the result at "url_filepath.xls" and "/images".


## Options
<pre><code>
max_crawling_num=1000
max_thread=4
prohibit_site=['dermnet.com'] 
crawl_melanoma_only=True
</code></pre>

1. By default, this script downloads melanoma images. If you want to download all kinds of skin disorders, modify line 75 (crawl_melanoma_only).
2. If website does not allow the use of image even for personal, non-commercial, and reserach purpose, modify line 74 (prohibit_site).


## Result (2019-10-10)

A total of 3034 images are available in 2019-10-10. 
#### https://github.com/whria78/skinimagecrawler/blob/master/result_20191010.csv

There are some duplicated images with different resolution. Try to use Duplicate Photo Finder (https://www.duplicatephotocleaner.com) or other applications to remove the duplicate images.
