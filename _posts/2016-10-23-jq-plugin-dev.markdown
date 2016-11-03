---
layout:     post
title:      "jQuery插件开发"
subtitle:   "对象级插件、类别级插件"
date:       2016-10-23
author:     "fairyly"
header-img: "img/post-bg-js-module.jpg"
tags:
    - 前端开发
    - jq插件
    - jQuery
---



## jQuery插件开发

> Here we go!



---

## 对象级插件:

```
    ;(function($){
        $.fn.extend({
            "foucuscolor":function(li_col){
                  var def_col="#ccc";
                  var les_col="#fff";
                  li_col=(li_col==undefined)? def_col:li_col;
                  $(this).each(function(){
                    $(this).mouseover(function(){
                        $(this).css("background",li_col);
                    })
                    $(this).mouseout(function(){
                        $(this).css("background","yellow");
                    })
                  });
                  return $(this);
            }
        });
    })(jQuery);
    
```

---

## 类别级插件
   
   
```
    ;(function($){
       $.extend({
              "add":function(pr,prt){
                     var re=parseInt(pr)+parseInt(prt);
                     return re;
              },
              "sub":function(pr,prt){
                     var re=parseInt(pr)-parseInt(prt);
                     return re;
              },
              "plus":function(pr,prt){
                     var re=parseInt(pr)*parseInt(prt);
                     return re;
              }

       })
    })(jQuery);
    
```
   
   ---




 
> working  study......
