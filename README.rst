=====================
scrapy-dotpersistence
=====================

Scrapy extension to sync `.scrapy` folder to an S3 bucket.

Installation
============

You can install scrapy-dotpersistence using pip::

    pip install scrapy-dotpersistence

You can then enable the extension in your `settings.py`::

    EXTENSIONS = {
        ...
        'scrapy_dotpersistence.DotScrapyPersistence': 0
    }

How to use it
=============

Enable extension through `settings.py`::

    DOTSCRAPY_ENABLED = True

Configure the exension through `settings.py`::

    ADDONS_AWS_ACCESS_KEY_ID = "ABC"
    ADDONS_AWS_SECRET_ACCESS_KEY = "DEF"
    ADDONS_AWS_USERNAME = "username"
    ADDONS_S3_BUCKET = "test-bucket-name"

To override extension settings on Scrapy Cloud::

    DOT_SCRAPY_PERSISTENCE_AWS_ACCESS_KEY_ID = "FOO"
    DOT_SCRAPY_PERSISTENCE_AWS_SECRET_ACCESS_KEY = "BAR"
    DOT_SCRAPY_PERSISTENCE_S3_PATH = "s3://test-bucket-name/dot-scrapy/%(name)s/" # To insert spider's name.

You can change a dotpersistence folder path with environ::

    export DOTSCRAPY_DIR='/tmp/.scrapy'
