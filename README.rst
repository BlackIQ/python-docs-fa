ترجمه مستندات پایتون — fa
============================================

.. image:: https://travis-ci.org/python/python-docs-fa.svg?branch=3.7
  :target: https://travis-ci.org/python/python-docs-fa


Documentation Contribution Agreement
------------------------------------

NOTE REGARDING THE LICENSE FOR TRANSLATIONS: Python's documentation is
maintained using a global network of volunteers. By posting this
project on Transifex, Github, and other public places, and inviting
you to participate, we are proposing an agreement that you will
provide your improvements to Python's documentation or the translation
of Python's documentation for the PSF's use under the CC0 license
(available at
https://creativecommons.org/publicdomain/zero/1.0/legalcode). In
return, you may publicly claim credit for the portion of the
translation you contributed and if your translation is accepted by the
PSF, you may (but are not required to) submit a patch including an
appropriate annotation in the Misc/ACKS or TRANSLATORS file. Although
nothing in this Documentation Contribution Agreement obligates the PSF
to incorporate your textual contribution, your participation in the
Python community is welcomed and appreciated.

You signify acceptance of this agreement by submitting your work to
the PSF for inclusion in the documentation.


مشارکت در ترجمه
-------------------------------

چگونه مشارکت کنیم؟
~~~~~~~~~~~~~~~~~

شما برای مشارکت در ترجمه میتوانید از موارد زیر استفاده کنید:

- گیت هاب
- یا فقط `یک ایشو در گیت‌هاب <https://github.com/mmdbalkhi/python-docs-fa/issues>`_ باز کنید.


مشارکت با استفاده از گیت هاب
~~~~~~~~~~~~~~~~~~~~~~~~~

پیش‌نیاز ها:

- یک `حساب کاربری گیت‌هاب <https://github.com/join>`_.
- ``git`` `نصب شده داشته باشید <https://help.github.com/articles/set-up-git/>`_ (برای ویندوز, این را ببینید
  https://gitforwindows.org/).
- یک ادیتور فایل``.po`` (اگر هنوز گزینه ای را انتخاب نکرده اید، میتوانید از
`poedit <https://poedit.net/>`_ استفاده کنید).


بیاین شروع کنیم:

شما به یک فورک از  `python-docs-fa
<https://github.com/python/python-docs-fa>`_ نیاز دارید. بر روی دکمه ``Fork``
کلیک کنید. این یک کپی از کل پروژه را در حساب کاربری گیت‌هاب شما ایجاد میکند. 
اینجا جایی است که شما میتوانید در آن تغییر ایجاد کنید.

گام به گام:

.. code-block:: bash

    # کلون کردن فورک شما با توسط ssh (نام کاربری خودتان را با Username جایگزین کنید):
    git clone git@github.com:Username/python-docs-fa.git

    # به دایرکتوری کلون شده بروید:
    cd python-docs-fa/

    # مخزن اصلی را توسط HTTPS اضافه کنید(رمز عبوری از شما نخواهد پرسید):
    git remote add upstream https://github.com/python/python-docs-fa.git

تمام ترجمه ها باید در آخرین نسخه انجام شوند.
ما هرگز بر روی قدیمی ترین نسخه، به عنوان مثال، آخرین نسخه پایتون ترجمه نمی کنیم
پایتون 3.9 است، ما نمی خواهیم مستقیماً در نسخه 3.5 پایتون ترجمه کنیم.
در صورت نیاز، ترجمه‌ها بر روی قدیمی‌ترین نسخه‌ها توسط سازمان پشتیبانی می‌شوند
`تیم مستندسازی <https://www.python.org/dev/peps/pep-8015/#documentation-team>`_.

اکنون برای شروع یک جلسه کاری آماده هستید، هر بار که کار جدیدی را شروع می کنید، از اینجا شروع کنید:

.. code-block:: bash

    # برای کار، به یک شاخه بر اساس شاخه به‌روز (جدیدا fetch شده) نیاز داریم
    # شاخه upstream/3.10، فرض کنید روی "glossary" کار می کنیم تا نام گذاری کنیم
    # شاخه "glossary":
    git fetch upstream
    git checkout -b glossary upstream/3.7

    # اکنون می توانید روی فایل کار کنید.(معمولا از poedit استفاده میشود)
    poedit directory/file.po

    # وقتی همه چیز واضح است (خطاهای نحوی از Sphinx، رندر html،
    # معناشناسی، تایپوگرافی)،
    # می توانید کار خود را با یک پیام صریح زیبا کامیت کنید:
    git commit -a -m "Working on glossary."

    # سپس تغییرات خود را به کلون github خود پوش کنید،
    # چون شاخه های زودگذر هستند، اجازه دهید git را برای ردیابی همه آنها پیکربندی نکنیم،
    # "origin HEAD" یک نحو "ویژه" برای گفتن "Push on origin" است،
    # در شاخه ای با همان نام محلی،"
    # خوب است زیرا دقیقاً همان چیزی است که ما می خواهیم:
    git push origin HEAD

    # دستور قبلی یک پیوند برای باز کردن روابط عمومی در github برای شما چاپ می کند.
    # اگر آن را از دست دادید، فقط به آن بروید
    # https://github.com/mmdbalkhi/python-docs-fa/ و یک "درخواست مقایسه و کشش" خوب
    دکمه # باید بعد از چند ثانیه ظاهر شود و به شما بگوید می‌توانید درخواست کشش کنید.

    # اکنون شخصی در حال بررسی تغییرات شما است و شما می خواهید آنها را اصلاح کنید
    # یافته ها، به شعبه خود بازگردید
    # (در صورتی که کار دیگری را در شاخه دیگری شروع کرده باشید):
    git checkout glossary
    # مشکلات را برطرف کنید، سپس دوباره متعهد شوید:
    git commit -a -m "glossary: small fixes."
    git push origin HEAD

You may have noted that this looks like a triangle, with a missing segment:

- You're fetching from upstream (public common repo on github)
- You're pushing to origin (your clone on github)

So yes it's the work of someone to add the last segment, from your
origin to the public upstream, to "close the loop", that's the role of
the people who merges pull requests after proofreading them.

You may also have noted you never ever commit on a version branch
(``3.6``, ``3.7``, ...), only pull from them, consider them read-only
you'll avoid problems.


What to translate
~~~~~~~~~~~~~~~~~

You can start with easy tasks like reviewing fuzzy entries to help
keeping the documentation up to date (find them using ``make fuzzy``).

You can also proofread already translated entries, and finally
translate untranslated ones (find them using ``make todo``)..

- Do not translate content of ``:ref:...`` and ``:term:...``
- Put english words, if you have to use them, in *italics* (surrounded
  by stars).
- If you translate a link title, please translate the link too
  (typically if it's Wikipedia and the article has a translation). If
  no translation of the target exists, do not translate the
  title.


Where to get help
~~~~~~~~~~~~~~~~~


Translation Resources
---------------------


Glossary
--------

For consistency in our translations, here are some propositions and
reminders for frequent terms you'll have to translate, don't hesitate
to open an issue if you disagree.

To easily find how a term is already translated in our documentation,
you may use
`find_in_po.py <https://gist.github.com/JulienPalard/c430ac23446da2081060ab17bf006ac1>`_.

========================== ===========================================
Term                       Proposed Translation
========================== ===========================================
-like
abstract data type
argument
backslash
bound
bug
built-in
call stack
debugging
deep copy
double quote
e.g.
garbage collector
identifier
immutable
installer
interpreter
library
list comprehension
little-endian, big-endian
mutable
namespace
parameter
prompt
raise
regular expression
return
simple quote
socket
statement
subprocess
thread
underscore
expression
========================== ===========================================


Simplify git diffs
------------------

Git diffs are often crowded with useless line number changes, like:

.. code-block:: diff

    -#: ../Doc/library/signal.rst:406
    +#: ../Doc/library/signal.rst:408

To tell git they are not usefull information, you can do the following
after ensuring ``~/.local/bin/`` is in your ``PATH``.

.. code-block:: bash

    cat <<EOF > ~/.local/bin/podiff
    #!/bin/sh
    grep -v '^#:' "\$1"
    EOF

    chmod a+x ~/.local/bin/podiff

    git config diff.podiff.textconv podiff


Maintenance
-----------

All those snippets are to run from the root of a ``python-docs-fa``
clone, and some expect to find an up-to-date CPython clone near to it,
like:

.. code-block:: bash

  ~/
  ├── python-docs-fa/
  └── cpython/

To clone CPython you may use:

.. code-block:: bash

  git clone --depth 1 --no-single-branch https://github.com/python/cpython.git

This avoids to download the whole history (not usefull to build
documentation) but still fetches all branches.


Merge pot files from CPython
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

  make merge


Find fuzzy strings
~~~~~~~~~~~~~~~~~~

.. code-block:: bash

  make fuzzy


Run a test build locally
~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: bash

  make


Synchronize translation with Transifex
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

You'll need the ``transifex-client`` and ``powrap``
from Pypi.

You'll need to configure ``tx`` via ``tx init`` if not already done.

.. code-block:: bash

   pomerge --from-files **/*.po
   tx pull -f
   pomerge --to-files **/*.po
   pomerge --from-files **/*.po
   git checkout -- .
   pomerge --to-files **/*.po
   powrap --modified
   git commit -m "tx pull"
   tx push -t -f
