#项目
##代码核心功能说明
###1. 获取邮件内容并切词处理 (get_words 函数)
$def get_top_words(top_num):
    filename_list = ['邮件_files/{}.txt'.format(i) for i in range(151)]
    for filename in filename_list:
        all_words.append(get_words(filename))  # 遍历所有邮件生成词库
    freq = Counter(chain(*all_words))  # 统计词频
    return [i[0] for i in freq.most_common(top_num)]  # 返回前 top_num 个高频词
![屏幕截图 2025-04-06 150749](https://github.com/user-attachments/assets/9c8836e5-67b3-493c-ac5d-e8b2671e9df2)
![屏幕截图 2025-04-06 151113](https://github.com/user-attachments/assets/6d8b65bd-6966-4a99-9284-84da0c38af09)
![屏幕截图 2025-04-06 154520](https://github.com/user-attachments/assets/7540bce9-026b-495e-b6f0-b10bb7277951)
