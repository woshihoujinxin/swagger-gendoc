#项目简介
> 本项目主要演示了将swagger-editor编辑好的swagger.yaml或swagger.json,转换为asciidoc,继而转换成其他各种格式,如:HTML、PDF、EPUB3、DOCBOOK等
  主要用到了两个maven插件:
   1. swagger2markup-maven-plugin
   2. asciidoctor-maven-plugin
> 基本的配置已经完成,不需要太大的改动。
> pdf主题配置过于耗时,这里只是简单设置了下,如果对样式不满意,可以自行参考官方文档配置pdf的样式

#如何使用
> 将swagger.yaml或swagger.json文件放入src/test/resources包,若是swagger.json格式的话需要修改pom.xml中定义的<swagger.input>属性。
> 因为用到的两个插件不会自动执行,所以指定了插件执行所在的阶段为test,故运行一下命令即可。
> `mvn test`
> 执行完毕后,将在target/asciidoc下看到生成的文档。

#注意事项
1. 若你设计的API中没有用TAG分类,则必须将pom中的<swagger2markup.pathsGroupedBy>TAGS</swagger2markup.pathsGroupedBy> 改为AS-IS或者直接注释掉

#联系方式
> * QQ: 574311651
> * email: woshihoujinxin@163.com
> * 个人博客: [www.houjinxin.com](www.houjinxin.com)

#参考链接:
> * [swagger2markupmaven插件官方文档](http://swagger2markup.github.io/swagger2markup/1.0.1/)
> * [asciidoctor maven插件官方文档](http://asciidoctor.org/docs/asciidoctor-maven-plugin/)
> * [pom中配置的asciidoctor属性说明](http://asciidoctor.org/docs/asciidoctor-maven-plugin/#configuration-options)
> * [asciidoctor maven插件中文说明](https://github.com/asciidoctor/asciidoctor-maven-plugin/blob/master/README_zh-CN.adoc)
> * [asciidoctor maven插件使用范例](https://github.com/asciidoctor/asciidoctor-maven-examples)
> * [pdf文件样式设置指引](https://github.com/asciidoctor/asciidoctor-pdf/blob/master/docs/theming-guide.adoc)
> * [pdf文件自定义字体设置参考](https://github.com/asciidoctor/asciidoctor-pdf/blob/master/docs/theming-guide.adoc#custom-fonts)

#其他
如果觉得不错,请加个星,不甚感激!!!