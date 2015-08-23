FROM ubuntu:15.04
RUN apt-get update && apt-get install -y \
        ffmpeg \
        curl \
        ;
RUN curl -o bunny.mov -L http://download.blender.org/peach/bigbuckbunny_movies/big_buck_bunny_480p_h264.mov
CMD ffmpeg -re -i bunny.mov -acodec copy -vcodec copy -f flv ${TARGET:-rtmp://localhost/live/stream}
