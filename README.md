# WHATSAPP CHATGPT
This is a source code to build a WhatsApp bot using OpenAI bot and Node.js. The bot is capable of understanding natural language and providing information on various topics. It can be used to answer questions, provide advice, and even have conversations with users. With this source code, you can create a powerful bot that can be used for a variety of purposes. <br>

NOTE: DON'T MESS UP WITH INDEX.JS FILE. <br>

# How to Install? 
$ git clone https://github.com/lilOussvmv/Whatsapp_GPT <br>
$ cd whatsapp-chatgpt <br>
$ npm install <br>
$ node index.js <br>


# How to get OpenAI API?
Visit: https://beta.openai.com/account/api-keys
"# Whatsapp_GPT Bot" 


```
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin

ENV LANG=C.UTF-8

apt-get update && apt-get install -y --no-install-recommends ca-certificates netbase && rm -rf /var/lib/apt/lists/*

ENV GPG_KEY=0D96DF4D4110E5C43FBFB17F2D347EA6AA65421D

ENV PYTHON_VERSION=3.7.5

set -ex && savedAptMark="$(apt-mark showmanual)" && apt-get update && apt-get install -y --no-install-recommends dpkg-dev gcc libbz2-dev libc6-dev libexpat1-dev libffi-dev libgdbm-dev liblzma-dev libncursesw5-dev libreadline-dev libsqlite3-dev libssl-dev make tk-dev uuid-dev wget xz-utils zlib1g-dev $(command -v gpg > /dev/null || echo 'gnupg dirmngr') && wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" && wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" && export GNUPGHOME="$(mktemp -d)" && gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" && gpg --batch --verify python.tar.xz.asc python.tar.xz && { command -v gpgconf > /dev/null && gpgconf --kill all || :; } && rm -rf "$GNUPGHOME" python.tar.xz.asc && mkdir -p /usr/src/python && tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz && rm python.tar.xz && cd /usr/src/python && gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" && ./configure --build="$gnuArch" --enable-loadable-sqlite-extensions --enable-optimizations --enable-shared --with-system-expat --with-system-ffi --without-ensurepip && make -j "$(nproc)" PROFILE_TASK='-m test.regrtest --pgo test_array test_base64 test_binascii test_binhex test_binop test_bytes test_c_locale_coercion test_class test_cmath test_codecs test_compile test_complex test_csv test_decimal test_dict test_float test_fstring test_hashlib test_io test_iter test_json test_long test_math test_memoryview test_pickle test_re test_set test_slice test_struct test_threading test_time test_traceback test_unicode ' && make install && ldconfig && apt-mark auto '.*' > /dev/null && apt-mark manual $savedAptMark && find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' | awk '/=>/ { print $(NF-1) }' | sort -u | xargs -r dpkg-query --search | cut -d: -f1 | sort -u | xargs -r apt-mark manual && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false && rm -rf /var/lib/apt/lists/* && find /usr/local -depth \( \( -type d -a \( -name test -o -name tests -o -name idle_test \) \) -o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) \) -exec rm -rf '{}' + && rm -rf /usr/src/python && python3 --version

cd /usr/local/bin && ln -s idle3 idle && ln -s pydoc3 pydoc && ln -s python3 python && ln -s python3-config python-config

ENV PYTHON_PIP_VERSION=19.3.1

ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py

ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee

set -ex; savedAptMark="$(apt-mark showmanual)"; apt-get update; apt-get install -y --no-install-recommends wget; wget -O get-pip.py "$PYTHON_GET_PIP_URL"; echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; apt-mark auto '.*' > /dev/null; [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; rm -rf /var/lib/apt/lists/*; python get-pip.py --disable-pip-version-check --no-cache-dir "pip==$PYTHON_PIP_VERSION" ; pip --version; find /usr/local -depth \( \( -type d -a \( -name test -o -name tests -o -name idle_test \) \) -o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) \) -exec rm -rf '{}' +; rm -f get-pip.py

CMD ["python3"]

ENV COMMIT_HASH=48930240573d87d1b06d7504cff41916ce40d28d

ENV PYTHONUNBUFFERED=1

ENV LIBRARY_PATH=/usr/local/lib

ENV LD_LIBRARY_PATH=/usr/local/lib

ENV LIBRARY_INCLUDE_PATH=/usr/local/include

set -ex && cd /usr/local/lib && ln -s libpbc.so.1.0.0 libpbc.so && ln -s libpbc.so.1.0.0 libpbc.so.1

ENV PYTHON_LIBRARY_PATH=/opt/venv

ENV PATH=/opt/venv/bin:/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin

set -ex && savedAptMark="$(apt-mark showmanual)" && apt-get update && apt-get install -y --no-install-recommends bison flex gcc git make libc6-dev libgmp-dev libssl-dev wget && mkdir -p /usr/src/charm && git clone https://github.com/JHUISI/charm.git /usr/src/charm && cd /usr/src/charm && git reset --hard $COMMIT_HASH && python -m venv ${PYTHON_LIBRARY_PATH} && ./configure.sh && make install && apt-mark auto '.*' > /dev/null && apt-mark manual $savedAptMark && find /usr/local -type f -executable -execdir ldd '{}' ';' | awk '/=>/ { print $(NF-1) }' | sort -u | xargs -r dpkg-query --search | cut -d: -f1 | sort -u | xargs -r apt-mark manual && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false && rm -rf /var/lib/apt/lists/* && rm -rf /usr/src/charm
```
