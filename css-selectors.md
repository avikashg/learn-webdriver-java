# CSS Selector

### CSS with just tagname

```java
driver.findElement(By.cssSelector("a")) //finds first anchor tag
driver.findElement(By.cssSelector("input")) // finds first input tag
driver.findElement(By.cssSelector("div")) // finds first div tag
driver.findElements(By.cssSelector("button")) //finds all the button tags.
 ```

### CSS with Special Attributes id and class

id = #    e.g.,  tagname#idvalue   #idvalue
<br>
class = .  e.g.,  tagname.classvalue  .classvalue1.classvalue2
<br>
combination = tagname#idvalue.classvalue

```java
driver.findElement(By.cssSelector("a#log")) // finds anchor tag with id equal to log
driver.findElement(By.cssSelector("#log")) // finds any tag with id equal to log
driver.findElement(By.cssSelector(".classvalue")) // finds any tag with class 'classvalue'
driver.findElement(By.cssSelector("select.classvalue")) // finds select tag with class is equal to 'classvalue'
driver.findElement(By.cssSelector("select.classvalue1.classvalue2")) // finds select tag with classes classvalue1, classvalue2
driver.findElement(By.cssSelector("select#id1.classvalue1.classvalue2")) // finds select tag with id = id1 and classes classvalue1 and classvalue2
```



### CSS with other attributes 

 tagname[attributename='attributevalue']


```java
driver.findElement(By.cssSelector("input[attribute='value']")) //finds input with attribute have value
driver.findElement(By.cssSelector("input[attribute1='value1'][attribute2='value2']")) //finds input with attribute1 have value1 and attribute2 have input2
```



### css with starts-with(^), contains(*) and ends-with($)
select id="1234Qwerty123"
```java
driver.findElement(By.cssSelector("select[name^="123"]")) // startswith
driver.findElement(By.cssSelector("select[name*="qwerty"]")) //contains
driver.findElement(By.cssSelector("select[name$="123"]")) //ends-with
```


### CSS case insensitive

```java
driver.findElement(By.cssSelector("select[name="123" i]")) // letter i makes css selector as case insensitive

```

### CSS with attributes only

```java
driver.findElement(By.cssSelector("[name=abc]")) // find any element having name attribute having value abc
driver.findElement(By.cssSelector("[name]")) // find any element having name attribute


```


### CSS with negative query

```java
driver.findElements(By.cssSelector("not([name])")) // find all elements with no name attribute


```





