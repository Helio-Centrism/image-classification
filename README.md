# image-classification

Open In Colab
In [ ]:
!pip install ipython-autotime
%load_ext autotime
Collecting ipython-autotime
  Downloading https://files.pythonhosted.org/packages/b4/c9/b413a24f759641bc27ef98c144b590023c8038dfb8a3f09e713e9dff12c1/ipython_autotime-0.3.1-py2.py3-none-any.whl
Requirement already satisfied: ipython in /usr/local/lib/python3.7/dist-packages (from ipython-autotime) (5.5.0)
Requirement already satisfied: pickleshare in /usr/local/lib/python3.7/dist-packages (from ipython->ipython-autotime) (0.7.5)
Requirement already satisfied: setuptools>=18.5 in /usr/local/lib/python3.7/dist-packages (from ipython->ipython-autotime) (54.1.2)
Requirement already satisfied: simplegeneric>0.8 in /usr/local/lib/python3.7/dist-packages (from ipython->ipython-autotime) (0.8.1)
Requirement already satisfied: pexpect; sys_platform != "win32" in /usr/local/lib/python3.7/dist-packages (from ipython->ipython-autotime) (4.8.0)
Requirement already satisfied: pygments in /usr/local/lib/python3.7/dist-packages (from ipython->ipython-autotime) (2.6.1)
Requirement already satisfied: prompt-toolkit<2.0.0,>=1.0.4 in /usr/local/lib/python3.7/dist-packages (from ipython->ipython-autotime) (1.0.18)
Requirement already satisfied: decorator in /usr/local/lib/python3.7/dist-packages (from ipython->ipython-autotime) (4.4.2)
Requirement already satisfied: traitlets>=4.2 in /usr/local/lib/python3.7/dist-packages (from ipython->ipython-autotime) (5.0.5)
Requirement already satisfied: ptyprocess>=0.5 in /usr/local/lib/python3.7/dist-packages (from pexpect; sys_platform != "win32"->ipython->ipython-autotime) (0.7.0)
Requirement already satisfied: six>=1.9.0 in /usr/local/lib/python3.7/dist-packages (from prompt-toolkit<2.0.0,>=1.0.4->ipython->ipython-autotime) (1.15.0)
Requirement already satisfied: wcwidth in /usr/local/lib/python3.7/dist-packages (from prompt-toolkit<2.0.0,>=1.0.4->ipython->ipython-autotime) (0.2.5)
Requirement already satisfied: ipython-genutils in /usr/local/lib/python3.7/dist-packages (from traitlets>=4.2->ipython->ipython-autotime) (0.2.0)
Installing collected packages: ipython-autotime
Successfully installed ipython-autotime-0.3.1
time: 2.29 ms (started: 2021-03-30 14:30:32 +00:00)
In [ ]:
# Data :Images 
#Use Python libraries to scrape the images (Using)
time: 1.71 ms (started: 2021-03-30 14:31:01 +00:00)
In [ ]:
!pip install bing-image-downloader
Collecting bing-image-downloader
  Downloading https://files.pythonhosted.org/packages/0d/bf/537a61030b84ae4cd5022d5c7b014fd9bc3ce7c02358919153a6658a61d3/bing_image_downloader-1.0.4-py3-none-any.whl
Installing collected packages: bing-image-downloader
Successfully installed bing-image-downloader-1.0.4
time: 3.13 s (started: 2021-03-30 14:31:31 +00:00)
In [ ]:
!mkdir images
time: 120 ms (started: 2021-03-30 14:32:19 +00:00)
In [ ]:
from bing_image_downloader import downloader
downloader.download("rugby leather ball",limit=30,output_dir='images',
                    adult_filter_off=True)

[!!]Indexing page: 1

[%] Indexed 12 Images on Page 1.

===============================================

[%] Downloading Image #1 from https://cdn.notonthehighstreet.com/system/product_images/images/000/393/351/original_CF016852.jpg
[%] File Downloaded !

[%] Downloading Image #2 from http://cdn.shopify.com/s/files/1/0788/5979/products/mvp-leather-balls-heritage-leather-rugby-ball-1_1024x1024.jpg?v=1550134680
[%] File Downloaded !

[%] Downloading Image #3 from https://www.john-woodbridge.com/1536-tm_large_default/leather-vintage-football-allen-1938.jpg
[%] File Downloaded !

[%] Downloading Image #4 from https://images.antiquesatlas.com/dealer-stock-images/puckeringsantiques/Antique_Novelty_Travel_Inkwell_as584a1568z-3.jpg
[%] File Downloaded !

[%] Downloading Image #5 from http://cdn.shopify.com/s/files/1/0020/1025/1324/products/32p_black_1024x.png?v=1534865418
[%] File Downloaded !

[%] Downloading Image #6 from https://cdn.thinglink.me/api/image/586569159714799617/1240/10/scaletowidth
[%] File Downloaded !

[%] Downloading Image #7 from https://www.upfrontcricket.com/media/catalog/product/cache/1/image/9df78eab33525d08d6e5fb8d27136e95/j/n/jnrclub_cb_edited-2.jpg
[%] File Downloaded !

[%] Downloading Image #8 from https://media.istockphoto.com/photos/wooden-cricket-bat-and-ball-on-a-white-background-picture-id505125296?k=6&amp;m=505125296&amp;s=612x612&amp;w=0&amp;h=SwBPWBfK8e2UHz6r8G0_-A5nRp13LVeGPr9vwla3FAI=
[%] File Downloaded !

[%] Downloading Image #9 from https://www.prodirectrugby.com/productimages/V3_1_Main/82143.jpg
[!] Issue getting: https://www.prodirectrugby.com/productimages/V3_1_Main/82143.jpg
[!] Error:: HTTP Error 403: Forbidden
[%] Downloading Image #9 from https://www.prodirectrugby.com/productimages/V3_1_Main/201596_Main_Thumb_0419944.jpg
[!] Issue getting: https://www.prodirectrugby.com/productimages/V3_1_Main/201596_Main_Thumb_0419944.jpg
[!] Error:: HTTP Error 403: Forbidden
[%] Downloading Image #9 from https://abclive1.s3.amazonaws.com/efe3ebc9-f32d-4915-b7bc-fbbbb13bed2f/productimage/P-BGG7___2___L.jpg
[%] File Downloaded !

[%] Downloading Image #10 from https://www.prodirectrugby.com/productimages/V3_1_Main/54935.jpg
[!] Issue getting: https://www.prodirectrugby.com/productimages/V3_1_Main/54935.jpg
[!] Error:: HTTP Error 403: Forbidden


[!!]Indexing page: 2

[%] Indexed 12 Images on Page 2.

===============================================

[%] Downloading Image #10 from https://sportantiques.co.uk/pub/media/catalog/product/2/5/sportantiques-388204978300.jpg
[%] File Downloaded !

[%] Downloading Image #11 from http://clipart-library.com/image_gallery/n1570522.png
[%] File Downloaded !

[%] Downloading Image #12 from https://www.john-woodbridge.com/1020-tm_thickbox_default/1950s-football.jpg
[%] File Downloaded !

[%] Downloading Image #13 from https://img0.etsystatic.com/000/0/5219063/il_fullxfull.22734302.jpg
[%] File Downloaded !

[%] Downloading Image #14 from https://resources.stuff.co.nz/content/dam/images/1/c/m/1/z/u/image.related.StuffLandscapeSixteenByNine.1420x800.1cm0lm.png/1467325338558.jpg
[%] File Downloaded !

[%] Downloading Image #15 from https://cdn.shopify.com/s/files/1/0226/2169/products/Teak_Basketball_02_1024x1024.jpg?v=1568214929
[%] File Downloaded !

[%] Downloading Image #16 from https://static.vecteezy.com/system/resources/previews/000/094/728/original/rugby-pitch-vector.jpg
[%] File Downloaded !

[%] Downloading Image #17 from https://sportantiques.co.uk/pub/media/catalog/product/2/5/sportantiques-388204969606.jpg
[%] File Downloaded !

[%] Downloading Image #18 from https://91b6be3bd2294a24b7b5-da4c182123f5956a3d22aa43eb816232.ssl.cf1.rackcdn.com/contentItem-718381-4539004-koydcm2qn2ye1-or.jpg
[%] File Downloaded !

[%] Downloading Image #19 from https://avicii.ca/wp-content/uploads/2020/10/CLOTHING-STORE-FOR-MEN-WOMEN-KIDS-NEARBY-AVICII.CA_-3.jpg
[%] File Downloaded !

[%] Downloading Image #20 from https://thumbs.dreamstime.com/z/cartoon-sport-balls-25573001.jpg
[%] File Downloaded !

[%] Downloading Image #21 from https://www.prodirectrugby.com/productimages/V3_1_Gallery_1/62355.jpg
[!] Issue getting: https://www.prodirectrugby.com/productimages/V3_1_Gallery_1/62355.jpg
[!] Error:: HTTP Error 403: Forbidden


[!!]Indexing page: 3

[%] Indexed 11 Images on Page 3.

===============================================

[%] Downloading Image #21 from http://cdn.shopify.com/s/files/1/0788/5979/products/mvp-leather-balls-heritage-leather-rugby-ball-1_1024x1024.jpg?v=1550134680
[%] File Downloaded !

[%] Downloading Image #22 from https://www.john-woodbridge.com/1536-tm_large_default/leather-vintage-football-allen-1938.jpg
[%] File Downloaded !

[%] Downloading Image #23 from https://images.antiquesatlas.com/dealer-stock-images/puckeringsantiques/Antique_Novelty_Travel_Inkwell_as584a1568z-3.jpg
[%] File Downloaded !

[%] Downloading Image #24 from http://cdn.shopify.com/s/files/1/0020/1025/1324/products/32p_black_1024x.png?v=1534865418
[%] File Downloaded !

[%] Downloading Image #25 from https://cdn.thinglink.me/api/image/586569159714799617/1240/10/scaletowidth
[%] File Downloaded !

[%] Downloading Image #26 from https://www.upfrontcricket.com/media/catalog/product/cache/1/image/9df78eab33525d08d6e5fb8d27136e95/j/n/jnrclub_cb_edited-2.jpg
[%] File Downloaded !

[%] Downloading Image #27 from https://media.istockphoto.com/photos/wooden-cricket-bat-and-ball-on-a-white-background-picture-id505125296?k=6&amp;m=505125296&amp;s=612x612&amp;w=0&amp;h=SwBPWBfK8e2UHz6r8G0_-A5nRp13LVeGPr9vwla3FAI=
[%] File Downloaded !

[%] Downloading Image #28 from https://www.prodirectrugby.com/productimages/V3_1_Main/82143.jpg
[!] Issue getting: https://www.prodirectrugby.com/productimages/V3_1_Main/82143.jpg
[!] Error:: HTTP Error 403: Forbidden
[%] Downloading Image #28 from https://www.prodirectrugby.com/productimages/V3_1_Main/201596_Main_Thumb_0419944.jpg
[!] Issue getting: https://www.prodirectrugby.com/productimages/V3_1_Main/201596_Main_Thumb_0419944.jpg
[!] Error:: HTTP Error 403: Forbidden
[%] Downloading Image #28 from https://abclive1.s3.amazonaws.com/efe3ebc9-f32d-4915-b7bc-fbbbb13bed2f/productimage/P-BGG7___2___L.jpg
[%] File Downloaded !

[%] Downloading Image #29 from https://www.prodirectrugby.com/productimages/V3_1_Main/54935.jpg
[!] Issue getting: https://www.prodirectrugby.com/productimages/V3_1_Main/54935.jpg
[!] Error:: HTTP Error 403: Forbidden


[!!]Indexing page: 4

[%] Indexed 10 Images on Page 4.

===============================================

[%] Downloading Image #29 from https://www.john-woodbridge.com/1536-tm_large_default/leather-vintage-football-allen-1938.jpg
[%] File Downloaded !

[%] Downloading Image #30 from https://images.antiquesatlas.com/dealer-stock-images/puckeringsantiques/Antique_Novelty_Travel_Inkwell_as584a1568z-3.jpg
[%] File Downloaded !



[%] Done. Downloaded 30 images.

===============================================

time: 18.9 s (started: 2021-03-30 14:33:29 +00:00)
In [ ]:
from bing_image_downloader import downloader
downloader.download("aeroplane",limit=30,output_dir='images',
                    adult_filter_off=True)

[!!]Indexing page: 1

[%] Indexed 12 Images on Page 1.

===============================================

[%] Downloading Image #1 from https://i.ytimg.com/vi/qz1RREH-IBo/maxresdefault.jpg
[%] File Downloaded !

[%] Downloading Image #2 from https://www.masterwishmakers.com/wp-content/uploads/2014/08/kids-airplane-room.jpg
[%] File Downloaded !

[%] Downloading Image #3 from http://i.ytimg.com/vi/_hSrNMX5Fig/maxresdefault.jpg
[%] File Downloaded !

[%] Downloading Image #4 from https://hative.com/wp-content/uploads/2014/03/transport-paper-roll-crafts/9-homemade-airplanes.JPG
[%] File Downloaded !

[%] Downloading Image #5 from https://i.ytimg.com/vi/iGtZHHj2w4U/maxresdefault.jpg
[%] File Downloaded !

[%] Downloading Image #6 from https://www.fonewalls.com/wp-content/uploads/1242x2688-Background-HD-Wallpaper-024-300x649.jpg
[%] File Downloaded !

[%] Downloading Image #7 from https://i.ytimg.com/vi/7iOOiYmSOt8/maxresdefault.jpg
[%] File Downloaded !

[%] Downloading Image #8 from https://i.ytimg.com/vi/LMTcQ8f1QO4/maxresdefault.jpg
[%] File Downloaded !

[%] Downloading Image #9 from https://cdn.iflscience.com/images/6f6cc652-bc59-526d-8a77-d79606443798/default-1464369623-3648-why-do-all-airplane-windows-have-a-tiny-hole-in-them.jpg
[%] File Downloaded !

[%] Downloading Image #10 from https://i.pinimg.com/736x/dd/dd/97/dddd97563775fde9013f4978de7cf96e--bad-cockpit.jpg
[%] File Downloaded !

[%] Downloading Image #11 from http://static.soposted.com/uploads/2016/05/First_BodyBuilder.jpg
[%] File Downloaded !

[%] Downloading Image #12 from https://www.plungecreations.co.uk/wp-content/uploads/File-31-07-2017-19-29-01.jpg
[%] File Downloaded !



[!!]Indexing page: 2

[%] Indexed 12 Images on Page 2.

===============================================

[%] Downloading Image #13 from https://i.ytimg.com/vi/qz1RREH-IBo/maxresdefault.jpg
[%] File Downloaded !

[%] Downloading Image #14 from https://www.masterwishmakers.com/wp-content/uploads/2014/08/kids-airplane-room.jpg
[%] File Downloaded !

[%] Downloading Image #15 from http://i.ytimg.com/vi/_hSrNMX5Fig/maxresdefault.jpg
[%] File Downloaded !

[%] Downloading Image #16 from https://hative.com/wp-content/uploads/2014/03/transport-paper-roll-crafts/9-homemade-airplanes.JPG
[%] File Downloaded !

[%] Downloading Image #17 from https://i.ytimg.com/vi/iGtZHHj2w4U/maxresdefault.jpg
[%] File Downloaded !

[%] Downloading Image #18 from https://www.fonewalls.com/wp-content/uploads/1242x2688-Background-HD-Wallpaper-024-300x649.jpg
[%] File Downloaded !

[%] Downloading Image #19 from https://i.ytimg.com/vi/7iOOiYmSOt8/maxresdefault.jpg
[%] File Downloaded !

[%] Downloading Image #20 from https://i.ytimg.com/vi/LMTcQ8f1QO4/maxresdefault.jpg
[%] File Downloaded !

[%] Downloading Image #21 from https://cdn.iflscience.com/images/6f6cc652-bc59-526d-8a77-d79606443798/default-1464369623-3648-why-do-all-airplane-windows-have-a-tiny-hole-in-them.jpg
[%] File Downloaded !

[%] Downloading Image #22 from https://i.pinimg.com/736x/dd/dd/97/dddd97563775fde9013f4978de7cf96e--bad-cockpit.jpg
[%] File Downloaded !

[%] Downloading Image #23 from http://static.soposted.com/uploads/2016/05/First_BodyBuilder.jpg
[%] File Downloaded !

[%] Downloading Image #24 from https://www.plungecreations.co.uk/wp-content/uploads/File-31-07-2017-19-29-01.jpg
[%] File Downloaded !



[!!]Indexing page: 3

[%] Indexed 11 Images on Page 3.

===============================================

[%] Downloading Image #25 from https://www.masterwishmakers.com/wp-content/uploads/2014/08/kids-airplane-room.jpg
[%] File Downloaded !

[%] Downloading Image #26 from http://i.ytimg.com/vi/_hSrNMX5Fig/maxresdefault.jpg
[%] File Downloaded !

[%] Downloading Image #27 from https://hative.com/wp-content/uploads/2014/03/transport-paper-roll-crafts/9-homemade-airplanes.JPG
[%] File Downloaded !

[%] Downloading Image #28 from https://i.ytimg.com/vi/iGtZHHj2w4U/maxresdefault.jpg
[%] File Downloaded !

[%] Downloading Image #29 from https://www.fonewalls.com/wp-content/uploads/1242x2688-Background-HD-Wallpaper-024-300x649.jpg
[%] File Downloaded !

[%] Downloading Image #30 from https://i.ytimg.com/vi/7iOOiYmSOt8/maxresdefault.jpg
[%] File Downloaded !



[%] Done. Downloaded 30 images.

===============================================

time: 7.32 s (started: 2021-03-30 14:37:08 +00:00)
In [ ]:
from bing_image_downloader import downloader
downloader.download("cruise",limit=30,output_dir='images',
                    adult_filter_off=True)

[!!]Indexing page: 1

[%] Indexed 12 Images on Page 1.

===============================================

[%] Downloading Image #1 from https://www.canadianaffair.com/images/canada/british-columbia/vancouver/VAN018/fairmont-hotel-vancouver/gall-e/max/yvrcp-exterior-003.jpg
[%] File Downloaded !

[%] Downloading Image #2 from https://thumbs.dreamstime.com/x/pharaoh-ramses-ii-ancient-king-egypt-1388113.jpg
[%] File Downloaded !

[%] Downloading Image #3 from http://www.tourismbonaire.com/includes/images/gallery/BonaireCaribbean_24.jpg
[%] File Downloaded !

[%] Downloading Image #4 from http://www.disneyeveryday.com/wp-content/uploads/2015/11/FinnTFA.jpg
[%] File Downloaded !

[%] Downloading Image #5 from https://www.hdwallpapers.in/download/godafoss_waterfalls_iceland-1280x800.jpg
[%] File Downloaded !

[%] Downloading Image #6 from http://funnypost.in/wp-content/uploads/2016/08/Funny-Pic-12-560x994.jpg
[%] File Downloaded !

[%] Downloading Image #7 from http://www.movienewz.com/img/gallery/upside-down/photos/upside_down_2.jpg
[%] File Downloaded !

[%] Downloading Image #8 from https://www.wdwinfo.com/wdwinfo/Resorts/gaylordpalms/images/photos-gallery/Emerald_Room.jpg
[%] File Downloaded !

[%] Downloading Image #9 from https://cdn.shopify.com/s/files/1/0923/4522/products/32824-1_600x.jpg?v=1488888494
[%] File Downloaded !

[%] Downloading Image #10 from http://classymommy.com/wp-content/uploads/2015/08/IMG_0598.jpg
[%] File Downloaded !

[%] Downloading Image #11 from https://www.hdwallpapers.in/download/android_marshmallow_pyramid-1920x1200.jpg
[%] File Downloaded !

[%] Downloading Image #12 from http://www.movienewz.com/img/gallery/wild/posters/wild-movie-poster-1.jpg
[%] File Downloaded !



[!!]Indexing page: 2

[%] Indexed 12 Images on Page 2.

===============================================

[%] Downloading Image #13 from https://www.canadianaffair.com/images/canada/british-columbia/vancouver/VAN018/fairmont-hotel-vancouver/gall-e/max/yvrcp-exterior-003.jpg
[%] File Downloaded !

[%] Downloading Image #14 from https://thumbs.dreamstime.com/x/pharaoh-ramses-ii-ancient-king-egypt-1388113.jpg
[%] File Downloaded !

[%] Downloading Image #15 from http://www.tourismbonaire.com/includes/images/gallery/BonaireCaribbean_24.jpg
[%] File Downloaded !

[%] Downloading Image #16 from http://www.disneyeveryday.com/wp-content/uploads/2015/11/FinnTFA.jpg
[%] File Downloaded !

[%] Downloading Image #17 from https://www.hdwallpapers.in/download/godafoss_waterfalls_iceland-1280x800.jpg
[%] File Downloaded !

[%] Downloading Image #18 from http://funnypost.in/wp-content/uploads/2016/08/Funny-Pic-12-560x994.jpg
[%] File Downloaded !

[%] Downloading Image #19 from http://www.movienewz.com/img/gallery/upside-down/photos/upside_down_2.jpg
[%] File Downloaded !

[%] Downloading Image #20 from https://www.wdwinfo.com/wdwinfo/Resorts/gaylordpalms/images/photos-gallery/Emerald_Room.jpg
[%] File Downloaded !

[%] Downloading Image #21 from https://cdn.shopify.com/s/files/1/0923/4522/products/32824-1_600x.jpg?v=1488888494
[%] File Downloaded !

[%] Downloading Image #22 from http://classymommy.com/wp-content/uploads/2015/08/IMG_0598.jpg
[%] File Downloaded !

[%] Downloading Image #23 from https://www.hdwallpapers.in/download/android_marshmallow_pyramid-1920x1200.jpg
[%] File Downloaded !

[%] Downloading Image #24 from http://www.movienewz.com/img/gallery/wild/posters/wild-movie-poster-1.jpg
[%] File Downloaded !



[!!]Indexing page: 3

[%] Indexed 11 Images on Page 3.

===============================================

[%] Downloading Image #25 from http://www.tourismbonaire.com/includes/images/gallery/BonaireCaribbean_24.jpg
[%] File Downloaded !

[%] Downloading Image #26 from https://cdn.shopify.com/s/files/1/0923/4522/products/32824-1_600x.jpg?v=1488888494
[%] File Downloaded !

[%] Downloading Image #27 from https://www.hdwallpapers.in/download/godafoss_waterfalls_iceland-1280x800.jpg
[%] File Downloaded !

[%] Downloading Image #28 from http://www.movienewz.com/img/gallery/upside-down/photos/upside_down_2.jpg
[%] File Downloaded !

[%] Downloading Image #29 from https://www.wdwinfo.com/wdwinfo/Resorts/gaylordpalms/images/photos-gallery/Emerald_Room.jpg
[%] File Downloaded !

[%] Downloading Image #30 from https://www.hdwallpapers.in/download/android_marshmallow_pyramid-1920x1200.jpg
[%] File Downloaded !



[%] Done. Downloaded 30 images.

===============================================

time: 12.7 s (started: 2021-03-30 14:39:52 +00:00)
In [ ]:
# Preprocessing
# 1. Resize
# 2. Flatten

import os
import matplotlib.pyplot as plt
import numpy as np
from skimage.io import imread
from skimage.transform import resize

target = []
images = []
flat_data = []

DATADIR = '/content/images'
CATEGORIES = ['rugby leather ball','aeroplane','cruise']

for category in CATEGORIES:
  class_num = CATEGORIES.index(category) # Label Encoding the values
  path = os.path.join(DATADIR,category) # Create path to use all the images
  for img in os.listdir(path):
    img_array = imread(os.path.join(path,img))
    #print(img_array.shape)
    #plt.imshow(img_array)
    img_resized = resize(img_array,(150,150,3)) # Normalizes the value from 0 to 1
    flat_data.append(img_resized.flatten())
    images.append(img_resized)
    target.append(class_num)

flat_data = np.array(flat_data)
target = np.array(target)
images = np.array(images)
time: 19.8 s (started: 2021-03-30 14:41:58 +00:00)
In [ ]:
len(flat_data[0])
Out[ ]:
67500
time: 4.63 ms (started: 2021-03-30 14:42:40 +00:00)
In [ ]:
150*150*3
Out[ ]:
67500
time: 4.48 ms (started: 2021-03-30 14:43:00 +00:00)
In [ ]:
target
Out[ ]:
array([0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0,
       0, 0, 0, 0, 0, 0, 0, 0, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1,
       1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 2, 2, 2, 2, 2, 2,
       2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2,
       2, 2])
time: 8.39 ms (started: 2021-03-30 14:43:11 +00:00)
In [ ]:
unique,count = np.unique(target,return_counts=True)
plt.bar(CATEGORIES,count)
Out[ ]:
<BarContainer object of 3 artists>

time: 166 ms (started: 2021-03-30 14:43:48 +00:00)
In [ ]:
# Split data into Training and testing
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(flat_data,target,
                                  test_size=0.3,random_state=109)
time: 233 ms (started: 2021-03-30 14:44:13 +00:00)
In [ ]:
from sklearn.model_selection import GridSearchCV
from sklearn import svm
param_grid = [
              {'C':[1,10,100,1000],'kernel':['linear']},
              {'C':[1,10,100,1000],'gamma':[0.001,0.0001],'kernel':['rbf']},
]

svc = svm.SVC(probability=True)
clf = GridSearchCV(svc,param_grid)
clf.fit(x_train,y_train)
Out[ ]:
GridSearchCV(cv=None, error_score=nan,
             estimator=SVC(C=1.0, break_ties=False, cache_size=200,
                           class_weight=None, coef0=0.0,
                           decision_function_shape='ovr', degree=3,
                           gamma='scale', kernel='rbf', max_iter=-1,
                           probability=True, random_state=None, shrinking=True,
                           tol=0.001, verbose=False),
             iid='deprecated', n_jobs=None,
             param_grid=[{'C': [1, 10, 100, 1000], 'kernel': ['linear']},
                         {'C': [1, 10, 100, 1000], 'gamma': [0.001, 0.0001],
                          'kernel': ['rbf']}],
             pre_dispatch='2*n_jobs', refit=True, return_train_score=False,
             scoring=None, verbose=0)
time: 1min 38s (started: 2021-03-30 14:44:45 +00:00)
In [ ]:
y_pred = clf.predict(x_test)
y_pred
Out[ ]:
array([1, 0, 1, 2, 2, 1, 0, 1, 1, 0, 1, 0, 1, 2, 2, 1, 2, 1, 0, 1, 2, 2,
       2, 0, 0, 0, 1])
time: 144 ms (started: 2021-03-30 14:54:23 +00:00)
In [ ]:
y_test
Out[ ]:
array([1, 0, 1, 2, 2, 1, 0, 1, 1, 0, 1, 0, 1, 2, 2, 1, 2, 1, 0, 1, 2, 2,
       2, 0, 0, 0, 1])
time: 5.45 ms (started: 2021-03-30 14:54:43 +00:00)
In [ ]:
from sklearn.metrics import accuracy_score,confusion_matrix
time: 1.34 ms (started: 2021-03-30 14:55:00 +00:00)
In [ ]:
accuracy_score(y_pred,y_test)
Out[ ]:
1.0
time: 5.33 ms (started: 2021-03-30 14:55:19 +00:00)
In [ ]:
confusion_matrix(y_pred,y_test)
Out[ ]:
array([[ 8,  0,  0],
       [ 0, 11,  0],
       [ 0,  0,  8]])
time: 6.29 ms (started: 2021-03-30 14:55:36 +00:00)
In [ ]:
# Save the model using Pickle library
import pickle
pickle.dump(clf,open('img_model.p','wb'))
time: 34.2 ms (started: 2021-03-30 14:56:18 +00:00)
In [ ]:
model = pickle.load(open('img_model.p','rb'))
time: 24 ms (started: 2021-03-30 14:56:34 +00:00)
In [ ]:
# Testing a brand new Image
flat_data = []
url = input('Enter your URL')
img = imread(url)
img_resized = resize(img,(150,150,3))
flat_data.append(img_resized.flatten())
flat_data = np.array(flat_data)
print(img.shape)
plt.imshow(img_resized)
y_out = model.predict(flat_data)
y_out = CATEGORIES[y_out[0]]
print(f' PREDICTED OUTPUT: {y_out}')
Enter your URLhttps://www.aljazeera.com/wp-content/uploads/2020/12/2020-12-09T114554Z_1329857512_RC2NJK98FXB2_RTRMADP_3_HEALTH-CORONAVIRUS-SINGAPORE-CRUISESHIP.jpg
(4480, 6720, 3)
 PREDICTED OUTPUT: cruise

time: 3min 30s (started: 2021-03-30 14:57:02 +00:00)
In [ ]:
!pip install streamlit

!pip install pyngrok
from pyngrok import ngrok
Collecting streamlit
  Downloading https://files.pythonhosted.org/packages/76/a6/2507aedaa1c80d39eccd601129d273f4091720f4b1031997bb52630ba504/streamlit-0.79.0-py2.py3-none-any.whl (7.0MB)
     |████████████████████████████████| 7.0MB 6.3MB/s 
Requirement already satisfied: click>=7.0 in /usr/local/lib/python3.7/dist-packages (from streamlit) (7.1.2)
Requirement already satisfied: pillow>=6.2.0 in /usr/local/lib/python3.7/dist-packages (from streamlit) (7.0.0)
Requirement already satisfied: cachetools>=4.0 in /usr/local/lib/python3.7/dist-packages (from streamlit) (4.2.1)
Requirement already satisfied: toml in /usr/local/lib/python3.7/dist-packages (from streamlit) (0.10.2)
Collecting validators
  Downloading https://files.pythonhosted.org/packages/db/2f/7fed3ee94ad665ad2c1de87f858f10a7785251ff75b4fd47987888d07ef1/validators-0.18.2-py3-none-any.whl
Collecting gitpython
  Downloading https://files.pythonhosted.org/packages/a6/99/98019716955ba243657daedd1de8f3a88ca1f5b75057c38e959db22fb87b/GitPython-3.1.14-py3-none-any.whl (159kB)
     |████████████████████████████████| 163kB 42.2MB/s 
Requirement already satisfied: python-dateutil in /usr/local/lib/python3.7/dist-packages (from streamlit) (2.8.1)
Requirement already satisfied: pyarrow; python_version < "3.9" in /usr/local/lib/python3.7/dist-packages (from streamlit) (3.0.0)
Collecting base58
  Downloading https://files.pythonhosted.org/packages/b8/a1/d9f565e9910c09fd325dc638765e8843a19fa696275c16cc08cf3b0a3c25/base58-2.1.0-py3-none-any.whl
Requirement already satisfied: pandas>=0.21.0 in /usr/local/lib/python3.7/dist-packages (from streamlit) (1.1.5)
Requirement already satisfied: astor in /usr/local/lib/python3.7/dist-packages (from streamlit) (0.8.1)
Collecting pydeck>=0.1.dev5
  Downloading https://files.pythonhosted.org/packages/1c/3f/8f04ae0c22d82ec7bec7fcc03270a142f637e362bbd285f7daeeda24fbef/pydeck-0.6.1-py2.py3-none-any.whl (4.6MB)
     |████████████████████████████████| 4.6MB 44.3MB/s 
Collecting blinker
  Downloading https://files.pythonhosted.org/packages/1b/51/e2a9f3b757eb802f61dc1f2b09c8c99f6eb01cf06416c0671253536517b6/blinker-1.4.tar.gz (111kB)
     |████████████████████████████████| 112kB 43.3MB/s 
Requirement already satisfied: requests in /usr/local/lib/python3.7/dist-packages (from streamlit) (2.23.0)
Requirement already satisfied: tornado>=5.0 in /usr/local/lib/python3.7/dist-packages (from streamlit) (5.1.1)
Requirement already satisfied: altair>=3.2.0 in /usr/local/lib/python3.7/dist-packages (from streamlit) (4.1.0)
Collecting watchdog; platform_system != "Darwin"
  Downloading https://files.pythonhosted.org/packages/c6/ba/a36ca5b4e75649a002f06531862467b3eb5c768caa23d6d88b921fe238d8/watchdog-2.0.2-py3-none-manylinux2014_x86_64.whl (74kB)
     |████████████████████████████████| 81kB 4.2MB/s 
Requirement already satisfied: packaging in /usr/local/lib/python3.7/dist-packages (from streamlit) (20.9)
Requirement already satisfied: numpy in /usr/local/lib/python3.7/dist-packages (from streamlit) (1.19.5)
Requirement already satisfied: protobuf!=3.11,>=3.6.0 in /usr/local/lib/python3.7/dist-packages (from streamlit) (3.12.4)
Requirement already satisfied: tzlocal in /usr/local/lib/python3.7/dist-packages (from streamlit) (1.5.1)
Requirement already satisfied: decorator>=3.4.0 in /usr/local/lib/python3.7/dist-packages (from validators->streamlit) (4.4.2)
Requirement already satisfied: six>=1.4.0 in /usr/local/lib/python3.7/dist-packages (from validators->streamlit) (1.15.0)
Collecting gitdb<5,>=4.0.1
  Downloading https://files.pythonhosted.org/packages/ea/e8/f414d1a4f0bbc668ed441f74f44c116d9816833a48bf81d22b697090dba8/gitdb-4.0.7-py3-none-any.whl (63kB)
     |████████████████████████████████| 71kB 5.4MB/s 
Requirement already satisfied: pytz>=2017.2 in /usr/local/lib/python3.7/dist-packages (from pandas>=0.21.0->streamlit) (2018.9)
Requirement already satisfied: ipywidgets>=7.0.0 in /usr/local/lib/python3.7/dist-packages (from pydeck>=0.1.dev5->streamlit) (7.6.3)
Requirement already satisfied: traitlets>=4.3.2 in /usr/local/lib/python3.7/dist-packages (from pydeck>=0.1.dev5->streamlit) (5.0.5)
Requirement already satisfied: jinja2>=2.10.1 in /usr/local/lib/python3.7/dist-packages (from pydeck>=0.1.dev5->streamlit) (2.11.3)
Collecting ipykernel>=5.1.2; python_version >= "3.4"
  Downloading https://files.pythonhosted.org/packages/56/95/3a670c8b2c2370bd8631c313f42e60983b3113ffec4035940592252bd6d5/ipykernel-5.5.0-py3-none-any.whl (120kB)
     |████████████████████████████████| 122kB 39.7MB/s 
Requirement already satisfied: urllib3!=1.25.0,!=1.25.1,<1.26,>=1.21.1 in /usr/local/lib/python3.7/dist-packages (from requests->streamlit) (1.24.3)
Requirement already satisfied: idna<3,>=2.5 in /usr/local/lib/python3.7/dist-packages (from requests->streamlit) (2.10)
Requirement already satisfied: certifi>=2017.4.17 in /usr/local/lib/python3.7/dist-packages (from requests->streamlit) (2020.12.5)
Requirement already satisfied: chardet<4,>=3.0.2 in /usr/local/lib/python3.7/dist-packages (from requests->streamlit) (3.0.4)
Requirement already satisfied: jsonschema in /usr/local/lib/python3.7/dist-packages (from altair>=3.2.0->streamlit) (2.6.0)
Requirement already satisfied: toolz in /usr/local/lib/python3.7/dist-packages (from altair>=3.2.0->streamlit) (0.11.1)
Requirement already satisfied: entrypoints in /usr/local/lib/python3.7/dist-packages (from altair>=3.2.0->streamlit) (0.3)
Requirement already satisfied: pyparsing>=2.0.2 in /usr/local/lib/python3.7/dist-packages (from packaging->streamlit) (2.4.7)
Requirement already satisfied: setuptools in /usr/local/lib/python3.7/dist-packages (from protobuf!=3.11,>=3.6.0->streamlit) (54.1.2)
Collecting smmap<5,>=3.0.1
  Downloading https://files.pythonhosted.org/packages/68/ee/d540eb5e5996eb81c26ceffac6ee49041d473bc5125f2aa995cf51ec1cf1/smmap-4.0.0-py2.py3-none-any.whl
Requirement already satisfied: nbformat>=4.2.0 in /usr/local/lib/python3.7/dist-packages (from ipywidgets>=7.0.0->pydeck>=0.1.dev5->streamlit) (5.1.2)
Requirement already satisfied: ipython>=4.0.0; python_version >= "3.3" in /usr/local/lib/python3.7/dist-packages (from ipywidgets>=7.0.0->pydeck>=0.1.dev5->streamlit) (5.5.0)
Requirement already satisfied: widgetsnbextension~=3.5.0 in /usr/local/lib/python3.7/dist-packages (from ipywidgets>=7.0.0->pydeck>=0.1.dev5->streamlit) (3.5.1)
Requirement already satisfied: jupyterlab-widgets>=1.0.0; python_version >= "3.6" in /usr/local/lib/python3.7/dist-packages (from ipywidgets>=7.0.0->pydeck>=0.1.dev5->streamlit) (1.0.0)
Requirement already satisfied: ipython-genutils in /usr/local/lib/python3.7/dist-packages (from traitlets>=4.3.2->pydeck>=0.1.dev5->streamlit) (0.2.0)
Requirement already satisfied: MarkupSafe>=0.23 in /usr/local/lib/python3.7/dist-packages (from jinja2>=2.10.1->pydeck>=0.1.dev5->streamlit) (1.1.1)
Requirement already satisfied: jupyter-client in /usr/local/lib/python3.7/dist-packages (from ipykernel>=5.1.2; python_version >= "3.4"->pydeck>=0.1.dev5->streamlit) (5.3.5)
Requirement already satisfied: jupyter-core in /usr/local/lib/python3.7/dist-packages (from nbformat>=4.2.0->ipywidgets>=7.0.0->pydeck>=0.1.dev5->streamlit) (4.7.1)
Requirement already satisfied: simplegeneric>0.8 in /usr/local/lib/python3.7/dist-packages (from ipython>=4.0.0; python_version >= "3.3"->ipywidgets>=7.0.0->pydeck>=0.1.dev5->streamlit) (0.8.1)
Requirement already satisfied: pexpect; sys_platform != "win32" in /usr/local/lib/python3.7/dist-packages (from ipython>=4.0.0; python_version >= "3.3"->ipywidgets>=7.0.0->pydeck>=0.1.dev5->streamlit) (4.8.0)
Requirement already satisfied: prompt-toolkit<2.0.0,>=1.0.4 in /usr/local/lib/python3.7/dist-packages (from ipython>=4.0.0; python_version >= "3.3"->ipywidgets>=7.0.0->pydeck>=0.1.dev5->streamlit) (1.0.18)
Requirement already satisfied: pygments in /usr/local/lib/python3.7/dist-packages (from ipython>=4.0.0; python_version >= "3.3"->ipywidgets>=7.0.0->pydeck>=0.1.dev5->streamlit) (2.6.1)
Requirement already satisfied: pickleshare in /usr/local/lib/python3.7/dist-packages (from ipython>=4.0.0; python_version >= "3.3"->ipywidgets>=7.0.0->pydeck>=0.1.dev5->streamlit) (0.7.5)
Requirement already satisfied: notebook>=4.4.1 in /usr/local/lib/python3.7/dist-packages (from widgetsnbextension~=3.5.0->ipywidgets>=7.0.0->pydeck>=0.1.dev5->streamlit) (5.3.1)
Requirement already satisfied: pyzmq>=13 in /usr/local/lib/python3.7/dist-packages (from jupyter-client->ipykernel>=5.1.2; python_version >= "3.4"->pydeck>=0.1.dev5->streamlit) (22.0.3)
Requirement already satisfied: ptyprocess>=0.5 in /usr/local/lib/python3.7/dist-packages (from pexpect; sys_platform != "win32"->ipython>=4.0.0; python_version >= "3.3"->ipywidgets>=7.0.0->pydeck>=0.1.dev5->streamlit) (0.7.0)
Requirement already satisfied: wcwidth in /usr/local/lib/python3.7/dist-packages (from prompt-toolkit<2.0.0,>=1.0.4->ipython>=4.0.0; python_version >= "3.3"->ipywidgets>=7.0.0->pydeck>=0.1.dev5->streamlit) (0.2.5)
Requirement already satisfied: terminado>=0.8.1 in /usr/local/lib/python3.7/dist-packages (from notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.0.0->pydeck>=0.1.dev5->streamlit) (0.9.2)
Requirement already satisfied: nbconvert in /usr/local/lib/python3.7/dist-packages (from notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.0.0->pydeck>=0.1.dev5->streamlit) (5.6.1)
Requirement already satisfied: Send2Trash in /usr/local/lib/python3.7/dist-packages (from notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.0.0->pydeck>=0.1.dev5->streamlit) (1.5.0)
Requirement already satisfied: testpath in /usr/local/lib/python3.7/dist-packages (from nbconvert->notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.0.0->pydeck>=0.1.dev5->streamlit) (0.4.4)
Requirement already satisfied: mistune<2,>=0.8.1 in /usr/local/lib/python3.7/dist-packages (from nbconvert->notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.0.0->pydeck>=0.1.dev5->streamlit) (0.8.4)
Requirement already satisfied: bleach in /usr/local/lib/python3.7/dist-packages (from nbconvert->notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.0.0->pydeck>=0.1.dev5->streamlit) (3.3.0)
Requirement already satisfied: pandocfilters>=1.4.1 in /usr/local/lib/python3.7/dist-packages (from nbconvert->notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.0.0->pydeck>=0.1.dev5->streamlit) (1.4.3)
Requirement already satisfied: defusedxml in /usr/local/lib/python3.7/dist-packages (from nbconvert->notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.0.0->pydeck>=0.1.dev5->streamlit) (0.7.1)
Requirement already satisfied: webencodings in /usr/local/lib/python3.7/dist-packages (from bleach->nbconvert->notebook>=4.4.1->widgetsnbextension~=3.5.0->ipywidgets>=7.0.0->pydeck>=0.1.dev5->streamlit) (0.5.1)
Building wheels for collected packages: blinker
  Building wheel for blinker (setup.py) ... done
  Created wheel for blinker: filename=blinker-1.4-cp37-none-any.whl size=13448 sha256=789dd22f08ad1e5916ea0829c10e931934201ba1a798f4984bbc9a8e273ce218
  Stored in directory: /root/.cache/pip/wheels/92/a0/00/8690a57883956a301d91cf4ec999cc0b258b01e3f548f86e89
Successfully built blinker
ERROR: google-colab 1.0.0 has requirement ipykernel~=4.10, but you'll have ipykernel 5.5.0 which is incompatible.
Installing collected packages: validators, smmap, gitdb, gitpython, base58, ipykernel, pydeck, blinker, watchdog, streamlit
  Found existing installation: ipykernel 4.10.1
    Uninstalling ipykernel-4.10.1:
      Successfully uninstalled ipykernel-4.10.1
Successfully installed base58-2.1.0 blinker-1.4 gitdb-4.0.7 gitpython-3.1.14 ipykernel-5.5.0 pydeck-0.6.1 smmap-4.0.0 streamlit-0.79.0 validators-0.18.2 watchdog-2.0.2
Collecting pyngrok
  Downloading https://files.pythonhosted.org/packages/6b/4e/a2fe095bbe17cf26424c4abcd22a0490e22d01cc628f25af5e220ddbf6f0/pyngrok-5.0.5.tar.gz (745kB)
     |████████████████████████████████| 747kB 6.2MB/s 
Requirement already satisfied: PyYAML in /usr/local/lib/python3.7/dist-packages (from pyngrok) (3.13)
Building wheels for collected packages: pyngrok
  Building wheel for pyngrok (setup.py) ... done
  Created wheel for pyngrok: filename=pyngrok-5.0.5-cp37-none-any.whl size=19246 sha256=cea4f51aae3bbf21974fe1e3ac50d9da615e235bc3d413ab1020d69f9eeebf92
  Stored in directory: /root/.cache/pip/wheels/0c/13/64/5ebbcc22eaf53fdf5766b397c1fb17c83f5775fdccf0ea1b88
Successfully built pyngrok
Installing collected packages: pyngrok
Successfully installed pyngrok-5.0.5
time: 20 s (started: 2021-03-30 15:01:00 +00:00)
In [ ]:
#Deployement
In [ ]:
%%writefile app.py
import streamlit as st
import numpy as np
from skimage.io import imread
from skimage.transform import resize
import pickle 
from PIL import Image
st.set_option('deprecation.showfileUploaderEncoding', False)
st.title('Image Classifier using Machine Learning')
st.text('Upload the Image')

model = pickle.load(open('img_model.p','rb'))

uploaded_file = st.file_uploader("Choose an image...", type="jpg")
if uploaded_file is not None:
  img = Image.open(uploaded_file)
  st.image(img,caption='Uploaded Image')

  if st.button('PREDICT'):
    CATEGORIES = ['rugby leather ball','aeroplane','cruise']
    st.write('Result...')
    flat_data=[]
    img = np.array(img)
    img_resized = resize(img,(150,150,3))
    flat_data.append(img_resized.flatten())
    flat_data = np.array(flat_data)
    y_out = model.predict(flat_data)
    y_out = CATEGORIES[y_out[0]]
    st.title(f' PREDICTED OUTPUT: {y_out}')
    q = model.predict_proba(flat_data)
    for index, item in enumerate(CATEGORIES):
      st.write(f'{item} : {q[0][index]*100}%')
Writing app.py
time: 4.38 ms (started: 2021-03-30 15:02:38 +00:00)
In [ ]:
!nohup streamlit run app.py &

url = ngrok.connect(port='8501')
url
nohup: appending output to 'nohup.out'
Out[ ]:
<NgrokTunnel: "http://b181e55e3314.ngrok.io" -> "http://localhost:80">
time: 1.93 s (started: 2021-03-30 15:02:55 +00:00)
