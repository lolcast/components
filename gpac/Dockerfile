FROM ubuntu:15.04
RUN apt-get update && apt-get install -y \
	dvb-apps \
	ffmpeg \
	firefox-dev \
	g++ \
	git-core \
	liba52-0.7.4-dev \
	libasound2-dev \
	libavcodec-ffmpeg-dev \
	libavdevice-ffmpeg56 \
	libavdevice-ffmpeg-dev \
	libavfilter-ffmpeg-dev \
	libavformat-ffmpeg-dev \
	libavresample-ffmpeg-dev \
	libavutil-ffmpeg-dev \
	libfaad-dev \
	libfreetype6-dev \
	libgl1-mesa-dev \
	libjack-dev \
	libjpeg62-dev \
	libmad0-dev \
	libmozjs185-dev \
	libogg-dev \
	libopenjpeg-dev \
	libpng12-dev \
	libpostproc-ffmpeg-dev \
	libpulse-dev \
	libsdl1.2-dev \
	libssl-dev \
	libswresample-ffmpeg-dev \
	libswscale-ffmpeg-dev \
	libtheora-dev \
	libvorbis-dev \
	libx264-dev \
	libxv-dev \
	libxvidcore-dev \
	linux-sound-base \
	make \
	pkg-config \
	rtmpdump \
	subversion \
	x11proto-gl-dev \
	x11proto-video-dev \
	yasm \
	zlib1g-dev \
	;
RUN grep -q -R av_make_error_string /usr /opt
ADD . /
RUN cd /gpac && ./configure
RUN cd /gpac && make && make install || true
