.. _sphinx_installation:

======================
Sphinx安装
======================

Linux
======================

.. note::

    以下操作基于Ubuntu 18.04, 不同的Linux发行版安装方式可能略有差别

安装python
----------------

执行如下命令::

    sudo apt install python3.5

.. tip::
    
    Ubuntu18.04自带python3.6，可以跳过这步，如你的操作系统未安装python，
    最好安装python3.5及以上版本，旧版本python可能不支持最新版本sphinx。
    官网给的说明是：Sphinx is written in Python and supports Python 3.5+.

安装sphinx
---------------

如系统未安装python，可执行如下命令::

    sudo apt install python3-sphinx

该命令或同时安装python和sphinx，如仅需安装sphinx，请使用如下命令::

    pip3 install -U sphinx

安装主题
-------------------------------

Sphinx默认主题比较丑，如有需要可以安装其他主题，这里以常用的ReadTheDocs的主题为例::

    pip3 install sphinx_rtd_theme

安装扩展
-----------

Sphinx有很多实用的扩展(Extension)，使用各种扩展可以极大的丰富sphinx的功能。
根据自己的实际情况选择安装何种扩展，这里以我项目中使用到的一些扩展为例

* `水印工具sphinxmark <https://github.com/kallimachos/sphinxmark>`_ ::

    pip3 install sphinxmark

* `生成各种图片工具blockdiag <http://blockdiag.com/en/>`_ ::

    pip3 install sphinxcontrib.blockdiag
    pip3 install sphinxcontrib.nwdiag
    pip3 install sphinxcontrib.seqdiag
    pip3 install sphinxcontrib.actdiag

* `插入plantuml <https://pypi.org/project/sphinxcontrib-plantuml/>`_ ::

    pip3 install sphinxcontrib-plantuml
    sudo apt install default-jre（安装java运行环境）
    sudo apt install plantuml
    sudo apt install graphviz

* `导出pdf <http://www.sphinx-doc.org/en/master/usage/builders/index.html#sphinx.builders.latex.LaTeXBuilder>`_ ::

    sudo apt texlive-latex-recommended
    sudo apt install texlive-latex-recommended
    sudo apt install texlive-fonts-recommended
    sudo apt install texlive-latex-extra（如安装失败尝试sudo apt-get update,后再进行安装）
    sudo apt install latexmk
    可能出现epstopdf cannot run，执行以下安装：
    sudo apt install texlive-extra-utils（可能非必须）
    sudo apt install texlive-font-utils
    可能出现platex not found错误提示，执行以下安装：
    sudo apt search platex（通过这个可以搜索platex所需安装包）
    sudo apt install texlive-lang-japanese

* `matplotlib <https://matplotlib.org/sampledoc/extensions.html>`_ ::

    pip3 install matplotlib
    pip3 install numpydoc
    pip3 install scipy







