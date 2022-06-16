# SpreadJS_BindStyles_Tables
### 表格绑定时同时绑定样式
### SpreadJS 示例，基于 JavaScript组件实现包含合并单元格的数据绑定

该示例包括使用 SpreadJS API 的演示脚本，可用于实现包含合并单元格的数据绑定。
有关 SpreadJS API 的更多信息，请参阅[SpreadJS API指南]( https://demo.grapecity.com.cn/spreadjs/help/api/) 和[帮助手册]( https://help.grapecity.com.cn/pages/viewpage.action?pageId=5963808)。
 

目录：
-	运行步骤
-	控件初始化
-	示例代码
-	关于 SpreadJS
外部文件：
-	临时授权申请



### 运行步骤
1、在开始之前，请确保您已满足以下先决条件：

要运行 SpreadJS，浏览器必须支持 HTML5，客户端导入和导出 Excel 需要 IE10及以上。请先了解 [SpreadJS 的产品使用环境]( https://www.grapecity.com.cn/developer/spreadjs/selection-guide/product-use-environment)，并申请临时部署授权激活
安装并更新NodeJS和NPM
2、克隆或下载此代码库
3、初始化控件，并运行示例脚本

#### 控件初始化
1、	首先，创建一个新页面，并在页面上输入以下代码：
```
<!DOCTYPE html>
    <html>
    <head>
        <title>Spread HTML test page</title>
```
2、	在页面中添加对 Spread.JS 的引用。代码如下。需要注意的是，Spread 提供压缩过（minified）的 JavaScript 文件和和用于调试的文件：
```
<script src="[Your_Scripts_Path]/gc.spread.sheets.all.xxxx.min.js" type="text/javascript"></script>
```
3、添加 CSS 文件以改变Spread.JS 的外观。默认的CSS文件名为： gc.spread.sheets.xxxx.css，里面包含了所有的默认样式。该 CSS 文件将会影响滚动条，筛选框及其子元素，单元格和下方标签栏的样式。引入 CSS 的代码如下：
```
//<link href="[Your_CSS_Path]/gc.spread.sheets.xxxx.css" rel="stylesheet" type="text/css"/>
//OR
<link href="[Your_CSS_Path]/bootstrap/bootstrap.min.css" rel="stylesheet" type="text/css"/>
<link href="[Your_CSS_Path]/bootstrap/bootstrap-theme.min.css" rel="stylesheet" type="text/css"/>
```
4、添加产品授权，代码为：
```
GC.Spread.Sheets.LicenseKey = "xxx";
```
5、 添加控件初始化代码。本例会在一个 id 为“ss”的 DOM 元素上初始化 Spread.Sheets：
```
<script type="text/javascript">
// Add your license
 GC.Spread.Sheets.LicenseKey = "xxx";
// Add your code
 window.onload = function(){
var spread = new GC.Spread.Sheets.Workbook(document.getElementById("ss"),{sheetCount:3});
var sheet = spread.getActiveSheet();
 }
</script>
</head>
<body>
```
6、创建一个 id 为 “ss”的元素，Spread.Sheets 将在该 DOM 中初始化：
```
<div id="ss" style="height: 500px; width: 800px"></div>
</body>
</html>
```
#### 示例代码
```
HTML：
    <p>表格绑定时同时绑定样式</p>
    <div id='ss'></div>
CSS：
    #ss {
        height: 400px;
        width: 100%
    }
    
    p{
        color: #336699;
        text-align: center;
    }
JavaScript：
    // Title：绑定复制表格样式
    // Description：绑定复制表格样式
    // Tag：表格数据绑定，复制样式
    
    GC.Spread.Common.CultureManager.culture('zh-cn');
    
    $(document).ready(function() {
        var templateJSON = {
            "version": "10.0.1",
            "sheetCount": 2,
            "sheets": {
                "Sheet1": {
                    "name": "Sheet1",
                    "rowCount": 16,
                    "columnCount": 12,
                    "spans": [{
                        "row": 1,
                        "rowCount": 1,
                        "col": 1,
                        "colCount": 10
                    }],
                    "data": {
                        "dataTable": {
                            "1": {
                                "1": {
                                    "style": {
                                        "hAlign": 1,
                                        "vAlign": 1,
                                        "font": "bold 34.6667px Calibri"
                                    },
                                    "bindingPath": "Title"
                                },
                                "2": {
                                    "style": {
                                        "vAlign": 1,
                                        "font": "bold 34.6667px Calibri"
                                    }
                                },
                                "3": {
                                    "style": {
                                        "vAlign": 1,
                                        "font": "bold 34.6667px Calibri"
                                    }
                                },
                                "4": {
                                    "style": {
                                        "vAlign": 1,
                                        "font": "bold 34.6667px Calibri"
                                    }
                                },
                                "5": {
                                    "style": {
                                        "vAlign": 1,
                                        "font": "bold 34.6667px Calibri"
                                    }
                                },
                                "6": {
                                    "style": {
                                        "vAlign": 1,
                                        "font": "bold 34.6667px Calibri"
                                    }
                                },
                                "7": {
                                    "style": {
                                        "vAlign": 1,
                                        "font": "bold 34.6667px Calibri"
                                    }
                                },
                                "8": {
                                    "style": {
                                        "vAlign": 1,
                                        "font": "bold 34.6667px Calibri"
                                    }
                                },
                                "9": {
                                    "style": {
                                        "vAlign": 1,
                                        "font": "bold 34.6667px Calibri"
                                    }
                                },
                                "10": {
                                    "style": {
                                        "vAlign": 1,
                                        "font": "bold 34.6667px Calibri"
                                    }
                                }
                            },
                            "3": {
                                "1": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "2": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "3": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "4": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "5": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "6": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "7": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                }
                            },
                            "4": {
                                "1": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "2": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "3": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "4": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "5": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "6": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "7": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                }
                            },
                            "5": {
                                "1": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "2": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "3": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "4": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "5": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "6": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "7": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                }
                            },
                            "6": {
                                "1": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "2": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "3": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "4": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "5": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "6": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "7": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                }
                            },
                            "7": {
                                "1": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "4": {
                                    "value": "Total2",
                                    "style": {
                                        "autoFormatter": {},
                                        "labelOptions": {}
                                    }
                                },
                                "6": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "7": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                }
                            },
                            "8": {
                                "1": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "2": {
                                    "style": {
                                        "formatter": "0.00",
                                        "labelOptions": {}
                                    }
                                },
                                "3": {
                                    "style": {
                                        "formatter": "$#,##0.00",
                                        "labelOptions": {}
                                    }
                                },
                                "4": {
                                    "value": 0,
                                    "style": {
                                        "foreColor": "rgb(255, 0, 0)",
                                        "formatter": "$#,##0.00",
                                        "labelOptions": {}
                                    },
                                    "formula": "gcTable0[[#This Row], [Quantity]]*gcTable0[[#This Row], [Price]]"
                                },
                                "6": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "7": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                }
                            },
                            "9": {
                                "1": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "2": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "3": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "4": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "5": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "6": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "7": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                }
                            },
                            "10": {
                                "1": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "2": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "3": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "4": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "5": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "6": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "7": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                }
                            },
                            "11": {
                                "1": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "2": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "3": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "4": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "5": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "6": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "7": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                }
                            },
                            "12": {
                                "1": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "2": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "3": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "4": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "5": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "6": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "7": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                }
                            },
                            "13": {
                                "1": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "2": {
                                    "style": {
                                        "labelOptions": {}
                                    }
                                },
                                "3": {
                                    "style": {
                                        "labelOptions": {}
                                    }
                                },
                                "4": {
                                    "value": "Age2",
                                    "style": {
                                        "autoFormatter": {},
                                        "labelOptions": {}
                                    }
                                },
                                "5": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "6": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "7": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                }
                            },
                            "14": {
                                "1": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "2": {
                                    "style": {
                                        "backColor": "Accent 6 60",
                                        "labelOptions": {}
                                    }
                                },
                                "3": {
                                    "style": {
                                        "backColor": "Accent 6 60",
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "formatter": "yyyy年m月d日",
                                        "locked": true,
                                        "textIndent": null,
                                        "labelOptions": {}
                                    }
                                },
                                "4": {
                                    "value": 118,
                                    "style": {
                                        "backColor": "Accent 6 60",
                                        "labelOptions": {}
                                    },
                                    "formula": "YEAR(TODAY())-YEAR(D15)"
                                },
                                "5": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "6": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "7": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                }
                            },
                            "15": {
                                "1": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "2": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "3": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "4": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "5": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "6": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                },
                                "7": {
                                    "style": {
                                        "hAlign": 3,
                                        "vAlign": 0,
                                        "themeFont": "Body",
                                        "imeMode": 1,
                                        "labelOptions": {}
                                    }
                                }
                            }
                        },
                        "defaultDataNode": {
                            "style": {
                                "themeFont": "Body"
                            }
                        }
                    },
                    "rowHeaderData": {
                        "defaultDataNode": {
                            "style": {
                                "themeFont": "Body"
                            }
                        }
                    },
                    "colHeaderData": {
                        "defaultDataNode": {
                            "style": {
                                "themeFont": "Body"
                            }
                        }
                    },
                    "selections": {
                        "0": {
                            "row": 0,
                            "rowCount": 1,
                            "col": 0,
                            "colCount": 1
                        },
                        "length": 1
                    },
                    "theme": "Office",
                    "rows": [{
                        "size": 39
                    }, {
                        "size": 66
                    }],
                    "columns": [{
                        "size": 40
                    }, {
                        "size": 40
                    }, {
                        "size": 77
                    }, {
                        "size": 97
                    }, null, {
                        "size": 71
                    }, {
                        "size": 75
                    }, null, null, null, null, {
                        "size": 31
                    }],
                    "tables": [{
                        "name": "gcTable1",
                        "row": 13,
                        "col": 2,
                        "rowCount": 2,
                        "colCount": 3,
                        "style": {
                            "buildInName": "Medium2"
                        },
                        "autoGenerateColumns": false,
                        "bindingPath": "C_Table",
                        "rowFilter": {
                            "range": {
                                "row": 14,
                                "rowCount": 1,
                                "col": 2,
                                "colCount": 3
                            },
                            "typeName": "HideRowFilter",
                            "filterButtonVisibleInfo": {
                                "0": true,
                                "1": true,
                                "2": true
                            },
                            "showFilterButton": true
                        },
                        "columns": [{
                            "id": 1,
                            "name": "Person",
                            "dataField": "Person"
                        }, {
                            "id": 2,
                            "name": "Birthday",
                            "dataField": "Birthday"
                        }, {
                            "id": 3,
                            "name": "Age2"
                        }]
                    }, {
                        "name": "gcTable0",
                        "row": 7,
                        "col": 2,
                        "rowCount": 2,
                        "colCount": 4,
                        "style": {
                            "buildInName": "Medium2"
                        },
                        "autoGenerateColumns": false,
                        "bindingPath": "B_Table",
                        "rowFilter": {
                            "range": {
                                "row": 8,
                                "rowCount": 1,
                                "col": 2,
                                "colCount": 4
                            },
                            "typeName": "HideRowFilter",
                            "filterButtonVisibleInfo": {
                                "0": true,
                                "1": true,
                                "2": true,
                                "3": true
                            },
                            "showFilterButton": true
                        },
                        "columns": [{
                            "id": 1,
                            "name": "Quantity",
                            "dataField": "Quantity"
                        }, {
                            "id": 2,
                            "name": "Price",
                            "dataField": "Price"
                        }, {
                            "id": 3,
                            "name": "Total2"
                        }, {
                            "id": 4,
                            "name": "Date",
                            "dataField": "Date"
                        }]
                    }],
                    "index": 0
                },
                "Sheet2": {
                    "name": "Sheet2",
                    "data": {
                        "dataTable": {}
                    },
                    "selections": {
                        "0": {
                            "row": 0,
                            "rowCount": 1,
                            "col": 0,
                            "colCount": 1
                        },
                        "length": 1
                    },
                    "theme": "Office",
                    "index": 1
                }
            },
            "designerBindingPathSchema": {
                "$schema": "http://json-schema.org/draft-04/schema#",
                "properties": {
                    "B_Table": {
                        "dataFieldType": "table",
                        "type": "array",
                        "items": {
                            "type": "object",
                            "properties": {
                                "Quantity": {
                                    "type": "string"
                                },
                                "Price": {
                                    "type": "string"
                                },
                                "Date": {
                                    "type": "string"
                                }
                            }
                        }
                    },
                    "C_Table": {
                        "dataFieldType": "table",
                        "type": "array",
                        "items": {
                            "type": "object",
                            "properties": {
                                "Person": {
                                    "dataFieldType": "table",
                                    "type": "array"
                                },
                                "Birthday": {
                                    "type": "string"
                                }
                            }
                        }
                    },
                    "Title": {
                        "dataFieldType": "text",
                        "type": "string"
                    }
                },
                "type": "object"
            }
        }
        var data = {
            Title: "表格绑定样式",
            Sex: "男",
            B_Table: [{
                Quantity: 2,
                Price: 30.3,
                Date: "2017/8/5"
            }, {
                Quantity: 3,
                Price: 30.31,
                Date: "2013/8/5"
            }, {
                Quantity: 11,
                Price: 130.3,
                Date: "2017/5/5"
            }],
            C_Table: [{
                Person: "Super Man",
                Birthday: "2011/3/3"
            }, {
                Person: "Batman",
                Birthday: "2000/3/3"
            }, {
                Person: "Ant",
                Birthday: "2013/3/3"
            }, {
                Person: "Iron Man",
                Birthday: "1911/6/3"
            }]
        }
        var spread = new GC.Spread.Sheets.Workbook(document.getElementById("ss"));
        spread.suspendPaint();
    
        spread.fromJSON(templateJSON);
        var sheet = spread.getActiveSheet();
        sheet.setRowCount(50)
        var source = new GC.Spread.Sheets.Bindings.CellBindingSource(data);
        sheet.setDataSource(source);
        spread.resumePaint();
        sheet.setRowHeight(8, 30);
        sheet.getRange(8, 2, 1, 4).vAlign(GC.Spread.Sheets.VerticalAlign.center);
        sheet.getCell(8, 1).value("Detail").vAlign(GC.Spread.Sheets.VerticalAlign.center);
    
        var tables = sheet.tables.all();
        if (tables) {
            for (var i = 0; i < tables.length; i++) {
                copyTableStyle(sheet, tables[i])
            }
        }
        spread.resumePaint();
    });
    
    function copyTableStyle(sheet, table) {
        var range = table.dataRange();
        var rowHeight = sheet.getRowHeight(range.row);
        for (var i = 1; i < range.rowCount; i++) {
            // Copy Style
            sheet.copyTo(range.row + i - 1, range.col, range.row + i, range.col, 1, range.colCount, GC.Spread.Sheets.CopyToOptions.style);
            // Copy Formula
            sheet.copyTo(range.row + i - 1, range.col, range.row + i, range.col, 1, range.colCount, GC.Spread.Sheets.CopyToOptions.formula);
            // Copy Span
            sheet.copyTo(range.row + i - 1, range.col, range.row + i, range.col, 1, range.colCount, GC.Spread.Sheets.CopyToOptions.span);
            // Set Row Height
            sheet.setRowHeight(range.row + i, rowHeight);
    
    
            //copyCustomerTableRowHeader
            sheet.copyTo(range.row + i - 1, 0, range.row + i, 0, 1, range.col, GC.Spread.Sheets.CopyToOptions.style);
            sheet.copyTo(range.row + i - 1, 0, range.row + i, 0, 1, range.col, GC.Spread.Sheets.CopyToOptions.value);
        }
}
```
#### 关于 SpreadJS
[SpreadJS]( https://www.grapecity.com.cn/developer/spreadjs) 是一款基于 HTML5 的纯前端表格控件，兼容 450 多种 Excel 公式，具备“高性能、跨平台、与 Excel 高度兼容”的产品特性。使用 SpreadJS，可直接在 Angular、 React、 Vue 等前端框架中实现高效的模板设计、在线编辑和数据绑定等功能，为最终用户提供高度类似 Excel 的使用体验。
 

