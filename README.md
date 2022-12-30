# sequence_labelling


### Dataset
[Second International Chinese Word Segmentation Bakeoff Data](http://sighan.cs.uchicago.edu/bakeoff2005/)

#### data add tagging
```
raw_text = "  严格要求  自己  ，  从  一个  科举  出身  的  进士  成为  一个  伟大  的  民主主义  者  ，  进而  成为  一  位  杰出  的  党外  共产主义  战士  ，  献身  于  崇高  的  共产主义  事业  。"

tag = []
for wd in raw_text.split():
    if len(wd) == 1:
        tag.append('S')
    if len(wd) == 2:
        tag.append('BE')
    if len(wd) > 2:
        t = 'B' + 'M'* (len(wd)-2) + 'E'
        tag.append(t)

tag_list = list(''.join(tag))
text_list = list(''.join(raw_text.split()))

print(tag)
print(text_list)
print(tag_list)
print(len(text_list),len(tag_list))
```

```
['BMME', 'BE', 'S', 'S', 'BE', 'BE', 'BE', 'S', 'BE', 'BE', 'BE', 'BE', 'S', 'BMME', 'S', 'S', 'BE', 'BE', 'S', 'S', 'BE', 'S', 'BE', 'BMME', 'BE', 'S', 'BE', 'S', 'BE', 'S', 'BMME', 'BE', 'S']
['严', '格', '要', '求', '自', '己', '，', '从', '一', '个', '科', '举', '出', '身', '的', '进', '士', '成', '为', '一', '个', '伟', '大', '的', '民', '主', '主', '义', '者', '，', '进', '而', '成', '为', '一', '位', '杰', '出', '的', '党', '外', '共', '产', '主', '义', '战', '士', '，', '献', '身', '于', '崇', '高', '的', '共', '产', '主', '义', '事', '业', '。']
['B', 'M', 'M', 'E', 'B', 'E', 'S', 'S', 'B', 'E', 'B', 'E', 'B', 'E', 'S', 'B', 'E', 'B', 'E', 'B', 'E', 'B', 'E', 'S', 'B', 'M', 'M', 'E', 'S', 'S', 'B', 'E', 'B', 'E', 'S', 'S', 'B', 'E', 'S', 'B', 'E', 'B', 'M', 'M', 'E', 'B', 'E', 'S', 'B', 'E', 'S', 'B', 'E', 'S', 'B', 'M', 'M', 'E', 'B', 'E', 'S']
61 61
```




ref
(https://blog.csdn.net/taoyanqi8932/article/details/75312822)
(https://blog.csdn.net/katrina1rani/article/details/107197971) [code](https://github.com/luopeixiang/named_entity_recognition/blob/master/main.py)
