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
## 1.4 After The </b:skin>

```
     <!--CSS For Layout-->
    
    <b:template-skin><![CDATA[
    ]]></b:template-skin>
```
## 1.5 Meta tag add after  </title>

```
 <!--Meta Tags-->

  <meta charset='UTF-8'/>
  <meta content='width=device-width, initial-scale=1, minimum-scale=1, maximum-scale-1' name='viewport'/>
```

## 1.6 After the <b:skin><![CDATA[

```
   *{
margin:0;
padding:0;
box-sizing:border-box;
    }
```

## 1.7 In body Remove all and add this. Layout section we can see our changes

```
  <b:section class='header-section' id='header' name='header area'/>
```
# 2.0 If condition
## 2.1 After   meta content='width=device-width, initial-scale=1, minimum-scale=1, maximum-scale-1' name='viewport'/> add

```
<b:if cond='!data:view.isLayoutMode'>
```

## 2.2 After the 	]]></b:skin add this and save

```
  </b:if>
```

## 2.3 After     --CSS For Layout-->

```
 <b:if cond='data:view.isLayoutMode'>
```

## 2.4 After /b:template-skin>

```
 </b:if>
```

## 2.5 After <-- CSS For web page--> them *{} css then add

```
html{
overflow-x:hidden;
-webkit-text-size-adjust:100%;
-ms-text-size-adjust:100%;
}

img{
max-width:100%;
}

a{
color:inherit;
text-decoration:none;
}
```

## 2.6 Before  /body> add this for display something in my webpage

```
 <h1>Wellcome To Our Website</h1>
```
# 3 Header Design
## 3.1 !--CSS For Web Page--> then <a then add

```
.widget{
margin:0;
padding:0;
line-height:unset;
}

.widget li, li{
margin:0;
padding:0;
text-indent:0;
}

.section{
margin:0;
padding:0;
}
```
## 3.2 In body Section remove all and add

```
 <!-- Header Section Start -->
    
    <header id='header'>
      
      <b:section id='header-section' maxwidgets='2' name='Header Section'/>
      
    </header>
    
    <!-- Header Section End -->

```
