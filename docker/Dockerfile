FROM docker.io/fedora:27

RUN dnf -y install \
        cmake \
        gcc \
        gettext \
        git \
        gnome-online-accounts-devel \
        gstreamer1-devel \
        gstreamer1-plugins-base-devel \
        gtk3-devel \
        json-glib-devel \
        libcurl-devel \
        libgee-devel \
        libnotify-devel \
        libpeas-devel \
        libsecret-devel \
        libsoup-devel \
        libxml2-devel \
        rest-devel \
        sqlite-devel \
        vala \
        webkitgtk4-devel

# Install Feedbin
# Note: Some dependencies are duplicates of above, but it's easier to maintain if
# we use the exact list here: https://github.com/feedbin/feedbin/blob/master/doc/INSTALL-fedora.md
# TODO: Run Feedbin in its own container
RUN dnf -y install \
		gcc \
		gcc-c++ \
		git \
		libcurl-devel \
		libidn-devel \
		libxml2-devel \
		libxslt-devel \
		nodejs \
		postgresql \
		postgresql-devel \
		redhat-rpm-config \
		rubygems \
		ruby-devel \
		rubygem-bundler \
		ImageMagick-devel \
		opencv-devel \
		which
RUN git clone https://github.com/feedbin/feedbin.git
RUN gem install bundler
RUN cd feedbin && bundle
