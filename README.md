# bopomo

This is a package to translate a chinese article into bopomofo letters baesed on revised dictionary of Ministry of Education, segment corpus, artificial label data, and python package jieba and python-crfsuite.

```python
>>> import bopomo
>>> sent = '妹妹背著洋娃娃，走到花園來看花。'
>>> bopomo_sent = bopomo.bopomo_sent(sent)
>>> bopomo_sent.bopomo_tag()
[['妹妹背著洋娃娃', 'ㄇㄟˋ ˙ㄇㄟ ㄅㄟ ˙ㄓㄜ ㄧㄤˊ ㄨㄚˊ ˙ㄨㄚ'], ['走到花園來看花', 'ㄗㄡˇ ㄉㄠˋ ㄏㄨㄚ ㄩㄢˊ ㄌㄞˊ ㄎㄢˋ ㄏㄨㄚ']]

```






