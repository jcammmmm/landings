
# How to run
~~~
python3.11 -m http.server
curl http://localhost:8000
~~~


# Deployment
If you have a linux machine in the cloud:

1. `apt install apache2 git`
2. `cd /var/www`
3. `git clone https://github.com/jcammmmm/landings`

## Media Assets
Please place your media files in `_pics` folder (photos, audio, videos).
We do this way to avoid versioning them in git and having a big .git folder 
and also to be able to deploy easily this kind of assets.


# Create Gif from video
1. extract the part from your video if you need.
2. 

demo
ffmpeg -i vid1.mp4 -ss 00:02:00 -t 00:02:03 out.mp4

martilleo (seria bueno ponerlo para delante y para atras)
ffmpeg -i vid2.mp4 -ss 00:08:09 -t 00:08:19 out.mp4

pegando nuestra especialidad (ponerlo palante y pa tras)
ffmpeg -i vid3.mp4 -ss 00:08:09 -t 00:08:19 out.mp4



  ffmpeg -i vid1.mp4 \
    -vf "fps=10,split[s0][s1];[s0]palettegen[p];[s1][p]paletteuse" \
    -loop 0 output.gif

Command with only ffmpeg I find the other version better, because I can create timelapse also.

  ffmpeg -ss 00:02:00 -t 00:02:03 -i ismaelflorez-fabrica1.mp4 \
    -vf "fps=10,split[s0][s1];[s0]palettegen[p];[s1][p]paletteuse" \
    -loop 0 output.gif
        
mp4 to gif. we recomend first to cut the video the feed that file to this command.
 
 ffmpeg -i vid1.mp4 -vf "fps=10,scale=160:-1:flags=lanczos" -c:v pam \
    -f image2pipe - | \
    convert -delay 2 - -loop 0 -layers optimize output.gif
 
 
 
    
To grap images from instagram you need to replace `&amp;` for just `&`. The following image has that ampersand replaced.
    
<img crossorigin="anonymous" class="x5yr21d xu96u03 x10l6tqk x13vifvy x87ps6o xh8yej3" style="object-fit: cover;" src="https://scontent-muc2-1.cdninstagram.com/v/t51.29350-15/449326922_1590130121719789_1084395645137854628_n.heic?stp=dst-jpg_e35_tt6&_nc_cb=dae8a7dc-ddb356e0&efg=eyJ2ZW5jb2RlX3RhZyI6ImltYWdlX3VybGdlbi45NzJ4OTcyLnNkci5mMjkzNTAuZGVmYXVsdF9pbWFnZS5qcGVnbGlfODAwOTIzIn0&_nc_ht=scontent-muc2-1.cdninstagram.com&_nc_cat=101&_nc_ohc=EQ61DYsYbKQQ7kNvgHpu5HQ&_nc_gid=777e502fca4e446bbd85c4732a2a5d5c&edm=APoiHPcBAAAA&ccb=7-5&ig_cache_key=MzQwMzM5NjY3ODAwNTY4NjM5MQ%3D%3D.3-ccb7-5&oh=00_AYCPFjcuCptInHK1BtGUx1qhmAAlPrMW6GEM08tIoJ2Gzg&oe=6708BB34&_nc_sid=22de04">



<img crossorigin="anonymous" class="x5yr21d xu96u03 x10l6tqk x13vifvy x87ps6o xh8yej3" style="object-fit: cover;" src="https://scontent-muc2-1.cdninstagram.com/v/t51.29350-15/449599369_468926685749418_3670115926093596894_n.heic?stp=dst-jpg_e35_tt6&_nc_cb=dae8a7dc-ddb356e0&efg=eyJ2ZW5jb2RlX3RhZyI6ImltYWdlX3VybGdlbi4xMTMweDExMzAuc2RyLmYyOTM1MC5kZWZhdWx0X2ltYWdlLmpwZWdsaV84MDA5MjMifQ&_nc_ht=scontent-muc2-1.cdninstagram.com&_nc_cat=106&_nc_ohc=DTvmbItZ3vsQ7kNvgGHX-Rt&_nc_gid=777e502fca4e446bbd85c4732a2a5d5c&edm=APoiHPcBAAAA&ccb=7-5&ig_cache_key=MzQwMzM5NDMyNjMyNjU5ODc2MA%3D%3D.3-ccb7-5&oh=00_AYAqThWcDZFM7K6rcUeHUx6POT8FWmR5ooDV-IDriFXizQ&oe=6708D399&_nc_sid=22de04">
