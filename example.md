# 相關範例

### PlantUML

表示流程或是狀態圖可以用 PlantUML 來呈現。底下是簡單的示範，其他不同的 UML 圖例和表示方法請參考 [PlantUML 文件](http://plantuml.com/zh/)。

{% uml src="plantuml_sample.puml" %}{% enduml %}

引用方式：

```
{% uml src="plantuml_sample.puml" %}{% enduml %}
```
### 圖片說明

引用圖例的效果則是 gitbook-image-caption 帶來的，可以看到圖片的底下會顯示說明以及章節編號。 

![GitBook 的 Icon](images/gitbook-logo.png)

## 命令列指令的顯示

用了 gitbook-terminal-plugin 套件之後，可以讓命令列的顯示更清晰，會有別於 code block。

```
**[terminal]
**[delimiter  $ ]**[command cat .bashrc]
```