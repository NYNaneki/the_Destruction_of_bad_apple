<!--
 * @Author: CanNev
 * @Date: 2019-11-03 22:52:13
 * @LastEditTime: 2019-11-03 23:24:28
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: /the_Destruction_of_bad_apple/data/README.md
 -->

# 说明

## 目录

- date //所有数据

  - orign //爬虫获取的原始的数据,文件为\*.nmsl
    - 为了防止被反制,暂时不放出
  - comList//评论区列表,文件为\*.json

    - 结构体结构为

      ```golang
      type user struct {
          Nick    string
          Comment string
      }

      func newUser(nick string, comment string) user {
          return user{
              Nick:    nick,
              Comment: comment,
          }
      }

      type pullData struct {
          Date  string
          Users []user
      }

      ```

    - 重复的部分有点多,但是不影响 JavaScript 和 golang 的解析,其他语言不明确
    - 不会分析的可以通过这种方式检索

      - 建议每个人自己去认领,看看某咩可笑的"数据分析"

        ```json
        { "Nick": "你的名字", "Comment": "你的评论" }
        ```

- misc //烈士榜,正在同步统计中,文件格式\*.csv

  - 或许能搞个排位?
  - 构建中,受限于我当前的技术力,目前各种终端输出群魔乱舞,可读性差,格式化后上传

- fans //核心粉丝,文件格式\*.json
  - 在事情更加恶化前我不会主动发布
