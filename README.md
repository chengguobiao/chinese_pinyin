ChinesePinyin
=============

Translate chinese hanzi to pinyin.

The dict is borrowed from <http://github.com/fayland/perl-lingua-han/tree/master/Lingua-Han-PinYin/>

Install
-------

    sudo gem install chinese_pinyin

Usage
-----

    require 'rubygems'
    require 'chinese_pinyin'

    Pinyin.t('中国')  => "zhong guo"
    Pinyin.t('中国', '-') => "zhong-guo"
    Pinyin.t('中国', '') => "zhongguo"
    Pinyin.t('你好world') => "ni hao world"

Polyphone Issue
---------------

use Words.dat to override default behavior.

by default

    Pinyin.t('广州') => "yan zhou"

add file Words.dat

    广州|guang zhou

set ENV['WORDS_FILE'] for Words.dat

    ENV['WORDS_FILE'] = "Words.dat path"
    Pinyin.t('广州') => "guang zhou"
