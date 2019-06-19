# Industrial-Economics

北邮 产业经济学复习资料 markdown练习

本来只是一个很简单的开卷考试，但是突然兴起就用ppt把老师的ppt梳理了一遍，前前后后大约用了3天时间

话说真的会有需要考这个课的同学会在github上找资料的吗

## 相关软件

要正确的显示文档中的图像与公式，需要一个插件 [`Markdown Preview Enhanced`](https://shd101wyy.github.io/markdown-preview-enhanced/#/zh-cn/) 这个插件有 `vs code` 与`Atom`下都有具体使用方法可以看他们官网

## 样式设置

Markdown Preview Enhanced 允许你通过less自定义样式，具体怎么改建议看官网，我修改了一部分文件实现了首行缩进与章节自动编号

```less
.markdown-preview.markdown-preview {

  //首行缩进
  p {
    text-indent: 35px;
  }

  //将一部分不希望首行缩进的块的首行缩进去掉
  blockquote {
    p {
      text-indent: 0;
    }
  }

  h1 {
    counter-reset: one;
    /* 创建一个计数器 */
  }

  h2 {
    counter-reset: two;
  }

  h2:before {
    counter-increment: one;
    /* 自动将计数器加 1 */
    content: counter(one) "- ";
    /* 获取计数器值，把它填写在 content 中 */
  }

  h3 {
    counter-reset: three;
  }

  h3:before {
    counter-increment: two;
    content: counter(one) "."counter(two) "- ";
  }

  h4 {
    counter-reset: four;
  }

  h4:before {
    counter-increment: three;
    content: counter(one) "."counter(two) "."counter(three) "- ";
  }
  //五级标题有点长了就关掉了
  // h5 {
  //   counter-reset: five;
  // }

  // h5:before {
  //   counter-increment: four;
  //   content: counter(one) "."counter(two) "."counter(three) "."counter(four) "- ";
  // }


}
```

## 其他说明

一部分ppt要求全部掌握或者内容比较复杂，直接使用的老师的ppt 就不上传了

