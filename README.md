# Blogger-Template-Development

## 1.1 First Insert Demo Code
```
<?xml version="1.0" encoding="UTF-8" ?>
<!DOCTYPE html>
<html b:css='false' b:defaultwidgetversion='2' b:layoutsVersion='3' b:responsive='true' b:templateUrl='indie.xml' b:templateVersion='1.3.3' expr:dir='data:blog.languageDirection' expr:lang='data:blog.locale' xmlns='http://www.w3.org/1999/xhtml' xmlns:b='http://www.google.com/2005/gml/b' xmlns:data='http://www.google.com/2005/gml/data' xmlns:expr='http://www.google.com/2005/gml/expr'>
  <head>
    <title>
      <data:blog.title/>
    </title>
  </head>
  
  <body>
    <h1>Hellow Word</h1>
  </body>
  
</html>
```

## 1.2 In the head section after </title>
```
    <!--CSS For Web Page-->
    <b:skin>
</b:skin>
```  
  
## 1.3 In body Section

```
    <!--CSS For Web Page-->

    <b:section id='Layout_ID'/>
    <h1>Hellow Word</h1>
```
### After The </b:skin>

```
     <!--CSS For Layout-->
    
    <b:template-skin><![CDATA[
    ]]></b:template-skin>
```
