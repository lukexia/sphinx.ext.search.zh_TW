# sphinx.ext.search.zh_TW
Sphinx Traditional Chinese search extension
It forks from [bosbyj/sphinx.search.zh_CN](https://github.com/bosbyj/sphinx.search.zh_CN)

## Installation

Install pip
```bash
$ pip install jieba
```

Install sphinx.ext.search.zh_TW
```bash
$ cd PATH_TO_PROJECT_DIR
$ git clone https://github.com/enhao/sphinx.ext.search.zh_TW.git _extension
```

## Configuration

Edit `conf.py`
```python
# If extensions (or modules to document with autodoc) are in another directory,
# add these directories to sys.path here. If the directory is relative to the
# documentation root, use os.path.abspath to make it absolute, like shown here.
sys.path.insert(0, os.path.abspath('_extension'))

...

# Add any Sphinx extension module names here, as strings. They can be
# extensions coming with Sphinx (named 'sphinx.ext.*') or your custom
# ones.
extensions = ['search-zh_TW']

...

# Language to be used for generating the HTML full-text search index.
# Sphinx supports the following languages:
#   'da', 'de', 'en', 'es', 'fi', 'fr', 'hu', 'it', 'ja'
#   'nl', 'no', 'pt', 'ro', 'ru', 'sv', 'tr'
html_search_language = 'zh_TW'
```

You can use the custom dictionary as the following
```python
# A dictionary with options for the search language support, empty by default.
# Now only 'ja' uses this config value
html_search_options = {'dict': '_extension/dict/zh.dict'}
```

