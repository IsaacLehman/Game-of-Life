# Game-of-Life
The Conway Game of Life in c, parallelized with openMP and creates .pbm images for visualization.  

```sh
# COMPILE
gcc -o GameOfLife.exe -fopenmp GameOfLife.c && chmod +x GameOfLife.exe
# RUN
./GameOfLife.exe 500 500 20 2
# GENERATE .mp4 VIDEO
ffmpeg -r 60 -f image2 -s 1920x1080 -i GameOfLife_gen_%d.pbm -vcodec libx264 -crf 25  -pix_fmt yuv420p GOL.mp4
```

> NOTE: you may need to install ffmpeg - `sudo apt install ffmpeg`
