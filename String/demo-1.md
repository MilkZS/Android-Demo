#### 将一段字符串转为带省略号的字段

```
public String getStr(String str，int length){
  if(str.length() > length){//字符串的长度 可修改
    return str.substring(0,length) + "....";//substring()方法的使用
  }
 
  if(str.length() == 0 || str == ""){
    return "";
  }else{
    return str;
  }
}
```



