# kcquant

This package enables you to perform exploratory data analysis on images, as well as
easily quantize the colors of an image to be used for machine learning applications.

To install this package, use

```bash
pip install kcquant
```

Currently only one function (get_colors) exists, which displays the top *n* pixel values (RGB format) in an image.

```bash
from kcquant import get_colors
from PIL import Image
import numpy as np

# open image
img = Image.open(<file path>).convert('RGB')
# call get_colors()
# if image is in RGB set color='RGB'
# if image is in BGR set color='BGR'
# n=5 will display top 5 pixel colors in image
# n=10 will display top 10 pixel colors in image
n=10
get_colors(np.array(img), color = 'RGB', top=n)

```

![image](https://github.com/kbkus/kcquant/blob/main/kcquant/Images/get_colors.png?raw=true)

