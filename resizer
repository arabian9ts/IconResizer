#!/usr/bin/env python

import os
import sys
from PIL import Image

if(len(sys.argv) < 2):
    print('Usage: $ python main.py <your favo size list)>')
    quit()

img_path = sys.argv[1]
size_list = sys.argv[2:]
origin = Image.open(img_path)
img_name,ext = os.path.splitext(os.path.basename(sys.argv[1]))

for size in size_list:
    resized = origin.resize((int(size), int(size)), Image.LANCZOS)
    export_name = img_name + '_' + size + ext
    resized.save(export_name)
    print('exported as ' + export_name)
