# chatbot
一个可以进行训练的聊天机器人

#关于语料的说明

本次训练的语料是从互联网上找到的shooter的训练语料，语料质量很差劲，仅作为演示代码来用，大家可以使用自己的语料
语料下载地址：https://pan.baidu.com/s/1kWYIOVt,将文件下载后放到data目录下

#代码执行顺序

1、在下载好代码和语料之后，将语料文件放入data目录下
2、按照 数据预处理器（data_utls.py)-->execute.py(执行器)-->web/app.py（预测可视化模块）的顺序执行就可以了。
3、超参配置在seq2seq.ini和seq2seq_sever.ini文件中配置
4、详细的代码讲解可以参与我的chat文章(http://gitbook.cn/books/5a4a16da1f2e8d585e464f44/index.html)


#参考代码和文献

http://blog.topspeedsnail.com/archives/10735/comment-page-1#comment-1161

http://www.easyapple.net/?p=1384&from=singlemessage&isappinstalled=0

#建议环境

ubuntu14.04
python3.5
tensorflow==1.0.1
flask==0.11.1

#关于版权

本代码完全开源，只是用作一个小玩具供大家学习和研究交流，不过还是希望大家fork和给个star，后续也会根据大家的反馈持续更新代码，希望可以做成一个不傻的中文聊天机器人。

#演示地址

自己用语料训练了一个模型，preplexity降到10，虽然还不是理想的结果，但是完全在不进行分词、不做词库的情况，在有些方面聊天还是有关联的。

http://115.231.97.140:8999/

#关于增加分词

今天有小伙伴提出分词的问题，如果要增加分词的话直接在数据处理器里添加分词就可以了，可以使用结巴分词或者一些主流的分词，也可以对原始语料进行分词。其实分词这里，主要影响的是
字典的生成以及依据字典进行的向量化，理论上进行分词后会更加的贴合实际语境一些，大家可以尝试。我也会抽空试一下，加上分词后的效果，如果效果好的话会更新到代码上。







