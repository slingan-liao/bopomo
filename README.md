# bopomo

This is a package to translate a chinese article into bopomofo letters baesed on revised dictionary of Ministry of Education, segment corpus, artificial label data, and python package jieba and python-crfsuite.

```python
>>> import bopomo
>>> sent = '妹妹背著洋娃娃，走到花園來看花。'
>>> bopomo_sent = bopomo.bopomo_sent(sent)
>>> print(bopomo_sent.bopomo_tag())
[['妹妹背著洋娃娃', 'ㄇㄟˋ ˙ㄇㄟ ㄅㄟ ˙ㄓㄜ ㄧㄤˊ ㄨㄚˊ ˙ㄨㄚ'], ['走到花園來看花', 'ㄗㄡˇ ㄉㄠˋ ㄏㄨㄚ ㄩㄢˊ ㄌㄞˊ ㄎㄢˋ ㄏㄨㄚ']]

>>> sent = '如果薪水不到4萬8，可向老闆說你給的薪水太低了。'
>>> bopomo_sent = bopomo.bopomo_sent(sent)
>>> print(bopomo_sent.bopomo_tag())
[['如果薪水不到4萬8', 'ㄖㄨˊ ㄍㄨㄛˇ ㄒㄧㄣ ㄕㄨㄟˇ ㄅㄨˋ ㄉㄠˋ 4 ㄨㄢˋ 8'], ['可向老闆說你給的薪水太低了', 'ㄎㄜˇ ㄒㄧㄤˋ ㄌㄠˇ ㄅㄢˇ ㄕㄨㄛ ㄋㄧˇ ㄍㄟˇ ˙ㄉㄜ ㄒㄧㄣ ㄕㄨㄟˇ ㄊㄞˋ ㄉㄧ ˙ㄌㄜ']]

>>> sent = '有人年輕時就培養多元興趣，退休後全心投入自己喜愛的事物；有人一輩子在職場奔忙，不知興趣為何物，一旦退休每天閒得發慌。\n除了金錢的準備，心靈、健康、興趣的準備都很重要，及早作好規畫，無縫接軌，退休應該是人生另一個美好階段的開始。'
>>> bopomo_sent = bopomo.bopomo_sent(sent)
>>> bopomo = bopomo_sent.bopomo_tag()
>>> for i in range(len(bopomo)):
...     print(bopomo[i])
['有人年輕時就培養多元興趣', 'ㄧㄡˇ ㄖㄣˊ ㄋㄧㄢˊ ㄑㄧㄥ ㄕˊ ㄐㄧㄡˋ ㄆㄟˊ ㄧㄤˇ ㄉㄨㄛ ㄩㄢˊ ㄒㄧㄥˋ ㄑㄩˋ']
['退休後全心投入自己喜愛的事物', 'ㄊㄨㄟˋ ㄒㄧㄡ ㄏㄡˋ ㄑㄩㄢˊ ㄒㄧㄣ ㄊㄡˊ ㄖㄨˋ ㄗˋ ㄐㄧˇ ㄒㄧˇ ㄞˋ ˙ㄉㄜ ㄕˋ ㄨˋ']
['有人一輩子在職場奔忙', 'ㄧㄡˇ ㄖㄣˊ ㄧ ㄅㄟˋ ˙ㄗ ㄗㄞˋ ㄓˊ ㄔㄤˇ ㄅㄣ ㄇㄤˊ']
['不知興趣為何物', 'ㄅㄨˋ ㄓ ㄒㄧㄥˋ ㄑㄩˋ ㄨㄟˋ ㄏㄜˊ ㄨˋ']
['一旦退休每天閒得發慌', 'ㄧ ㄉㄢˋ ㄊㄨㄟˋ ㄒㄧㄡ ㄇㄟˇ ㄊㄧㄢ ㄒㄧㄢˊ ㄉㄜˊ ㄈㄚ ㄏㄨㄤ']
['除了金錢的準備', 'ㄔㄨˊ ˙ㄌㄜ ㄐㄧㄣ ㄑㄧㄢˊ ˙ㄉㄜ ㄓㄨㄣˇ ㄅㄟˋ']
['心靈', 'ㄒㄧㄣ ㄌㄧㄥˊ']
['健康', 'ㄐㄧㄢˋ ㄎㄤ']
['興趣的準備都很重要', 'ㄒㄧㄥˋ ㄑㄩˋ ˙ㄉㄜ ㄓㄨㄣˇ ㄅㄟˋ ㄉㄡ ㄏㄣˇ ㄓㄨㄥˋ ㄧㄠˋ']
['及早作好規畫', 'ㄐㄧˊ ㄗㄠˇ ㄗㄨㄛˋ ㄏㄠˇ ㄍㄨㄟ ㄏㄨㄚˋ']
['無縫接軌', 'ㄨˊ ㄈㄥˊ ㄐㄧㄝ ㄍㄨㄟˇ']
['退休應該是人生另一個美好階段的開始', 'ㄊㄨㄟˋ ㄒㄧㄡ ㄧㄥ ㄍㄞ ㄕˋ ㄖㄣˊ ㄕㄥ ㄌㄧㄥˋ ㄧ ˙ㄍㄜ ㄇㄟˇ ㄏㄠˇ ㄐㄧㄝ ㄉㄨㄢˋ ˙ㄉㄜ ㄎㄞ ㄕˇ']



```






 
